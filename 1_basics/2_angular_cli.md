## Angular cli update:

```s
sudo npm uninstall -g angular-cli @angular/cli
sudo npm cache verify
sudo npm install -g @angular/cli
```
COMMAND | ALIAS | DESCRIPTION
--------|-------|------------
add | | Adds support for an external library to your project.
analytics | | Configures the gathering of Angular CLI usage metrics. See https://v8.angular.io/cli/usage-analytics-gathering.
build | b | Compiles an Angular app into an output directory named dist/ at the given output path. Must be executed from within a workspace directory.
config | | Retrieves or sets Angular configuration values in the angular.json file for the workspace.
deploy | d | Invokes the deploy builder for a specified project or for the default project in the workspace.
doc | d | Opens the official Angular documentation (angular.io) in a browser, and searches for a given keyword.
e2e | e | Builds and serves an Angular app, then runs end-to-end tests using Protractor.
generate | g | Generates and/or modifies files based on a schematic.
help | | Lists available commands and their short descriptions.
lint | l | Runs linting tools on Angular app code in a given project folder.
new | n | Creates a new workspace and an initial Angular app.
run | | Runs an Architect target with an optional custom builder configuration defined in your project.
serve | s | Builds and serves your app, rebuilding on file changes.
test | t | Runs unit tests in a project.
update | | Updates your application and its dependencies. See https://update.angular.io/
version | v | Outputs Angular CLI version.
xi18n | | Extracts i18n messages from source code.
