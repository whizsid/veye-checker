# Veye-Checker

Simple command-line util to scan Nupkg and Jar files and translate them into SHA code, 
which in return can be used to fetch package information from VersionEye API.


## Usage

* **scan** - scans the target folder recursively and digest supported packagefiles into SHA

```bash

veye-checker scan ../temp/ 
veye-checker scan ../temp/ -o results.csv
```

* **lookup** - fetches product details from VersionEye api for generated SHA hash

```bash

veye-checker lookup <SHA_STRING> -a <YOUR_API_CODE>
```


## Build

```bash
> cargo build
> ./target/debug/veye-checker

or simpler command
> cargo run

or optimized production release
> cargo build --release
> ./target/release/veye-checker
```