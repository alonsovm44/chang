# Chang
Chang is a simple, easy to use, practical CLI tool written in Glupe to keep track of changes in your project. It is not meant to replace git, but to work along side it. 

Given the nature of glupe files, `main.acn`can be compiled to C, C++, Rust, Go, Python or any supported language by Glupe.

## Setup
1. Download Chang.exe and set it in C:\chang\chang.exe
1. Or build from source with `glupe main.acn -o chang.exe -target-lang` 
2. Set Chang to path

## How to use
1. Begin by running:
`chang init`
This creates a CHANGELOG.md file with a starting template
```
## v0.0.0 2026-02-13

Added:

Removed:

Improved/Fixed:
```

2. `chang help` 
This outputs
```bash
chang help menu:
Commands:
  init - create CHANGELOG.md
  new <version> - create new version block
  log -a|-r|-f <message> [version]
```
3. Chang begins the changelog by default on v0.0.0, to bump a new version entry run
`chang new <version>`

This creates a version entry on The beggining of the file.

4. Loging a change
`chang log -a|-r|-f <message>`

Typing `-a`will log the message into the added section of the changelog
Typing `-r`will log the message into the removed section of the changelog
Typing `-f`will log the message into the fixed section of the changelog

If no version is specified in the command, Chang will by default log in the most recent version.
To override this, specify a version to log the change at. 