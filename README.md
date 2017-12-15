# How do I find all files containing specific text on linux

```
grep -rnw '/path/to/somewhere/' -e 'pattern'
```

Along with these, `--exclude`, `--include`, `--exclude-dir` or `--include-dir` flags could be used for efficient searching:

 - This will only search through those files which have .c or .h extensions:

```
grep --include=\*.{c,h} -rnw '/path/to/somewhere/' -e "pattern"
```

 - This will exclude searching all the files ending with .o extension:

```
grep --exclude=*.o -rnw '/path/to/somewhere/' -e "pattern"
```


