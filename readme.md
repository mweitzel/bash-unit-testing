functions/templates/etc for unit testing bash

in your scripts, run main with

    test $SOURCE_FOR_UNIT_TESTING || main "$@"
```

you can escape the main function by setting `SOURCE_FOR_UNIT_TESTING=1` before sourcing

as shown in the `test-template`, to assert against a successful exit code (0), use

`function_you_expect_to_pass && pass || fail`

and to assert against a failing exit code, use

`function_you_expect_to_fail && fail || pass`

To test streams, write a function and assert against *their* exit codes


license: MIT
