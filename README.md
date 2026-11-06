# vim speak : screen reader for Vim (speech-dispatcher)

Implementation of a screen reader : makes Vim speak using
speech-dispatcher (spd-say). If you are using Orca, it should already be installed.

Depends on plugins : [selection](https://github.com/luffah/vim-selection), [keybindings](https://github.com/luffah/vim-keybindings).

```vim
:SpeakLine      " speak the whole line
:SpeakWORD      " speak the following word (vim: W to go to next word)
```
Setup in .vimrc:
```vim
packloadall    " if using vim pack structure

" (can setup lang and voice with g:speak_lang and g:speak_voice_type
"  else use spd-say default)
call speak#enable(0)   " Speak* commands only
call speak#enable(1)   " Speak* commands and keybinding layer
```

In a GVim or Vim, just hit `<C-s>` (Ctrl + s) to toggle the screen
reader mode.

# Example installation


```sh
mkdir -p ~/.vim/pack/ui/start/
cd ~/.vim/pack/ui/start

# Install keybindings lib
wget https://github.com/luffah/vim-keybindings/archive/refs/heads/main.zip
unzip main.zip

# Install selection lib
wget https://github.com/luffah/vim-selection/archive/refs/heads/main.zip
unzip main.zip

# Install speak lib
wget https://github.com/luffah/vim-speak/archive/refs/heads/main.zip
unzip main.zip
```
Dependencies on GNU/Linux : speech-dispatcher (`spd-say`),
recommended : mbrola, gnome-orca.

License GPLv3.
