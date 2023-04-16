# py2rs

## From Python into Rust 

```rust
let x = Rust::from("Python");
```

A quick reference guide for the **Pythonista** in process of becoming a **Rustacean**. Basically, Rust for Python programmer/developer. 


![image_2017-11-28_08-03-59](https://user-images.githubusercontent.com/458654/33350327-50e76baa-d485-11e7-8a6e-b3dd0c337046.png)

### Monty Python - Season 3 - Episode 49

[The sketch](http://montypython.50webs.com/scripts/Series_3/49.htm)

```
Mrs. Jalin: George.
Mr. Jalin: Yes, Gladys.
Mrs. Jalin: There's a man at the door with a moustache.
Mr. Jalin: Tell him I've already got one. (Mrs. Jalin hits him hard with a newspaper) 
          All right, all right. What's he want then?
Mrs. Jalin: He says do we want a documentary on crustaceans.
Mr. Jalin: Crustaceans!
Mrs. Jalin: Yes.
Mr. Jalin: What's he mean, crustaceans?
Mrs. Jalin: CRUSTACEANS!! GASTROPODS! LAMELLIBRANCHS! CEPHALOPODS!
...
```

Ok... [watch it later...](https://web.archive.org/web/20140806053203/https://www.youtube.com/watch?v=8R2zvE615dM) let's learn some Rust now...

## TOC

- [Getting Started with Rust](#getting-started-with-rust)
- [Where to exercise](#exercises)
- [Where to be informed on news and updates](#getting-updated)
- [Interacting with Rustacean Communities](#interact-with-other-rustaceans)
- [Additional learning Resources](#additional-learning-resources)
- [Curious Facts](#facts)
- [Glossary of terms](#glossary-of-terms)
- [General fact comparison](#general)
- [Environment Tools](#environment-tools)
- [Libraries and Frameworks](#libraries-and-frameworks)
- [Applications](#applications)
- [Useful Crates](#useful-crates)
- [Code Comparison](CODE_COMPARISON.md)
- [Acknowledgement](ACKNOWLEDGEMENT.md)

## Getting Started with Rust

Assuming you already know what is [**Rust**](http://rust-lang.org) and already 
decided to start learning it. Here are some steps for you to follow:

1) Take a tour of **Rust Syntax** and **Coding Style**  
   https://learnxinyminutes.com/docs/rust/
2) Watch some **screencasts** to get basics of **Ownership &Borrowing** concept  
   http://intorust.com/
3) Follow this set of runnable examples to understand how everything fit together  
   https://doc.rust-lang.org/stable/rust-by-example/
4) Now it is time to read your first book, you can pick:  
    * **Rust Essentials**  
      > A good introduction to Rust language in a more `superficial` approach which results
      > in a very pleasant and easy reading, recommended even for those who are not experienced
      > with low level systems languages.  
        * Paparback and e-book available on Packt Publisher  
          https://www.packtpub.com/application-development/rust-essentials-second-edition

    * **TRPL** (The Rust Programming language Book)   
      > A complete Guide to Rust Language  
      > https://doc.rust-lang.org/book/   
        * Official Book  
        * Free to read online  
        * Available as paperback or e-book (buy at Amazon)
5) Read some real examples
    * **Rust Cookbook**  
     https://rust-lang-nursery.github.io/rust-cookbook/
     This Rust Cookbook is a collection of simple examples that demonstrate good 
     practices to accomplish common programming tasks, using the crates of the Rust ecosystem.
    * **Anthology**  
    https://github.com/brson/rust-anthology/blob/master/master-list.md 
6) Patterns and Good Practices  
   * **Rust Patterns** https://github.com/rust-unofficial/patterns
   * **API Guidelines** https://rust-lang-nursery.github.io/api-guidelines/

## Exercises

Time to put your new knowledge in action solving some exercises.

1) **Exercism.io**  
   Register a new account on exercism.io (using github auth)  
   Install exercism command line client on your computer  
   Solve some exercises:  https://www.exercism.io/languages/rust/

2) **Rust Playground**  
   Run Live Rust Code in the browser with https://play.rust-lang.org/

3) **rustlings**  
   Interactive rust exercises: https://github.com/rust-lang/rustlings 

## Getting updated

Now I assume you are addicted to **Rust** and you want to be updated about everything 
around it, here are some good links to follow.

1) This Week in Rust Newsletter  
   https://this-week-in-rust.org/   
   https://twitter.com/thisweekinrust 
2) Awesome Rust Newsletter  
   https://rust.libhunt.com/
3) Reddit  
   http://reddit.com/r/rust   (serious sub-reddit)  
   http://reddit.com/r/rustjerk (almost memes only)  
4) Official Twitter  
  https://twitter.com/rustlang

## Interact with other Rustaceans

> Don't be afraid, the Rustaceans are a very receptive species and are cozy with the Pythonistas.

### Main Community links

https://www.rust-lang.org/en-US/community.html

### Local Communities

- Brazil
    * General
        * Youtube :  http://bit.ly/canalrustbr
        * Telegram: https://t.me/rustlangbr
    * Rust BH
        * https://t.me/rustbh
    * Rust in POA
        * https://t.me/rustinpoa
        * https://www.meetup.com/Rust-in-POA/
- Indonesia
    * General
        * FB Groups (Rustaceans Indonesia) : https://fb.com/groups/RustaceansID
        * FB Groups (Rust ID)              : https://fb.com/groups/rustindo
        * Telegram (Rust Indonesia)        : https://t.me/rustindonesia
- Russia
    * General
        * FB Groups (RustyCrate)           : https://facebook.com/rustycrate/
        * Telegram (pro Rust)              : https://t.me/proRust
        
- Add your country/city here, send a Pull Request.

## Additional learning resources

- Learning Rust https://learning-rust.github.io/
- Rust Learning https://github.com/ctjhoa/rust-learning
- Rust Guidelines (WIP) https://aturon.github.io/
- Rust Design Patterns and Idioms https://github.com/rust-unofficial/patterns/
- Idiomatic Rust https://github.com/mre/idiomatic-rust
- GTK Rust Tutorial https://mmstick.github.io/gtkrs-tutorials/
- Effective use of iterators http://hermanradtke.com/2015/06/22/effectively-using-iterators-in-rust.html
- Red Hat Developers: Speed up Your Python with Rust https://developers.redhat.com/blog/2017/11/16/speed-python-using-rust/
- What's a reference in Rust? (The best article to understand `'lifetimes` and `&`) https://jvns.ca/blog/2017/11/27/rust-ref/

## Facts

- The language is named **Rust** because **"rust is as close to the bare metal as you can get".**,   
  in metal theory **rust** is the chemical layer closest to bare metal.  
  (also [Wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language)) says that the name was *possibly* inspired by the name of a Fungi)
- The Rust `trifecta` is 1) **Memory Safe**, 2) **Fast** 3) **Concurrent**
- Rust can be used for web development http://www.arewewebyet.org/
- Rust can be used for Gaming Development http://arewegameyet.com/
- Rust can be used for Machine Learning http://www.arewelearningyet.com/ 
- Lots of IDEs and Editors supports Rust https://areweideyet.com/  
  (VSCode is known to have the better support by now https://marketplace.visualstudio.com/items?itemName=kalitaalexey.vscode-rust)
- Rust packages are called `Crates` and are installed by `Cargo` explore them at http://crates.io
- In Rust there is no **Class** but **Structs**, **Enums**, **Traits**, **functions** and **macros!**
- Rust compiler was first written in **OCaml** then rewritten in Rust! (Rust is written in Rust!!!)
- Rust type system is strongly inspired by **Haskell**
- Rust **functional** style is inspired by **Erlang**
- Rust type inference is mainly inspired by **ML** and also by **Haskell**
- The main **syntax** style is inspired by **C** and **C++**
- There is no automated **Garbage Collector** so Rust frees memory based on Resource Aquisition RAII (a.k.a Ownership)
- Rust has **Generic Types**!!!
- As **Rust** is **close to bare metal** you can ship a program without the inclusion of **Rust's runtime** which makes easy to distribute programs (no need of dependencies and virtuelenvs management)
- There are **Python** code in Rust! Rust build is [bootstrapped by Python](https://github.com/rust-lang/rust/blob/master/src/bootstrap/bootstrap.py)
- Graydon Hoare (creator of Rust) is now working at **Apple** developing the **Swift** language
- Rust is the developers **most loved language** according to **Stack Overflow Survey**
- Rust is the most [**energy efficient**](https://sites.google.com/view/energy-efficiency-languages/results) language! and that is very important for environment, data center companies and maybe it can help saving your laptop and phone battery in near future. 
- There is an Operating System written in **Rust** - https://www.redox-os.org/
- Mozilla released the fastest version of Firefox (**quantum**) having many parts written on **Rust**
- The Rust mascot (unofficial) is called **Ferris** and it is a **crab** http://www.rustacean.net/  
  (There is no record of the official reason about being a crab, the reasonable history is that it was inspired by the **Rusty Crab** 
   a common species of crab and also a name of a famous restaurant.)
- To compliment your fellow Rustaceans don't say **~~cheers!~~**. Say **safe!** (**safe!** is also said when toasting with champagne at Rust conferences)
- Rust is to become a second programming language for the Linux kernel (see [here](https://en.wikipedia.org/wiki/Rust_for_Linux))

> **More facts? and curiosities** send a question here or send a Pull Request adding an interest fact to this list.

![ferris](http://www.rustacean.net/more-crabby-things/animated-ferris.gif)

## Glossary of terms

| Term      | Definition                                        |
| --------- | ------------------------------------------------- |
| crate     | A rust distributable **package**                  |
| ferris    | The unofficial Crab Mascot                        |
| Rustacean | The Rust programmer or evangelist or enthusiastic |
| nightly   | The unstable toolchain of the Rust compiler       |
| impl      | Implementation                                    |


## General
| Python                                                                       | Definition                         | Rust                                                                      |
| ---------------------------------------------------------------------------- | ---------------------------------- | ------------------------------------------------------------------------- |
| [PEP8](https://www.python.org/dev/peps/pep-0008/)                            | Guidelines and conventions         | [RustAPI Guidelines](https://rust-lang-nursery.github.io/api-guidelines/) |
| [PEPS](https://www.python.org/dev/peps/)                                     | Enhancement Proposals / RFC        | [Rust RFCs](https://github.com/rust-lang/rfcs)                            |
| [PSF](https://www.python.org/psf/)                                           | Organization / Foundation          | [Mozilla Research](https://research.mozilla.org/)                         |
| [PyCon](https://www.pycon.org/)                                              | Main Conference                    | [RustConf](http://rustconf.com/)                                          |
| [Guido Van Rossum](https://twitter.com/gvanrossum)                           | Creator                            | [Graydon Hoare](https://twitter.com/graydon_pub)                          |
| 1989                                                                         | First appeared                     | 2010                                                                      |
| 1991                                                                         | First Release                      | 2012                                                                      |
| [PSF](https://docs.python.org/3/license.html)                                | License                            | Apache 2.0 and MIT                                                        |
| C                                                                            | Implemented in                     | Rust                                                                      |
| .py, .pyw, .pyc                                                              | File Extensions                    | .rs, .rlib                                                                |
| http://github.com/python/cpython                                             | Repository                         | https://github.com/rust-lang/rust                                         |
| [Pyladies](), [AfroPython]()                                                 | Diversity and Inclusion initiative | [RustBridge](https://rustbridge.github.io/)                               |
| [comp.lang.Python](https://groups.google.com/forum/#!forum/comp.lang.python) | Official Users Forum               | [users.rust-lang.org](https://users.rust-lang.org)                        |


## Environment Tools

| Python                                                                                                | Definition                              | Rust                                                                                      |
| ----------------------------------------------------------------------------------------------------- | --------------------------------------- | ----------------------------------------------------------------------------------------- |
| `requirements.txt`                                                                                    | Official dependency tracker file        | `Cargo.toml`                                                                              |
| `setup.py`                                                                                            | Official installator / distributor file | `Cargo.toml`                                                                              |
| [PyPI](https://pypi.org/)                                                                             | Library repository                      | [Crates.io](http://crates.io)                                                             |
| [pip](https://pypi.python.org/pypi/pip)                                                               | Library installation                    | [Cargo](http://doc.crates.io/)                                                            |
| [setuptools](https://pypi.python.org/pypi/setuptools) and [poetry](https://python-poetry.org/)        | Library distribution                    | [Cargo](http://doc.crates.io/)                                                            |
| [pbr](https://docs.openstack.org/pbr/latest/)                                                         | Library distribution                    | [Cargo](http://doc.crates.io/)                                                            |
| [pipenv](https://pypi.python.org/pypi/pipenv) and [poetry](https://python-poetry.org/)                | Dependency manager                      | [Cargo](http://doc.crates.io/)                                                            |
| [twine](https://pypi.python.org/pypi/twine)                                                           | Package uploader                        | [Cargo](http://doc.crates.io/) and [Semantic](https://github.com/semantic-rs/semantic-rs) |
| `venv` *                                                                                              | Isolated environments                   | [Cargo](http://doc.crates.io/)                                                            |
| [pyinstaller](https://github.com/pyinstaller/pyinstaller)                                             | Generate standalone executables         | [Cargo](http://doc.crates.io/)                                                            |
| [pyenv](https://github.com/pyenv/pyenv-installer)                                                     | Install and manage versions of language | [rustup](https://www.rustup.rs/)                                                          |
| [pydoc](https://docs.python.org/library/pydoc.html) and [sphinx](https://pypi.python.org/pypi/sphinx) | Generate documentation from code        | [rustdoc](https://doc.rust-lang.org/stable/rustdoc/) and [Cargo](http://doc.crates.io/)   |
| [python](http://python.org)                                                                           | Interpreter / Compiler                  | [rustc](https://doc.rust-lang.org/1.1.0/rustc/) and [Cargo](http://doc.crates.io/)        |
| [ipython](https://pypi.python.org/pypi/ipython)                                                       | REPL                                    | [rusti](https://github.com/murarth/rusti)                                                 |
| [ipdb](https://pypi.python.org/pypi/ipdb)                                                             | Debugger                                | [rust-gdb](https://github.com/rust-lang/rust/blob/master/src/etc/rust-gdb)                |
| [Extending Python with C or C++](https://docs.python.org/3/extending/extending.html)                  | Foreign language interface              | [PyO3](https://pyo3.rs/v0.17.2/)

## Libraries and Frameworks

| Python                                                                                            | Definition                       | Rust                                                                                                              |
| ------------------------------------------------------------------------------------------------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `urllib` *                                                                                        | HTTP calls                       | [hyper](https://crates.io/crates/hyper)                                                                           |
| [requests](https://pypi.python.org/pypi/requests)                                                 | Simplified HTTP calls            | [reqwest](https://github.com/seanmonstar/reqwest)                                                                 |
| [json](https://pypi.python.org/pypi/json)                                                         | JSON parsing loading and dumping | [serde](https://github.com/serde-rs/serde)                                                                        |
| [pyYAML](https://pypi.python.org/pypi/pyyaml)                                                     | YAML parsing loading and dumping | [serde](https://github.com/serde-rs/serde)                                                                        |
| [lxml](https://pypi.python.org/pypi/lxml)                                                         | XML parsing loading and dumping  | [RustyXML](https://github.com/Florob/RustyXML)                                                                    |
| `csv` *                                                                                           | CSV parsing                      | [rust-csv](https://github.com/BurntSushi/rust-csv)                                                                |
| `datetime` *  & [Dateutils](https://pypi.python.org/pypi/dateutils)                               | Date & time                      | [Chrono](https://github.com/chronotope/chrono)                                                                    |
| [click](https://pypi.python.org/pypi/click) and [argparse](https://pypi.python.org/pypi/argparse) | CLI Framework                    | [clap](https://github.com/kbknapp/clap-rs)                                                                        |
| [docopt](https://pypi.python.org/pypi/docopt)                                                     | CLI Framework                    | [docopt](https://github.com/docopt/docopt.rs)                                                                     |
| `re` *                                                                                            | Regular Expressions              | [regex](https://github.com/rust-lang/regex)                                                                       |
| `subprocess` *                                                                                    | Run external commands            | [subprocess](https://crates.io/crates/subprocess)                                                                 |
| `multiprocessing` *                                                                               | Multiprocessing            | [Rayon](https://crates.io/crates/rayon)                                                                           |
| `logging` *                                                                                       | Logging                          | [log](https://github.com/rust-lang-nursery/log)                                                                   |
| `Pathlib` *                                                                                       | Path manipulation                | [fs](https://doc.rust-lang.org/std/fs/) and [fs_extra](https://github.com/webdesus/fs_extra)                      |
| [cryptography](https://pypi.python.org/pypi/cryptography)                                         | Crytography                      | [crypto](https://github.com/DaGenix/rust-crypto)                                                                  |
| `pickle` *                                                                                        | Object serialization             | [RON](https://github.com/ron-rs/ron)                                                                              |
| `heapq` *                                                                                         | Heap queue                       | `BinaryHeap` *                                                                                                    |
| [bottle](https://pypi.python.org/pypi/bottle)                                                     | Minimal web framework            | [Iron](https://github.com/iron/iron)                                                                              |
| [flask](https://pypi.python.org/pypi/flask)                                                       | Web framework                    | [Rocket](https://github.com/SergioBenitez/Rocket)                                                                 |
| [django](https://pypi.python.org/pypi/django)                                                     | Full stack web framework         | **DO NOT EXIST YET**                                                                                              |
| [SQL Alchemy](https://pypi.python.org/pypi/sqlalchemy)                                            | Relational database ORM          | [Diesel](https://github.com/diesel-rs/diesel)                                                                     |
| [Pymongo](https://pypi.python.org/pypi/pymongo)                                                   | MongoDB driver                   | [mongodb](https://crates.io/keywords/mongodb)                                                                     |
| [Jinja 2](https://pypi.python.org/pypi/jinja2)                                                    | Template engine                  | [Tera](https://github.com/Keats/tera)                                                                             |
| [pygtk](http://www.pygtk.org/)                                                                    | GTk desktop development          | [gtk](https://github.com/gtk-rs/gtk)                                                                              |
| [pyside](http://www.pyside.org/)                                                                  | QT desktop development           | [rust-qt](https://github.com/rust-qt)                                                                             |
| [pygame](https://pypi.python.org/pypi/pygame)                                                     | 2D UI library / gaming           | [ggez](http://ggez.rs/) & [Conrod](https://github.com/PistonDevelopers/conrod/) & [Piston](http://www.piston.rs/) |
| [unitest2](https://pypi.python.org/pypi/unittest2)                                                | Test framework                   | [Builtin]()                                                                                                       |
| [nose](https://pypi.python.org/pypi/nose)                                                         | Test runner                      | [Cargo](http://doc.crates.io/)                                                                                    |
| [pytest](https://pypi.python.org/pypi/pytest)                                                     | Testing framework and runner     | [Polish](https://github.com/AlKass/polish)                                                                        |
| [Flake8](https://pypi.python.org/pypi/flake8)                                                     | Linter                           | [Clippy](https://github.com/rust-lang-nursery/rust-clippy)                                                        |
| [autopep8](https://pypi.python.org/pypi/autopep8) and [black](https://pypi.org/project/black/)    | Auto formatter                   | [rustfmt]()                                                                                                       |
| [twisted](https://pypi.python.org/pypi/twisted)                                                   | Network application framework    | [libpnet](https://github.com/libpnet/libpnet)                                                                     |
| `AsyncIO` *                                                                                       | Async application framework      | [Tokio](https://github.com/tokio-rs/tokio) and [futures](https://github.com/alexcrichton/futures-rs)              |
| [Pillow](https://pypi.python.org/pypi/pillow)                                                     | Image manipulation               | [Image](https://github.com/PistonDevelopers/image)                                                                |
| [Beautiful Soup](https://pypi.python.org/pypi/beautifulsoup4)                                     | HTML parser                      | [html5ever](https://github.com/servo/html5ever)                                                                   |
| [Hypothesis](http://hypothesis.works/)                                                            | Data driven test framework       | [Quickcheck](https://github.com/BurntSushi/quickcheck) and [proptest](https://github.com/altsysrq/proptest)       |
| [mock](https://pypi.python.org/pypi/mock)                                                         | Test mocking                     | [Mockers](https://crates.io/crates/mockers)                                                                       |
| [bioPython](https://pypi.python.org/pypi/biopython)                                               | Bioinformathics libraries        | [Rust Bio](https://github.com/rust-bio)                                                                           |
| [Dynaconf](http://github.com/rochacbruno/dynaconf)                                                | Config management                | [Config](https://github.com/mehcode/config-rs)                                                                    |
| `itertools` *                                                                                     | Data structure iteration         | [Rust Itertools](https://github.com/bluss/rust-itertools)                                                         |
| [Geopython](https://pypi.python.org/pypi/geopython)                                               | Geo spatial data                 | [Geo Rust](https://github.com/georust)                                                                            |
| [ScikitLearn](https://pypi.python.org/pypi/scikit_learn)                                          | Machine learning                 | [rusty-machine](https://github.com/AtheMathmo/rusty-machine)                                                      |
| [mistune](https://pypi.python.org/pypi/mistune)                                                   | Markdown / Common Mark Parser    | [cmark](https://github.com/google/pulldown-cmark)                                                                 |
| [celery](https://pypi.python.org/pypi/celery)                                                     | Distributed computation          | [Antimony](https://github.com/antimonyproject/antimony)                                                           |
| [boto](https://pypi.python.org/pypi/boto)                                                         | AWS clients                      | [rusoto](https://github.com/rusoto/rusoto)                                                                        |
| [AstroPy](https://pypi.python.org/pypi/astropy)                                                   | Astronomy                        | [astro-rust](https://github.com/saurvs/astro-rust)                                                                |
| [Numpy](https://pypi.python.org/pypi/numpy)                                                       | Numeric                          | [ndarray](https://crates.io/crates/ndarray)                                                                       |
| [Pandas](https://pypi.org/project/pandas/)                                                        | Dataframes                       | [Polars](https://www.pola.rs/)                                                                                    | 

## Applications

| Python                                          | Definition                                       | Rust                                                   |
| ----------------------------------------------- | ------------------------------------------------ | ------------------------------------------------------ |
| [Pelican](https://pypi.python.org/pypi/pelican) | Static Site generator                            | [Cobalt](https://github.com/cobalt-org/cobalt.rs)      |
| [ansible](https://pypi.python.org/pypi/ansible) | Infra Orchestration                              | [realize](https://crates.io/crates/realize)            |
| [mkdocs](https://pypi.python.org/pypi/mkdocs)   | Generate documentation and e-books from Markdown | [mdBook](https://crates.io/crates/mdbook)              |
| [locust](https://pypi.python.org/pypi/locust)   | HTTP load test                                   | [drill](https://github.com/fcsonline/drill)            |
| [Nameko](https://pypi.python.org/pypi/nameko)   | Microservices Framework                          | [fractalide](https://github.com/fractalide/fractalide) |
| [Quokka CMS](http://quokkaproject.org)          | CMS                                              | [Nickel CMS](https://github.com/irony-rust/nickel-cms) |



## Useful crates

Add Pythonic features to Rust

| Python                            | Definition                                         | Rust                                             |
| --------------------------------- | -------------------------------------------------- | ------------------------------------------------ |
| `{'foo': "bar"}`                  | Syntax to create a dict / hashmap                  | [maplit](https://crates.io/crates/maplit)        |
| `__init__(self, value='default')` | Instance initialization (with some default values) | [derive_new](https://github.com/nrc/derive-new)  |
| itertools `*stdlib`               | Extra iterators methods                            | [itertools](https://crates.io/crates/itertools)  |
| `hashlib` *                       | Password Hashing                                   | [libpasta](https://github.com/libpasta/libpasta) |

