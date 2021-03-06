# tcpure README

TCPURE is a lightweight, featureless client for TidalCycles. 
Just an editor and _fast_ GHCI REPL output via 
the VS Code terminal. Uses a hard-coded Tidal bootup sequence with no
possibility of customization (yet?).

## Features

Just start typing some TidalCycles code, and eval it:

* `Shift+Enter` for a single line eval
* `Ctrl+Enter` for a multi-line eval

**This extension's keybindings will conflict with the main TidalCycles
extension**, so make sure to disable that extension's keyboard shortcuts
before using this one. 

You do not need to use a file with a `.tidal` extension. You can eval
Tidal code in any type of file.

## Installation from Binaries

If you want to install from a release, download the binary and then:

``` 
code --install-extension tcpure-1.1.0.vsix
```

## Build and install from source

Otherwise if you want to install from the source code you will need to use
`vsce` to package it first:

``` 
git clone git@github.com:kindohm/tcpure.git
cd tcpure
vsce package
code --install-extension tcpure-1.1.0.vsix
```

## Custom Bootup

If you really, _really_ want to use a custom Tidal bootup, then you will need
to modify the source code. Modify the `bootCommands.ts` file however
you like, then follow the "Build and install from source" instructions above.

## Contributing

The purpose of this extension is to provide a clean, minimal Tidal 
environment that is _fast_ in VS Code. Anything beyond minimal, default
Tidal behavior will not be accepted in pull requests. 

Feel free to submit a pull request for:

* bug fixes
* missing _default_ behaviors that you would normally find in [BootTidal.hs](https://github.com/tidalcycles/Tidal/blob/main/BootTidal.hs).
* aesthetic enhancements that possibly improve the appearance during a live performance
