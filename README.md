# vim-scilla

Basic syntax highlighting for [Scilla](https://scilla-lang.org/), a safe-by-design smart contract language. 

## Installation
### Pathogen
```
git clone https://github.com/edisonljh/vim-scilla.git ~/.vim/bundle/vim-scilla
```
### Vundle

Add the following line to your `~/.vimrc`:
```
Plugin 'edisonljh/vim-scilla'
```

## Syntax checker with ALE

If you are using [ALE](https://github.com/w0rp/ale), you can enable [scilla-checker](https://scilla.readthedocs.io/en/latest/scilla-checker.html) to show errors right inside vim.

Here is how to enable it:

1. Install [ALE](https://github.com/w0rp/ale) vim plugin
2. Make `scilla-checker` executable available (https://github.com/Zilliqa/scilla#compiling-and-running)
3. Set STDLIB dir in vimrc: `let g:ale_scilla_checker_libdir = '<path>/stdlib'`
4. Set CHECKER in vimrc: ` let g:ale_scilla_checker_executable='<path>/scilla-checker'`
5. Enable the linter in vimrc: `autocmd FileType scilla let b:ale_linters = ['checker']`
6. Open any scilla file and ensure checker is working: `:ALEInfo`

## Commenting

Comment functionality is available through [NERDCommenter](https://github.com/scrooloose/nerdcommenter). It's not natively supported on this plugin yet. PRs are welcome!

## License

See [LICENSE](./LICENSE)
