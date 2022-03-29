# File operations

## Search/replace in (multiple) files

### Problem

Replace `Alice` with `Bob` in all files in directory `*`

```bash
sed -i 's/Alice/Bob/g' *
```

### Command explanation

* `sed` is the **S**tream **ED**itor command tool which can be used to manipulate file contents (among other things)
* `-i` is the option for *edit file in place*. Without this a new file is generated as the result of the command.
  * Giving the command a suffix, e.g. `-i_backup`, will make backup files in case you need to undo changes.
* `s/Alice/Bob/g` is the substitute command that replaces *all* instances of `Alice` with `Bob`
  * `s` is the *substitute* command
  * `/` is the separator between the different command fragments. You can use other special characters as separators if needed
  * `Alice` is the search term. This can also be a regex
  * `Bob` is the replacement. This can also be a regex
  * `g` is regex for `global`, meaning replace all instances. Omit for only replacing the first occurrence
* `*` is the file(s) to affect.
