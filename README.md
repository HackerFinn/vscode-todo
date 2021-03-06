[![GitHub issues](https://img.shields.io/github/issues/HackerFinn/vscode-todo.svg)](https://github.com/HackerFinn/vscode-todo/issues)
[![Join the chat at https://gitter.im/vscode-todo/Lobby](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/vscode-todo/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# TODO extension for Visual Studio Code

This extension adds functionality to list TODO:s in the project:

- Choosing language
- Show TODO:s

# Why the fork of vscode-todo?

It was broken and I was getting annoyed that the maintainer was not updating it.
So here is my fork. I may or may not continue developing it, but at least it works for now. :)

## Features

![Imgur](http://i.imgur.com/p25rHeS.gif)


## Usage

### Settings
To exclude files from the search for TODO's, create the variable todoIgnore in your workspace or user settings:

``` json
{ 
  "todoIgnore":   ["**/test/**"]
}
```

It should contain an array of glob-patterns.

To customize scan expression, create the variable todoScanRegex in your workspace or user settings:

``` json
{ 
  "todoScanRegex":   "(?:TODO|FIXME)\\s*\\W{0,1}(\\s+.*|(?:\\w|\\d).*)$"
}
```

#### Marketplace
The extension is published on Visual Studio Codes marketplace at:
https://marketplace.visualstudio.com/items/HackerFinn.vscode-todo-renewed

Download the extension with Visual Studio Code by open the command palette and run
```bash
  ext install vscode-todo
```

#### Local usage
First you need to clone the project, I strongly recommend you to clone it directly to the extension folder under the .vscode folder, or you can clone it and then copy the project into this location.

The .vscode folder is located under:
* **Windows:** %USERPROFILE%\.vscode\extensions
* **Mac:** $HOME/.vscode/extensions
* **Linux:** $HOME/.vscode/extensions

## Contributing
If you like to contribute with new features or fixing issues just set up a development environment and make a pull request and I will look into that as soon as possible.

#### Development environment
You can set up a development environment for debugging the extension during extension development.

First make sure you do **not** have the extension installed in `~/.vscode/extensions`. Then clone the repo somewhere else on your machine, run `npm install` and open a development instance by pressing **F5**.

```bash
rm -rf ~/.vscode/extensions/vscode-todo
cd ~
git clone https://github.com/HackerFinn/vscode-todo
cd vscode-todo
npm install
code . 
```

## License
[MIT](LICENSE)
