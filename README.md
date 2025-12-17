> [!NOTE]
> This is a fork of `platformio-mode` from MELPA, mostly focused on merging some
> unattended PRs and adding a few bits of functionality I find useful for myself.

# 👽 `platformio-mode`
<!-- [![MELPA](https://melpa.org/packages/platformio-mode-badge.svg)](https://melpa.org/#/platformio-mode) -->
<!-- [![MELPA Stable](https://stable.melpa.org/packages/platformio-mode-badge.svg)](https://stable.melpa.org/#/platformio-mode) -->


`platformio-mode` is an Emacs minor mode which allows quick building and
uploading of PlatformIO projects with a few short key sequences.

Code completion can be provided either by installing a .ccls‑compatible package
such as ccls, or via LSP (`eglot` or `lsp‑mode`) using a language server like
clangd or ccls. To keep the index up to date run
`platformio-init-update-workspace` after installing libraries; if you use clangd
you can generate the required compilation database with
`platformio-generate-compiledb`.


## Dependencies

No extra dependencies, besides Emacs 25.1 or later.


## Keymap

The default keymap prefix is `C-c i`.

The following keybindings are currently available.

| Function                | Keymap    |
| --------                | :-------: |
| Build                   | `C-c i b` |
| Upload                  | `C-c i u` |
| Upload using Programmer | `C-c i p` |
| Upload SPIFFS           | `C-c i s` |
| Monitor device          | `C-c i m` |
| Clean                   | `C-c i c` |
| Update                  | `C-c i d` |
| Update Workspace        | `C-c i i` |
| Generate compilation db | `C-c i g` |
| Boards List             | `C-c i l` |


## Installation

### elpaca

```elisp
(use-package platformio-mode
    :ensure (:host github :repo "fabcontigiani/platformio-mode")
    :commands (platformio-mode))
```

### package.el

```elisp
(use-package platformio-mode
    :vc (:url "https://github.com/fabcontigiani/platformio-mode.git")
    :commands (platformio-mode))
```
