# Show me The code

From **Python** to **Rust** by examples  

> You can  copy-paste and run the **Rust** examples in https://play.rust-lang.org/ and **Python** in https://repl.it/languages/python3 


### Creating a new project

Create a new project with basic files, entry points, module initializer, dependency and installation artifacts.

**Python**

```bash
$ mkdir {pyproject,pyproject/src}
$ touch {pyproject/src/{__init__.py,__main__.py,program.py},pyproject/{requirements.txt,setup.py}} 
$ echo "-e ." >> pyproject/requirements.txt
$ echo "from setuptools import setup" >> pyproject/setup.py
$ echo "setup(author=..., name=...)" >> pyproject/setup.py
```

**Rust**

```bash
$ cargo new my-rust-program
```

---

### Installing new libraries/crates

**Python**

```bash
$ pip install foo 
```


**Rust**

```bash
$ cargo install foo
```

---

### Running / Compiling

**Python**

```bash
$ python my_python_program.py 
```


**Rust**

```bash
$ cargo run
```

In Rust, there is a `--release` flag that allows for more compile time optimization to be done, but it will take longer to compile

```bash
$ cargo run --release
```

---

### Hello World

**Python**

```python
if __name__ == "__main__":
    print("Hello, World")
```

**Rust**

```rust
fn main() {
  println!("Hello, World");
}
```

---

### Types and Declarations

Create new objects, values on basic primitive types and also data structures.

**Python**

```python
age = 80
name = 'daffy'
weight = 62.3
loons = ['bugs', 'daffy', 'taz']
ages = {  # Ages for 2017
    'daffy': 80,
    'bugs': 79,
    'taz': 63,
}
```

**Rust**

```rust
use std::collections::HashMap;

fn main() {
    let age = 80;
    let name = "daffy";
    let weight = 62.3;
    let mut loons = vec!["bugs", "daffy", "taz"];

    let mut ages = HashMap::new();  // Ages for 2017
    ages.insert("daffy", 80);
    ages.insert("bugs", 79);
    ages.insert("taz", 63);
}

```
---

### Define a function

Defining a function that takes 2 integer arguments and returns its sum.

**Python**

```python
def add(a, b):
    """Adds a to b"""
    return a + b
```
**Python with typing annotations**

It looks more similar to Rust.

```python
def add(a: int, b: int) -> int:
    """Adds a to b"""
    return a + b
```

**Rust**

```rust
/// Adds a to b
fn add(a: i32, b: i32) -> i32 {
  a + b
}
```

---

### List/Slice

Creating a list, adding new elements, gettings its length, slicing by index, iterating using for loop and iterating with enumerator.

**Python**

```python
names = ['bugs', 'taz', 'tweety']
print(names[0])  # bugs
names.append('elmer')
print(len(names))  # 4
print(names[2:])  # ['tweety', 'elmer']

for name in names:
    print(name)

for i, name in enumerate(names):
    print('{} at {}'.format(name, i))
```

**Rust**

```rust
fn main() {
    let mut names = vec!["bugs", "taz", "tweety"];
    println!("{}", names[0]);  // bugs
    names.push("elmer");
    println!("{}", names.len());  // 4
    println!("{:?}", &names[2..]);  // ["tweety", "elmer"]

    for name in &names {
        println!("{}", name);
    }

    for (i, name) in names.iter().enumerate() {
        println!("{} at {}", i, name);
    }
}
```

**.step_by()** is the equivalent for python's range/xrange step parameter.

python:
```py
for i in range(0,10,2):
   print(i) # 0, 2, 4, 6, 8
```

rust:
```rust
for i in (0..10).step_by(2) {
    println!("{}", i);  // 0, 2, 4, 6, 8
}
```

---

### Dict/Map

Create new dictionaries (hash maps), adding new keys and values, changing values, getting by key, checking if a key is containing, etc.

**Python**

```python

# Creating a new dict and populating it
ages = {}
ages['daffy'] = 80
ages['bugs'] = 79
ages['taz'] = 63

# or doing the same using a for loop
ages = {}
for name, age in [("daffy", 80), ("bugs", 79), ("taz", 63)]:
    ages[name] = age

# or initializing from a list
ages = dict([("daffy", 80), ("bugs", 79), ("taz", 63)])

# or passing key values on creation
ages = {  # Ages for 2017
    'daffy': 80,
    'bugs': 79,
    'taz': 63,
}

ages['elmer'] = 80
print(ages['bugs'])  # 79
print('bugs' in ages)  # True

del ages['taz']

for name in ages:  # Keys
    print(name)

for name, age in ages.items():  # Keys & values
    print('{} is {} years old'.format(name, age))
```

**Rust**

```rust
use std::iter::FromIterator;
use std::collections::HashMap;

fn main() {

    // Creating a new HashMap and populating it
    let mut ages = HashMap::new();  // Ages for 2017
    ages.insert("daffy", 80);
    ages.insert("bugs", 79);
    ages.insert("taz", 63);

    // or doing the same using a loop
    let mut ages = HashMap::new();
    for &(name, age) in [("daffy", 80), ("bugs", 79), ("taz", 63)].iter() {
        // For non-Copy data, remove & and use iter().clone()
        ages.insert(name, age);
    }

    // or initializing from Array
    let mut ages: HashMap<&str, i32> =  // Ages for 2017
        [("daffy", 80), 
         ("bugs", 79), 
         ("taz", 63)]
        .iter().cloned().collect();

    // or initializing from Vec (Iterator)
    let mut ages: HashMap<&str, i32> =  // Ages for 2017
        HashMap::from_iter(
            vec![
               ("daffy", 80),
               ("bugs", 79),
               ("taz", 63)
            ]
        );

    ages.insert("elmer", 80);
    println!("{}", ages["bugs"]);  // 79
    println!("{}", ages.contains_key("bugs")); // true
    ages.remove("taz");


    for name in ages.keys() {  // Keys
      println!("{}", name);
    }

    for (name, age) in &ages {  // Keys & values
      println!("{} is {} years old", name, age);
    }

}
```

#### Pythonic alternative to dict/map in Rust

You can use the [maplit](https://crates.io/crates/maplit) crate to load `hashmap!` macro to have an efficient sugared (a.k.a Pythonic) syntax!

```toml
# Cargo.toml
[dependencies]
maplit = "*"
```

then

```rust
#[macro_use] extern crate maplit;

let map = hashmap!{
    "daffy" => 80,
    "bugs" => 79,
    "taz" => 63,
};
```

---

### set / HashSet

Create a `set` (a hash of unique keys), add new keys and compute `intersection`, `difference` and `union`

**Python**

```python

# creating and populating
colors = set()
colors.add("red")
colors.add("green")
colors.add("blue")
colors.add("blue")

# using literal syntax
colors = {'red', 'green', 'blue', 'blue'}

# from an iterator
colors = set(['red', 'green', 'blue', 'blue'])


# deduplication
print(colors)  # {"blue", "green", "red"}

# operations
colors = {'red', 'green', 'blue', 'blue'}
flag_colors = {"red", "black"}

# difference
colors.difference(flag_colors)  # {'blue', 'green'}

# symmetric difference
colors.symmetric_difference(flag_colors)  # {'black', 'blue', 'green'}

# intersection
colors.intersection(flag_colors)  # {'red'}

# union
colors.union(flag_colors)  # {'black', 'blue', 'green', 'red'}

```

**Rust**

```rust
use std::collections::HashSet;
use std::iter::FromIterator;

fn main() {

    // creating and populating - type inference
    let mut colors = HashSet::new();
    colors.insert("red");
    colors.insert("green");
    colors.insert("blue");
    colors.insert("blue");

    // from an iterator - explicit type
    let mut colors: HashSet<&str> = HashSet::from_iter(vec!["red", "green", "blue", "blue"]);

    // deduplication
    println!("{:?}", colors); // {"blue", "green", "red"}

    // Operations
    let mut colors: HashSet<&str> = HashSet::from_iter(vec!["red", "green", "blue", "blue"]);
    let mut flag_colors: HashSet<&str> = HashSet::from_iter(vec!["red", "black"]);

    // difference
    colors.difference(&flag_colors); // ["green", "blue"]

    // symmetric difference
    colors.symmetric_difference(&flag_colors); // ["blue", "green", "black"]

    // intersection
    colors.intersection(&flag_colors); // ["red"]

    // union
    colors.union(&flag_colors); // ["red", "blue", "green", "black"]
}
```

or syntax sugared using [maplit](https://crates.io/crates/maplit) crate

```rust
#[macro_use] extern crate maplit;

let colors = hashset!{"red", "green", "blue", "blue"};
```

---

### while and for loops

Looping until a condition is met or over an iterable object.

**Python**

```python
# While loop

counter = 0
while counter < 10:
    print(counter)
    counter += 1

# infinite while loop
while True:
    print("loop Forever!")

# infinite while loop with break
counter = 0
while True:
    print(counter)
    counter += 1
    if counter >= 10:
        break


# while loop with continue
counter = 0
while True:
    counter += 1
    if counter == 5:
        continue
    print(counter)
    if counter >= 10:
        break

# For loop over a list
for color in ["red", "green", "blue"]:
    print(color)

# Enumerating indexes
for  i, color in enumerate(["red", "green", "blue"]):
    print(f"{color} at index {i}")

# For in a range
for number in range(0, 100):
    print(number)  # from 0 to 99

```

**Rust**

```rust
fn main() {

    // While loop
    let mut counter = 0;
    while counter < 10 {
        println!("{}", counter);
        counter += 1;
    }

    // infinite while loop
    loop {
        println!("Loop forever!");
    }

    // infinite while loop with break
    let mut counter = 0;
    loop {
        println!("{}", counter);
        counter += 1;
        if counter >= 10 { break; }
    }

    // infinite while loop with continue
    let mut counter = 0;
    loop {
        counter += 1;
        if counter == 5 { continue; }
        println!("{}", counter);
        if counter >= 10 { break; }
    }

    // for loop over a list
    for color in ["red", "green", "blue"].iter() {
        println!("{}", color);
    }

    // Enumerating indexes
    for (i, color) in ["red", "green", "blue"].iter().enumerate() {
        println!("{} at index {}", color, i);
    }

    // for in a range
    for number in 0..100 {
        println!("{}", number);  // from 0 to 99
    }
}
```

#### Loop Labels

**Rust** has a looping feature which is not present on Python: **Loop labels**

```rust
'outer: for x in 0..10 {
    'inner: for y in 0..10 {
        if x % 2 == 0 { continue 'outer; } // continues the loop over x
        if y % 2 == 0 { continue 'inner; } // continues the loop over y
        println!("x: {}, y: {}", x, y);
    }
}
```

---

### Files

Read a text file and iterate its lines printing the content, properly close the file at the end.

**Python**

```python
from pathlib import Path

with Path("/tmp/song.txt").open() as fp:
    #  Iterate over lines
    for line in fp:
        print(line.strip())
```

**Rust**

```rust
use std::io::{BufReader, BufRead};
use std::fs::File;
use std::path::Path;


fn main () {
    let fp = File::open(Path::new("/tmp/song.txt")).unwrap();
    let file = BufReader::new(&fp);
    for line in file.lines() {
        //  Iterate over lines
        println!("{}", line.unwrap());
    }
}

```

---

### Exceptions/Return Error

Expecting for exceptions and identifying errors.

**Python**

```python
def div(a, b):
    if b == 0:
        raise ValueError("b can't be 0")
    return a / b

# ...

try:
    div(1, 0)
except ValueError:
    print('An error occurred!')
```

**Rust**

```rust
fn div(a: i32, b: i32) -> Result<i32, &'static str> {
    if b == 0 {
        Err("b can't be 0")
    } else {
        Ok(a / b)
    }
}

fn main() {
    match div(1, 0) {
        Ok(_) => {},
        Err(_) => println!("An error occurred!"),
    };
}
```

---

### Concurrency

**Python**

```python
thr = Thread(target=add, args=(1, 2), daemon=True)
thr.start()
```

**Rust**

```rust
use std::thread;

thread::spawn(|| {
        add(5,5);
    });

```

---

### Communicating between threads

Managing data context between threads.

**Python**

```python
from queue import Queue
queue = Queue()
# ...
# Send message from a thread
queue.put(353)


# ...
# Get message to a thread
val = queue.get()
```

**Rust**

```rust
use std::thread;
use std::sync::mpsc;

fn main() {
    let (tx, rx) = mpsc::channel();

    let sender = thread::spawn(move || {
        let val = String::from("hi");
        tx.send(val.clone()).unwrap();
        println!("Sent {}", val);
    });

    let receiver = thread::spawn(move || {
        let received = rx.recv().unwrap();
        println!("Received: {}", received);
    });

    sender.join();
    receiver.join();
}
```

---

### Sorting

Sorting lists, reversing and using a key.

**Python**

```python
names = ['taz', 'bugs', 'daffy']

# Lexicographical order
names.sort()

# Reversed lexicographical order
names.sort(reverse=True)

# Sort by length
names.sort(key=len)
```

**Rust**

```rust
fn main() {
    let mut names = ["taz", "bugs", "daffy"];

    // Lexicographical order
    names.sort();

    // Reversed lexicographical order
    names.sort_by(|a, b| b.cmp(a));

    // Sort by length
    names.sort_by_key(|a| a.len());
}
```

---

### Web app with Flask / Rocket

**Python**

```python
from flask import Flask

app = Flask(__name__)


@app.route('/')
def index():
    return 'Hello Python'


if __name__ == '__main__':
    app.run(port=8080)
```

**Rust**

```rust
#![feature(plugin)]
#![plugin(rocket_codegen)]

extern crate rocket;

#[get("/")]
fn index() -> &'static str {
    "Hello Rust"
}

fn main() {
    rocket::ignite().mount("/", routes![index]).launch();
}
```

---

### HTTP Request with error handling

**Python**

Using [**requests**](http://pypi.org/project/requests)

```python
import requests

url = 'https://httpbin.org/ip'

try:
    resp = requests.get(url)
except HTTPError as err:
    msg = f"error: cannot get {url} - {err}"
    raise SystemExit(msg)

assert resp.status_code == 200

print(f"The response content is: {resp.content}")

```

**Rust**

using [**reqwest**](https://crates.io/crates/reqwest)

```rust
extern crate reqwest;
use std::io::Read;

fn main() {
    let url = "https://httpbin.org/ip";

    let mut resp = match reqwest::get(url) {
        Ok(response) => response,
        Err(e) => panic!("error: could not perform get request {}", e),
    };

    assert!(resp.status().is_success());

    let mut content = String::new();
    resp.read_to_string(&mut content).expect("valid UTF-8");

    println!("The response content is: {}", content);
}
```

---

### Multithreaded HTTP Crawler

**Python**

Using [**requests**](http://pypi.org/project/requests)

```python
from concurrent.futures import ThreadPoolExecutor
import requests


URLS = (
    "https://httpbin.org/html",
    "https://httpbin.org/links/10/0",
    "https://httpbin.org/robots.txt",
    "https://httpbin.org/user-agent",
    "https://httpbin.org/links/10/0",
    "https://httpbin.org/robots.txt",
    "https://httpbin.org/xml",
    "https://httpbin.org/redirect/1",
    "https://httpbin.org/redirect/2",
    "https://httpbin.org/cookies",
    "https://httpbin.org/basic-auth/user/passwd",
    "https://httpbin.org/gzip",
)


def crawl_worker(url):
    try:
        print(f"Response of url: {url} is {requests.get(url).status_code}")
    except Exception:
        print("Failed to get url.")


if __name__ == "__main__":
    with ThreadPoolExecutor() as executor:
        executor.map(crawl_worker, URLS)
```

**Rust**

using [**reqwest**](https://crates.io/crates/reqwest)

```rust
extern crate reqwest;
use std::thread;


fn crawl_worker(url: &str) {
    let parsed_url = reqwest::Url::parse(url).expect("Bad url format.");
    let response = reqwest::get(parsed_url).expect("Failed to get url.");
    println!("Response of url: {} is {:?}", url, response.status().to_string());
}


fn main() {
    let urls = vec![
        "https://httpbin.org/html",
        "https://httpbin.org/links/10/0",
        "https://httpbin.org/robots.txt",
        "https://httpbin.org/user-agent",
        "https://httpbin.org/links/10/0",
        "https://httpbin.org/robots.txt",
        "https://httpbin.org/xml",
        "https://httpbin.org/redirect/1",
        "https://httpbin.org/redirect/2",
        "https://httpbin.org/cookies",
        "https://httpbin.org/basic-auth/user/passwd",
        "https://httpbin.org/gzip",
    ];
    let mut queue = vec![];

    for url in urls {
        queue.push(thread::spawn(move || {
            crawl_worker(url);
        }));
    }

    for job in queue {
        let _ = job.join();
    }
}
```

---

### Encode and Decode JSON

**Python**

```python
import json

# Decode/Deserialize
data = '''{
    "name": "bugs",
    "age": 76
}'''

person = json.loads(data)

# Do things like with any other Python data structure
print(f"{person['name']} was born {person['age']} years ago")

# Encode/Serialize
serialized = json.dumps(obj)
print(f"The serialized value is: {serialized}")
```

**Rust**

```rust
extern crate serde;
extern crate serde_json;

#[macro_use]
extern crate serde_derive;

#[derive(Serialize, Deserialize)]
struct Person {
    name: String,
    age: u8,
}

fn main() {
    // Decode/Deserialize
    let data = r#"{"name": "bugs", "age": 76}"#;

    let p: Person = match serde_json::from_str(data) {
        Ok(person) => person,
        Err(e) => panic!("error: could not deserialize: {}", e),
    };

    // Do things just like with any other Rust data structure.
    println!("{} was born {} years ago.", p.name, p.age);

    // Encode/Serialize
    let serialized = serde_json::to_string(&p).unwrap();
    println!("The serialized value is: {}", serialized);
}

```

---

### Object Orientation

**Python**

[playground](https://repl.it/repls/SourPaltryHorseshoecrab)

```python
class Cat:
    def __init__(self, name):
        self.name = name

    def greet(self, other):
        print("Meow {}, I'm {}".format(other, self.name))

# ...

grumy = Cat('Grumpy')
grumy.greet('Garfield')  # Meow Garfield, I'm Grumpy
```

**Rust**

[playground](https://play.rust-lang.org/?gist=155c76fae5240e483858000e73e82f00&version=stable)

```rust
struct Cat {
    name: String
}

impl Cat {

    pub fn new<S>(name: S) -> Cat where S: Into<String> {
        Cat { name: name.into() }
    }
    
    pub fn greet<S: Into<String>>(&self, other:S) {
        println!("Meow {}, I'm {}", other.into(), self.name);
    }     
    
}

fn main() {
    let grumpy = Cat::new("Grumpy");
    grumpy.greet("Garfield");  // Meow Garfield, I'm Grumpy
}
```

> NOTE: In Rust, it is best to avoid `stringly types APIs` so in the above example it would be better if we do `let garfield = Cat::new("Garfield")` and then make `greet` to accept an instance of `Cat` as `other` argument. If you are interested [watch this](https://www.youtube.com/watch?v=0zOg8_B71gE).


---

### Print Object for Debug/Log 

Print formatted object debug information

**Python**

```python

class Actor:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __repr__(self):
      return str(self.__dict__)

daffy = Actor(
    name='Daffy',
    age=80,
)

print('{!r}'.format(daffy))  # {'name': 'Daffy', 'age': 80}
```

**Rust**

```rust
#[derive(Debug)]
struct Actor {
    name: String,
    age: i32
}

fn main() {
    let daffy = Actor {name: "Daffy".into(), age: 80};
    println!("{:#?}", daffy);   // Actor {name: "Daffy", age: 80 }
}

```

---


### Template for new examples

Explanation comes here.

**Python**

[playground](https://repl.it/repls/uniquelinkhere)

```python
# python code goes here
```

**Rust**

[playground](https://play.rust-lang.org/?gist=uniquehashhere&version=stable)

```rust
// rust code goes here
```