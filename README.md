# Suitcase

A flexible command line tool for instantly deploying user interfaces for simple commands and scripts. 

## Command-Line Utility

### Usage

	OVERVIEW: A flexible command line tool for instantly deploying user interfaces
	for simple commands and scripts.

	USAGE: Suitcase <subcommand>

	OPTIONS:
	  --version               Show the version.
	  -h, --help              Show help information.

	SUBCOMMANDS:
	  basic                   Launch a basic Suitcase process, that has a main menu
							  and an icon in the Dock when running.
	  utility                 Launch a utility Suitcase process, without a Dock
							  icon or main menu.

#### Suitcase `basic`

A `basic` Suitcase process has a [main menu](https://developer.apple.com/documentation/appkit/nsapplication/menus) and an [icon in the Dock](https://developer.apple.com/documentation/appkit/nsdocktile) when running.

See the [full documentation](./Basic.md).

#### Suitcase utility

A `utility` Suitcase process does not have a Dock icon or main menu. It consists of just a [main window](https://developer.apple.com/documentation/appkit/nswindow).

See the [full documentation](./Utility.md).

### Export as a `.command`

TO-DO 

### Examples

#### Hello World

```bash
Suitcase --name="Demo App" --window-title="Hello World" \\
	--window-width="200" --window-height="200" \
	--control-type="label" --control-title="Give a face to every voice…" \
	--control-type="button" \
	--control-title="🗣 Say hello" \
	--control-action="/usr/bin/say Hello World"
```

[![Hello World](./Resources/hello-world.gif)](https://vimeo.com/413136057)

#### Menus

[![Menus](./Resources/menus.gif)](https://vimeo.com/413141354)


```bash
	Suitcase --name="Demo App" --window-title="Menus" \
		--control-title="UUID" \
			--control-type="label" --control-identifier="com.label.uuid" \
		--menu-title="Action>Generate>UUID" \
			--menu-action="/usr/bin/uuidgen" \
				--menu-action-destination="com.label.uuid" \
		--menu-title="Action>Copy UUID" \
		--menu-shortcut="k" \
		--menu-action="/usr/bin/printenv com.label.uuid | /usr/bin/pbcopy"
```

#### Hidden Files & Folders

![Hidden Files & Folders](./Resources/hidden-files-abridged.gif)

```bash
	Suitcase --name="Hidden Finder Settings" \
	--control-title="Hidden Files & Folders:" \
		--control-group-identifier="com.finder.hidden" \
		--control-type="label" \
	--control-title="unknown" \
		--control-group-identifier="com.finder.hidden" \
		--control-type="label" \
		--control-identifier="com.label.hidden.state" \
	--control-title="Refresh" \
		--control-group-identifier="com.finder.hidden" \
		--control-type="button" \
		--control-action="/usr/bin/defaults read com.apple.finder AppleShowAllFiles | /usr/bin/sed s/1/Visible/g;s/0/Hidden/g" \
		--control-action-destination="com.label.hidden.state" \
	--control-title="Enable" \
		--control-type="button" \
		--control-group-identifier="com.finder.hidden.buttons" \
		--control-action="/usr/bin/defaults write com.apple.finder AppleShowAllFiles -bool TRUE & /usr/bin/killall Finder" \
	--control-title="Disable" \
		--control-type="button" \
		--control-group-identifier="com.finder.hidden.buttons" \
		--control-action="/usr/bin/defaults write com.apple.finder AppleShowAllFiles -bool FALSE & /usr/bin/killall Finder"
```

## Bug Reports & Feature Requests

Please [create an issue](https://github.com/Impedimenta/Suitcase/issues).

## Contact

Richard Stelling ([@rjstelling](https://twitter.com/rjstelling))

## Thanks to

- [Dave Verwer](https://github.com/daveverwer) at [iOS Dev Weekly](https://iosdevweekly.com)