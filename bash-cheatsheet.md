# BASH Cheatsheet
- As applied in [Secure Shell ChromeOS app](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo?hl=en)


## Cursor

`enter` Run command

`arrow-up` & `arrow-down` Previous commands

`arrow-left` & `arrow-right` Move cursor

`tab` Complete directory or file name

`ctrl+a` Move cursor to beginning

`ctrl+e` Move cursor to end

`ctrl+arrow-left` Move to beginning previous word

`ctrl+arrow-right` Move to end of next word

`ctrl+u` Clear from cursor to beginning of line

`ctrl+k` Clear from cursor to end of line

`ctrl+r` Find character sequence in history (typeahead)

`ctrl+l` Clear the terminal


## Info

`pwd` Print Working Directory

`ls` List files in current directory

`ls -a` List All files in current directory (hidden included)

`ls -al` List All Files as a List (shows permissions)

`ls -l *.css` Limited List of only .css files

`du -h` Disk Usage list of folders in Human readable output

`du -ah` Disk Usage list of All files & folders in Human readable output


## Navigation

`cd ~` Navigates (ie: Change) to the root directory

`cd path/to/directory` Navigate to directory
  *hint: start typing then hit 'tab' to auto-complete*

`cd ..` Navigate to the directory up one level


## File Manipulation

`mkdir <folder-name>` Make a new Directory at current location

`mv foo.txt bar/` Move file `foo.txt` into folder `bar`

`mv beans toast` Move folder `beans` into folder `toast`

`mv foo.txt foo.md` Rename file `foo.txt` to `foo.md`
  *Can rename filename or extension or both*

`mv beans/ ..` Move a folder `beans` up one level
