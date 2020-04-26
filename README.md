# Suitcase

A flexible command line tool for instantly deploying user interfaces for simple commands and scripts. 

## Command-Line Utility

### Usage

	OVERVIEW: Create and Run SwiftUI apps from the command line, for no reason.

	USAGE: suitcase <subcommand>

	OPTIONS:
	  --version               Show the version.
	  -h, --help              Show help information.

	SUBCOMMANDS:
	  basic                   Launch a basic application.
	  utility                 Launch a utility application.

#### Suitcase basic

	OVERVIEW: Launch a basic application.

	USAGE: suitcase basic <options>

	OPTIONS:
	  --name <name>           The name of the currently running Case. 
	  --icon <icon>           Path to an image file (JPEG, PNG) to use as the app icaon in the Dock. 
	  --environment <environment>
							  Set environmental variables. 
	  --window-title <window-title>
							  Title of the main window. 
	  --window-floating       Title of the main window. 
	  --window-width <window-width>
							  Width (in pixels) of the main window on first run. (default: 400)
	  --window-height <window-height>
							  Height (in pixels) of the main window on first run. (default: 320)
	  --drop-working-directory
							  Set the working directory to any directly dropped on the window 
	  --menu-title <menu-title>
							  The hierarchical path to the menu, seperated by >. 
	  --menu-action <menu-action>
							  A menu itms action. 
	  --menu-shortcut <menu-shortcut>
							  The keybaord shortcut for the menu item. 
	  --menu-action-destination <menu-action-destination>
							  The identifier of a control to send the output of the action to. 
	  --working-directory <working-directory>
							  Switch to this directory before running any actions. 
	  --control-type <control-type>
							  The type of control, see docs for a full list. 
	  --control-title <control-title>
							  The title or value of a control. Can be set by actions. 
	  --control-identifier <control-identifier>
							  A unique identfier for the control. Can be used to reference the control in actions. 
	  --control-action <control-action>
							  A controls action, only valid for `button`. Ignored if used incorrectly. 
	  --control-action-parameter <control-action-parameter>
							  A comma seperated list of parameter passed to an action. 
	  --control-action-destination <control-action-destination>
							  The identifier of a control to send the output of the action to. 
	  --control-group-identifier <control-group-identifier>
							  An identfier to group controls on screen. The first control in the group determines the on screen order of
							  the group. 
	  -V, --verbose           Increade the logging verbosity, included multiple times to increse verbosity level (max 4). 
	  --version               Show the version.
	  -h, --help              Show help information.

#### Suitcase utility

	OVERVIEW: Launch a utility application.

	USAGE: suitcase utility <options>

	OPTIONS:
	  --name <name>           The name of the currently running Case. 
	  --icon <icon>           Path to an image file (JPEG, PNG) to use as the app icaon in the Dock. 
	  --environment <environment>
							  Set environmental variables. 
	  --window-title <window-title>
							  Title of the main window. 
	  --window-floating       Title of the main window. 
	  --window-width <window-width>
							  Width (in pixels) of the main window on first run. (default: 400)
	  --window-height <window-height>
							  Height (in pixels) of the main window on first run. (default: 320)
	  --drop-working-directory
							  Set the working directory to any directly dropped on the window 
	  --working-directory <working-directory>
							  Switch to this directory before running any actions. 
	  --control-type <control-type>
							  The type of control, see docs for a full list. 
	  --control-title <control-title>
							  The title or value of a control. Can be set by actions. 
	  --control-identifier <control-identifier>
							  A unique identfier for the control. Can be used to reference the control in actions. 
	  --control-action <control-action>
							  A controls action, only valid for `button`. Ignored if used incorrectly. 
	  --control-action-parameter <control-action-parameter>
							  A comma seperated list of parameter passed to an action. 
	  --control-action-destination <control-action-destination>
							  The identifier of a control to send the output of the action to. 
	  --control-group-identifier <control-group-identifier>
							  An identfier to group controls on screen. The first control in the group determines the on screen order of
							  the group. 
	  -V, --verbose           Increade the logging verbosity, included multiple times to increse verbosity level (max 4). 
	  --version               Show the version.
	  -h, --help              Show help information.

### Examples

#### Hello World

![Hello World](./Resources/hello-world.gif)

#### Menus

![Menus](./Resources/menus.gif)

## Contact

Richard Stelling ((@rjstelling)[https://twitter.com/rjstelling])