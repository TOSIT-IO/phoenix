# TDP Phoenix Notes

The version 5.2.1-0.0 of Apache Phoenix is based on the branch `5.2.1` tag of the Apache [repository](https://github.com/apache/phoenix/releases/tag/5.2.1).

## Making a release

```
mvn clean install -DskipTests
```

This command generates `phoenix-hbase-2.5-5.2.1-0.0-bin.tar.gz` file in the `phoenix-assembly/target` directory.

## To run tests

### Unit tests
```
mvn test -DPhoenixPatchProcess -Dskip.code-coverage
```

- -DPhoenixPatchProcess, disables the build of the shaded artifacts (not necessary for tests)
- -Dskip.code-coverage, self explanatory

### Integration tests

```
mvn verify -DPhoenixPatchProcess -Dskip.code-coverage
```

- -DPhoenixPatchProcess, disables the build of the shaded artifacts (not necessary for tests)
- -Dskip.code-coverage, self explanatory

### Integration tests

```
mvn verify -DPhoenixPatchProcess -Dskip.code-coverage
```

- -DPhoenixPatchProcess, disables the build of the shaded artifacts (not necessary for tests)
- -Dskip.code-coverage, self explanatory
