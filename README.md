# commenter
A simple application because I got curious about the speed differences between Rust and Golang.

## To run the Rust side:
Should just be able to `cd rust; cargo r --release`. You'll find it on `localhost:3001`.

## To run the Go side:
 - Install `soda`.
 - cd to `golang`.
 - Set up the database using `soda g config -t sqlite3`.
 - `./go_run.sh` (or `go run -tags sqlite .`).

## Test parameters:
The tests in `oha_results.txt` were done with Rust in release mode and `go run`,
on an Intel Core i7-10750H 6-core, 12-thread laptop processor, running at 5 GHz,
on Arch Linux x86_64 - Sat 21 May 2022.

Rust was about three times faster (23 kreqs/sec vs 60 kreqs/sec). (And the language is better. But I'm biased. Bleh.)

Also thanks [Hannah](https://twitter.com/ravenslofty) for making me realise I put Rust in debug mode, skewing the results in the original commit.