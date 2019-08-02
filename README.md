# VIM Techniques

1. [Mark a Position and Jump Back](#mark-a-position-and-jump-back)

## Mark a Position and Jump Back
* Mark a position: `m{a-zA-Z}`
  * {a-z}: set a local mark, allows to only jump within a file
  * {A-Z}: set a global mark, allows to jump across files
* Jump back to a previously marked position: 
  * Jump to the row of mark: `'{mark}`
  * Jump to the row and column of a mark using backtick: `` `{mark}``
* Other useful mark commands

| Command        | Description           |
| ------------- |-------------|
| `d'a`      | delete from current line to line of mark `a` |
| `d`a`      | delete from current cursor position to position of mark `a`      |
| `y`a`      | yank text to unnamed buffer from cursor to position of mark `a`   |
|`:marks`    |	list all the current marks |
|`:marks aB` |	list marks `a`, `B`|

* Special Marks set automatically in Vim (N.B. backtick, `` ` ``, in the table can be safely replaced with `'`)

|Command	|Description
|---|---|
|`` `.``	|jump to position where last change occurred in current buffer|
|`` `"``	|jump to position where last exited current buffer|
|`` `0``	|jump to position in last file edited (when exited Vim)|
|`` `1``	|like `` `0`` but the previous file (also `` `2`` etc)|
|`''`	|jump back (to line in current buffer where jumped from)|
|`` ` ``	|jump back (to position in current buffer where jumped from)|
|`` `[`` or `` `]``	|jump to beginning/end of previously changed or yanked text|
|`` `<`` or `` `>``	|jump to beginning/end of last visual selection|
