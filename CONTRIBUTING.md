# Contributing Guidelines
This is a work-in-progress but you should follow what's here.


## Formatting
We have a couple general formatting rules.

### General rules
- All links should be `https://` not `http://`. If the website doesn't support https then frankly unless it's ***really*** important that it get's linked it doesn't deserve to be linked to.

### New lines, whitespace (spaces), and line endings
- You shouldn't use TABs, only spaces and indents should be two spaces in size.
- Every file should have a trailing new line (an empty line at the end of the file).
- You should use LF (Unix-style) line endings


## Versioning
We use a slightly modified version of [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html). As this project just config files, we don't have any APIs that can break. For this reason and because of the nature of the project, MAJOR version bumps are for changes that would break downstream forks of this project.
A few examples are; changing an alias name, changing the functionality of an alias, or changing a convar that other commands depend on the value of.


## Don't use Notepad++
Yes, it's what the community has used for a really long time but it's old, less than ideal, and outdated.

### What should I use then?
[Microsoft Visual Studio Code](https://code.visualstudio.com) with [CFG Games Support](https://marketplace.visualstudio.com/items?itemName=joelcancela.cfg-games-support). It has literally everything in Notepad++ plus way more and it hass "extensions" that let you customise and add functionality to VSC.
The extension metioned above callled [CFG Games Support](https://marketplace.visualstudio.com/items?itemName=joelcancela.cfg-games-support) **extremely useful**; it changes the coloring of comments, commands, convars, arguments, and delimiters (`"`s and `;`s). This makes it way less confusing and to be completely honest, Notepad++ is a joke compared to VSC.
