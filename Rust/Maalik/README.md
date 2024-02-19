Maalik
=

Maalik you are the real owner of the flag.

### Netcat: nc rust02.ctf.teamquark.com 65332

### Author: Piyush Waghulde

### Files: [rust2.zip](./rust2.zip)

Solution
=

By looking at the source code, I notice that we can actually print out the value required since its coded in such a way. I made a script which printed the value we need:

```rust
struct PuzzleResult {
    result: String,
}

fn main() {
    let puzzle_result = PuzzleResult::new("Rust");
    println!("{}", puzzle_result.result);
}

impl PuzzleResult {
    fn new(initial: &str) -> PuzzleResult {
        let mut s_result = String::from(initial);

        fn1(&mut s_result);
        s_result = fn2(s_result.clone());
        

        let mut m_result = s_result.clone();
        let i_variable = 42;
        
        m_result.push_str(&i_variable.to_string());
        
        let parsed_i_variable: i32 = m_result.chars().filter(|c| c.is_digit(10)).collect::<String>().parse().expect("Failed to parse integer");
        m_result = (parsed_i_variable * 3).to_string();
        let a_variable = 10;

        m_result.push_str(&a_variable.to_string());

        let parsed_a_variable: i32 = m_result.parse().expect("Failed to parse integer");
        m_result = (parsed_a_variable - a_variable).to_string();

        PuzzleResult { result: m_result }
    }

    fn validate_answer(&self, user_input: &str) -> bool {
        user_input.trim() == self.result
    }
}

fn fn1(s: &mut String) {
    let reversed: String = s.chars().rev().enumerate().map(|(i, c)| if i % 2 == 0 { c.to_uppercase().next().unwrap() } else { c }).collect();
    s.clear();
    s.push_str(&reversed);
}

fn fn2(s: String) -> String {
    let mut encoded: Vec<char> = s.chars().map(|c| {
        match c {
            'a'..='z' => ((c as u8 - b'a' + 13) % 26 + b'a') as char,
            'A'..='Z' => ((c as u8 - b'A' + 13) % 26 + b'A') as char,
            '0'..='9' => ((c as u8 - b'0' + 5) % 10 + b'0') as char,
            _ => c,
        }
    }).collect();
    encoded.reverse();
    encoded.into_iter().collect()
}
```

Running this script gives us the value of `12600`, and by putting it in the app, we get the flag!

`quarkCTF{j0_bh1_l@n@_d0_l@n@}`
