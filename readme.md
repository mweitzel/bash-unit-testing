#### bash testings, no library, no framework
##### functions/templates/etc for unit testing bash

in your bash scripts, run main with

```
test $SOURCE_FOR_UNIT_TESTING || main "$@"
```

to escape the main function you can set `SOURCE_FOR_UNIT_TESTING=1` in your tests before sourcing

as shown in the `test-template`, to assert against a successful exit code (0), use

`function_you_expect_to_pass ; assert`

and to assert against a failing exit code, use

`function_you_expect_to_fail ; refute`

To test streams, write a function and assert against *their* exit codes


### license

MIT
