# Logger - Logging singleton for Godot Engine

The _Logger_ class is a GDScript singleton that provides a logging API for projects developed with [Godot Engine](https://godotengine.org).

## Usage

Copy the `Logger.gd` file into your project folder, and define it as an autoloaded singleton in your project's settings (Project > Project Settings > AutoLoad), with the name `Logger`. The methods of the API can then be accessed from any other script via the `Logger` singleton:

```
Logger.info('There is a snake in my boot!')
Logger.warn('Alpaca mismatch!')
```

### Modules

Can define a module for better scope control and finer controls

```
Logger.add_module('Entity')
Logger.info('Reticulating splines...', 'Entity')
```

### Log files

Remember to enable logging to files in your project settings (Project > Project Settings > General > Logging > File Logging). If you're on macOS, you're file will output somewhere like

```
~/Library/Application Support/Godot/app_userdata/<PROJECT_NAME>/logs
```

## Licensing

The Logger class and all other files of this repository are distributed under the
MIT license (see the LICENSE.md file).
