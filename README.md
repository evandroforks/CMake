# Sublime Text 2/3 - CMake Package #

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/zyxar/Sublime-CMakeLists?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

* Simple auto-indentation support.
* Syntax highlighting for CMakeLists.txt files and `*.cmake` files, based on
  [CMake 3.0][1].
* Syntax highlighting for CMakeCache.txt files.
* Syntax highlighting for `.h.in` and `.hpp.in` files.
* Basic snippets.
* Basic keybindings.


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Now,
   Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   input the following address and press <kbd>Enter</kbd>
   ```
   https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
   ```
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   find the following setting on your **`Package Control.sublime-settings`** file:
   ```js
       "channels":
       [
           "https://packagecontrol.io/channel_v3.json",
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
       ],
   ```
1. And,
   change it to the following, i.e.,
   put the **`https://raw.githubusercontent...`** line as first:
   ```js
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
   ```
   * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
     you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`CMake`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


## Available Snippets

* `cmake_minimum_required`
* `foreach`
* `if`
* `option`
* `project`
* `set`
* `while`

If an argument to a command is optional, it is selectable when you tab through
the snippet, and you can then press backspace to remove the optional argument.

## Available Key Bindings

* Select a word, and press <kbd>$</kbd> to wrap the selection
  as a [variable substitution][3]. The newly inserted text will stay selected,
  so that you can press the double-quotes character <kbd>"</kbd> to enclose the
  selection in double-qoutes too. Press tab to get out of the selection if you
  don't want double-quotes.
* Select a word, and press <kbd>ctrl</kbd><kbd>shift</kbd><kbd>,</kbd> to wrap
  the selection as a [generator expression][2] with an argument.
* Select a word, and press <kbd>ctrl</kbd><kbd>shift</kbd><kbd>.</kbd> to wrap
  the selection as a [generator expression][2] without an argument.

[1]: https://cmake.org/cmake/help/v3.0/manual/cmake-language.7.html
[2]: https://cmake.org/cmake/help/v3.0/manual/cmake-generator-expressions.7.html
[3]: https://cmake.org/cmake/help/v3.0/manual/cmake-language.7.html#variable-references
