# Stuff in my custom.el

## To enable emacs source jumping for C for mplab project:

- Installed ecb for code browsing. Feels kinds of slow.
- Installed global on windows with the win32 port from here
  - http://adoxa.altervista.org/global/
  - Ran GTAGs on root folder of harmony
  - Installed helm-gtags in emacs, setting as in custom.el,
    - instruction fetched from http://tuhdo.github.io/c-ide.html
- Not yet done is code completion.

## To be able to edit FPGA code:

- Added '~/.emacs.d/ucf-mode/ucf-mode.el' to load path.
  This provide ucf file syntax highlighting.

## Outline mode
Don't like the default key binding. Setting them to something
shorter.

## Python stuff
The code added here are to configure python-mode to use ipython
shell. Copied off the web. So far, it does send code to ipython shell,
but it is not interactive. ie. still have to type show() after plot to
show the graph. I'm not sure if it is really needed. Prelube might
have already set it to ipython. Should try that someday.

## Custom variables
This section should be automatically added by emacs customization
tool.

### For web browsing
eww requires gnutls to open https site. gnutls.dll must be on Windows
loadpath. Also, it requires some certifies to open the webpage, and
the default place to look for these certificates are linux
path. Hence, the gnutls-trustfiles variables must be customized to
include the file location in windows. The files I used were downloaded
from
http://xn--9dbdkw.se/diary/how_to_enable_GnuTLS_for_Emacs_24_on_Windows/index.en.html

## Let Emacs display Images
I wish Emacs can simply bundle the dlls with them.

Emacs requires additional dlls for displaying images like png, jpg,
tiff, etc. Some dlls must be located in the /emacs/bin, others can be
simply on the windows path. I just copied everything to
/emacs/bin. Dlls are downloaded from ezwinport. GnuWin32 are old, and
no longer has the files emacs required. To find out what file emacs
requires, evaluate the function by

M-:image-library-alist RET
