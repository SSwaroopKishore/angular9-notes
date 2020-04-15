* The first file that is executed on launch of a angular application is index.html.
* Once index.html is rendered it will search for the main.ts file.
* Once the main.ts file is launched, within the file we mention which file or module should be bootstrapped first.
* In the example of main.ts, we have mentioned that app.module.ts is the first module that is going to be executed or launched by angular. We also imported the file before injecting it to angular's bootstrap method.
* App.module.ts is a simple typescript class with angular defined decorators to identify that this file is going to represent a module.
* The module has following properties:
    * Declarations: here we declare all the components that are part of the app module.
    * Imports: here we declare the names of all the imports that are required by the components of the app module.
    * Providers: here we declare all the providers that are used by this particular module.
    * Bootstrap: here we declare the bootstrapping component of the app module.
* Now the respective bootstrapping component declared in the bootstrap property of the app module will be executed. This hierarchy continues further based on the declarations made in the components.

> files like angular.json will not be executed by the browser since these files are used for the purpose of configuration by the angular to do cli specific tasks like serve, build, test etc..
