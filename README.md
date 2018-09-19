# What is this?

On MacOS, we always need load environment variables in Emacs
to make ```shell-command``` etc tools can works as expected.
[exec-path-from-shell](https://github.com/purcell/exec-path-from-shell) is wonderful extension to do that.

But command ```exec-path-from-shell-initialize``` is very slow
and perhaps many libraries need call ```exec-path-from-shell-initialize``` itself.

So, cache-path-from-shell use cache mechanism make sure
```exec-path-from-shell-initialize``` just execute once and
no matter how many times you call it.

### Installation:
Install [exec-path-from-shell](https://github.com/purcell/exec-path-from-shell) first.

Then put cache-path-from-shell.el to your load-path.
The load-path is usually ~/elisp/.
It's set in your ~/.emacs like this:

```Elisp
(add-to-list 'load-path (expand-file-name "~/elisp"))
(require 'cache-path-from-shell)
```

Then feel free to call `exec-path-from-shell-initialize' at anyplace. ;)
