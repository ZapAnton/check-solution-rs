### Usage

```shell
$ check_solution_rs <solution_uuid>
```

### Check steps

The script will perform the following operations, given the solution uuid:

- Download the solution to the local machine.
- Remove the `#[ignore]` lines from the test suite file.
- Run the tests via `cargo test`. If failing tests are present, print the test results.
- Run `cargo clippy`. If `clippy` produces warnings, print them.
- Run `rustfmt --check`. If the solution files where not formatted, print the warning.
- Try to analyze the solution. Print any general warnings or warnings, related to the mentor notes.
