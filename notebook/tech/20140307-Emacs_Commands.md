Mar 7 2014 | Emacs, IDE | Kelly Chan
# Emacs Commands

## 1. Basic Commands

- `C-x`: `ctrl-x`, to control buffers/windows/files
- `M-x`: `Alt-x`, to run commands
- `RET`: `Enter`

commands summary and .emacs reloaded
- `M-x make-command-summary`: show all commands
- `M-x load-file path/.emacs`: refresh file

### (1) basic

close and quit
- `C-x C-c`: close emacs
- `C-g`: quit

help
- `C-h C-h`: help
- `C-h i`: the info directory

### (2) buffers and windows

control buffers
- `C-x b`: switch buffers
- `C-x k`: kill buffer
- `C-x ->`: right-cycle through buffers
- `C-x <-`: left-cycle through buffers

control windows
- `C-x o`: change active window to next window
- `C-x 0`: close the active window
- `C-x 1`: colose all windows except the active window
- `C-x 2`: split the active window vertically into two horizontal windows
- `C-x 3`: split the active window horizontally into two vertical windows

### (3) files

file open/save
- `C-x C-f`: open file
- `C-x C-s`: save file
- `C-x C-w`: save file as

file edit
- `C-k`: kill current line
- `C-y`: yank current line

### (4) search

- `C-s`: search forwards
- `C-r`: search backwards
- `M-%`: find and replace


## 2. Customization and Themes

### (1) customization

custom-settings written in .emacs

`.emacs` script:
```lisp
;--------------------;
;;; User Interface ;;;
;--------------------;

; ignore case when searching
(setq case-fold-search t)

;----------------------;
;;; Windows & Frames ;;;
;----------------------;

; language
(setq current-language-environment "English")

; don't show the tool bar
(tool-bar-mode -1)

; display line numbers of the window
(global-linum-mode t)
; show the current line and column numbers in the stats bar as well
(line-number-mode t)
(column-number-mode t)
```

### (2) theme

commands: 
- `M-x color-theme-select`, to select theme, and write the theme name to .emacs  

installation:
- step1. download [color-theme](http://download.savannah.gnu.org/releases/color-theme/)
- step2. unzip folder (`themes` folder and `color-theme.el`) to `~/.emacs.d/plugins/color-theme-6.6.0`
- step3. open `~/.emacs`, and write scripts

.emacs script
```lisp
; color theme
(add-to-list 'load-path "~/.emacs.d/plugins/color-theme-6.6.0")
(require 'color-theme)
(color-theme-initialize)  
(setq color-theme-is-global t)
(color-theme-billw)
```

## 3. Packages and Extensions

packages installation
- step1. `M-x list-packages`: open package-list
- step2. search a package, select and install
- step3. settings in .emacs


---
### References
1. [Absolute Beginner's Guide to Emacs](http://www.jesshamrick.com/2012/09/10/absolute-beginners-guide-to-emacs/)
