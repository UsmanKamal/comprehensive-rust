# Unit Tests

Mark unit tests with `#[test]`:

```rust,editable
fn first_word(text: &str) -> &str {
    match text.find(' ') {
        Some(idx) => &text[..idx],
        None => &text,
    }
}

#[test]
fn test_empty() {
    assert_eq!(first_word(""), "");
}

#[test]
fn test_single_word() {
    assert_eq!(first_word("Hello"), Some("Hello"));
}

#[test]
fn test_multiple_words() {
    assert_eq!(first_word("Hello World"), Some("Hello"));
}
```

Use `cargo test` to find and run the unit tests.
