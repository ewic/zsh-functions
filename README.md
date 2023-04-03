# Introduction

Each file contains a function that is autoloaded in my zsh environment. Feel free to take or modify anything found in here.

# Installation and Usage

Method taken from blog post found here: https://dev.to/lukeojones/1up-your-zsh-abilities-by-autoloading-your-own-functions-2ngp

Download and move the files somewhere useful, suggestion is `~/.zshfn`.

Modify your `.zshrc` file to recognize autoload all the files in the specified folder:

```bash
# Append this to the bottom of your ~/.zshrc file
fpath=( ~/.zshfn "${fpath[@]}" )
autoload -Uz $fpath[1]/*(.:t)
```

# Function Index

## gopro-rename

Multi-part gopro files are named in a very unhelpful manner. This function simply asks for confirmation and then renames all the files into a sensible file-chapter style.