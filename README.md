> **NOTICE:** This repository is looking for a new owner+maintainer as I want to dedicate my focus on maintaining [xplr](https://github.com/sayanarijit/xplr). Please [contact me](https://arijitbasu.in) in case you are interested.

# xplr.vim

This is a fork of [nnn.vim](https://github.com/mcchrish/nnn.vim) modified to work with
[xplr](https://github.com/sayanarijit/xplr).


### Examples

Git project root

```
command XplrProjectRoot :XplrPicker `git rev-parse --show-toplevel`

:XplrProjectRoot
```

Current file

```
:XplrPicker %:p
```

Current working directory

```
:XplrPicker
```

Root
```
:XplrPicker /
```
