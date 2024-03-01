# Doubly Linked List

Doubly-Linked-List implementation in Rust

## Run

```bash
cargo run --package doubly-linked-list --bin doubly-linked-list
```

## usage

```rust
use std::fmt::Debug;

mod doubly_linked_list;

use crate::doubly_linked_list::Drop;
use doubly_linked_list::DoublyLinkedList;

#[derive(Debug, PartialEq, PartialOrd)]
pub struct Person {
    name: String,
    age: u8,
    height: f32,
}

fn main() {
    let mut dl: DoublyLinkedList<Person> = DoublyLinkedList::new();

    dl.push_back(Person {
        name: String::from("John"),
        age: 15,
        height: 1.7,
    });

    dl.push_back(Person {
        name: String::from("John"),
        age: 25,
        height: 2.0,
    });

    dl.push_back(Person {
        name: String::from("John"),
        age: 18,
        height: 2.0,
    });
    
    dl.push(
        Person {
            name: String::from("Emily"),
            age: 12,
            height: 1.25,
        },
        3,
    );
    
    println!("The first element: {:?}", dl.get(0));
}
```
