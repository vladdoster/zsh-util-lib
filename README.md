<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [zsh-util-lib](#zsh-util-lib)
  - [List Of The Functions](#list-of-the-functions)
    - [@util-bind-all](#util-bind-all)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# zsh-util-lib

An utility-library for Zshell that provides a few general-purpose functions.
It's a counterpart to the
[zsh-string-lib](https://github.com/zdharma/zsh-string-lib) library.

## List Of The Functions

### @util-bind-all

Rebinds all key bindings so that they're executing some custom code. It's an
alternative to overloading of all Zle widgets. It's twice as fast method.

Arguments:

1. The custom snippet of code to run before executing the original widget.
2. A bool (`1`,`yes`,`true` for truth or other value for false) indicating
   whether the widget calls should be automatically forwarded to their original
   (before-binding) versions.
3. An optional custom snippet of code to be executed **after** executing the
   original widget.

Example:

```zsh
@util-bind-all 'print hello!' yes 'print hello after!'
```

<!-- vim:set ft=markdown tw=80 fo+=an1 autoindent: -->
