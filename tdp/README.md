# TDP Phoenix Notes

The version 5.1.3-1.0 of Apache Phoenix is based on the branch `5.1` tag of the Apache [repository](https://github.com/apache/phoenix/tree/5.1).

## Making a release

```
mvn clean install -DskipTests -Dhbase.profile=2.1
```

This command generates `phoenix-hbase-2.1-5.1.3-1.0-bin.tar.gz` file in the `phoenix-assembly/target` directory.

## To run tests

### Unit tests
```
mvn test -Dhbase.profile=2.1 -DPhoenixPatchProcess -Dskip.code-coverage
```

- -Dhbase.profile=2.1, builds phoenix with hbase 2.1.10-1.0 and hadoop 3.1.1-0.0
- -DPhoenixPatchProcess, disables the build of the shaded artifacts (not necessary for tests)
- -Dskip.code-coverage, self explanatory

### Integration tests

```
mvn verify -Dhbase.profile=2.1 -DPhoenixPatchProcess -Dskip.code-coverage
```

- -Dhbase.profile=2.1, builds phoenix with hbase 2.1.10-1.0 and hadoop 3.1.1-0.0
- -DPhoenixPatchProcess, disables the build of the shaded artifacts (not necessary for tests)
- -Dskip.code-coverage, self explanatory
