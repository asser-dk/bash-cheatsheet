(Yes, vim is not bash but I didn't feel like making an entirely new setup just for vim.)

# Search

Source: https://linuxize.com/post/vim-search

## Basic search

* `/foo` will search for the next word that *contains* `"foo"`
* `?foo` will search for the previous word that *contains* `"foo"`
* `/\<foo` will search for the next word that *starts with* `"foo"`
* Similarily `/foo\>` will search for the next word that *ends with* `"foo"`
* And you can combine it into `/\<foo\>` to search for *the exact word* `"foo"`
* Use `n` to go to the next result, and `N` to go to the previous result.

## Search for the current word

You can also search for the "current word" (meaning the word the cursor is currently "on") by pressing:

*  `*` to search forward
*  `#` to search backwards
*  Use `*` and `#` repeatedly to search for the next or previous occurrence of said word

## Search history

* Type `/` or `?` and use the up and down arrows to see the previous search history

## Case sensitivity

By default searches are case sensitive.

You can change the case sensitivity behaviour from either the vim command line or the `~/.vimrc` like so:

* `:set ignorecase`/`ic` to... ignore the casing
* `set: noignorecase`/`noic` to make it case sensitive again
* 
