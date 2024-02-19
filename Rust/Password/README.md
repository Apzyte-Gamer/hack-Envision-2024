Password
=

Password can only contain: .... Nahhhh!! we don't do that here.

### Connection: nc rust03.ctf.teamquark.com 65333

### Author: Rahul Sundkar

Understanding the Code
=

Opening the code, I saw what password we need to get the flag and saw `\^Z[_c[``[\b`. This string was encoded by the do_something function.

```rust
fn do_something(password: &str) -> String {
        let mut some_string = String::new();
        
        for byte in password.trim().bytes() {
            byte
            .to_string()
            .chars()
            .for_each(|ch| {
                some_string.push(char::from_u32(ch.to_digit(10).expect("Valid Digit") + 90 ).expect("Valid ASCII code"))
            });
        }
        
        some_string
    }
```

To obtain the password, we need to reverse this, so lets get to it!

Reversing do_something()
=

If you understand the code well enough, you can see that for each character in the string `\^Z[_c[``[\b`, the original value of the character is turned to decimal and is being added to 90 and then getting converted to ASCII. So, we can easily reverse this by this piece of code:

```rust
fn reverse_string(some_string: &str) -> String {
    let mut password = String::new();

    for ch in some_string.chars() {
        let digit = ch as u32 - 90;
        if let Some(byte) = char::from_digit(digit, 10) {
            password.push(byte);
        } else {
            // Handle invalid digit
            panic!("Invalid digit");
        }
    }

    password
}

fn main() {
    let some_string = r"\^Z[_c[``[\b";
    let reversed_password = reverse_string(some_string);

    println!("Reversed Password: {}", reversed_password);
}
```

Running this gives us the password as `240159166128`, which on checking with the netcat server DOESN'T work. So this means either 2 things:

1) we have to reverse more
2) our algorithm is wrong

Upon asking the admins, they said to reverse more, so I started looking up what could we reverse more in `240159166128`. I searched for a while until I found out that `240159166128` was a Vector of Bytes and we could turn it to a string. I did this by this code:

```rust
fn main() {
    let bytes = vec![240, 159, 166, 128];
    let string = String::from_utf8_lossy(&bytes);

    println!("Converted String: {}", string);
}
```

Running this code strangely gives us `🦀`, and putting this in the netcat server gives us the flag!

`quarkCTF{3m0j1s_4r3_7h3_n3w_h13r09lyph1c5}`
