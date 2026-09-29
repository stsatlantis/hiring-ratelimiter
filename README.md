# Rate Limiter – Hiring Exercise

## Task

Implement a rate limiter library.

A rate limiter controls how frequently an operation can be performed. Your implementation should expose a clean API that allows callers to check whether a given action is permitted under the configured rate limit, and to record that the action was taken.

## Requirements

- Thread safety is a plus.
- Write tests that demonstrate correctness.

## Deliverables

- A library (or binary with a library interface) in this repository, under the language sub-project you are working in.
- A brief explanation in the sub-project README (or this README) of your chosen algorithm and any design decisions.

## Sub-projects

### Rust

Located in [`rust/`](rust/). Uses the Rust standard library only.

```sh
cd rust
cargo build
cargo test
cargo clippy
cargo fmt
```

### Scala

Located in [`scala/`](scala/). Uses the Scala / Java standard library only.

```sh
cd scala
sbt compile
sbt test
sbt run
```

### Java

Located in [`java/`](java/). Uses the Java standard library only (JUnit 5 is provided for tests).

```sh
cd java
mvn compile
mvn test
mvn compile exec:exec
```

## Getting Started

```sh
claude
```
