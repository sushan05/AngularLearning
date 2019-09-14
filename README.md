# Creating first Angular application

Now that you have Angular and its dependencies installed, we can move on and start building our Angular app. Let’s get started!

Starting a new angular app with the CLI is easy! From your command line, run this command: `ng new "my-app"`

The command above will create a folder named `"my-app"` and will copy all the required dependencies and configuration settings. The Angular CLI does this for you:

* Creates a new directory "my-app"
* Downloads and installs Angular libraries and any other dependencies
* Installs and configures TypeScript
* Installs and configures Karma & Protractor (testing libraries)
* You can also use the ng init command. The difference between ng init and ng new is that ng new requires you to specify the folder name and it will create a folder copying the files while ng init will copy the files to the current folder.

Now, you can cd into the created folder. To get a quick preview of your app inside the browser, use the serve command use `ng serve`

This command runs the compiler in watch mode (looks for changes in the code and recompiles if needed), starts the server, launches the app in a browser, and keeps the app running while we continue building it.

The Webpack Development server listens on HTTP port 4200. Hence, if you open the url `http://localhost:4200/` you will see the app running.

Note - Below documentation is inspired from [official angular site docs](https://angular.io/guide/file-structure)

# Workspace configuration files

All projects within a workspace share a [CLI configuration context](https://angular.io/guide/workspace-config). The top level of the workspace contains workspace-wide configuration files, configuration files for the root-level application, and subfolders for the root-level application source and test files.

WORKSPACE CONFIG FILES  |  PURPOSE
-----------------------  |  -----------
.editorconfig  |  Configuration for code editors.
.gitignore  |  Specifies intentionally untracked files that Git should ignore.
README.md  |  Introductory documentation for the root app.
angular.json  |  CLI configuration defaults for all projects in the workspace, including configuration options for build, serve, and test tools that the CLI uses, such as TSLint, Karma, and Protractor. For details, see Angular Workspace Configuration.
package.json  |  Configures npm package dependencies that are available to all projects in the workspace. See npm documentation for the specific format and contents of this file.
package-lock.json  |  Provides version information for all packages installed into node_modules by the npm client. See npm documentation for details. If you use the yarn client, this file will be yarn.lock instead.
src/  |  Source files for the root-level application project.
node_modules/  |  Provides npm packages to the entire workspace. Workspace-wide node_modules dependencies are visible to all projects.
tsconfig.json  |  Default TypeScript configuration for projects in the workspace.
tslint.json  |  Default TSLint configuration for projects in the workspace.


# Application project files

By default, the CLI command `ng new my-app` creates a workspace folder named "my-app" and generates a new application skeleton in a `src/` folder at the top level of the workspace. A newly generated application contains source files for a **root module**, with a **root component** and **template**.

## Application source files

APP SUPPORT FILES  |  PURPOSE
-----------------  |  ----------
app/  |  Contains the component files in which your application logic and data are defined. 
assets/  |  Contains image and other asset files to be copied as-is when you build your application.
environments/  |  Contains build configuration options for particular target environments. By default there is an unnamed standard development environment and a production ("prod") environment. You can define additional target environment configurations.
favicon.ico  |  An icon to use for this application in the bookmark bar.
index.html  |  The main HTML page that is served when someone visits your site. The CLI automatically adds all JavaScript and CSS files when building your app, so you typically don't need to add any <script> or<link> tags here manually.
main.ts  |  The main entry point for your application. Compiles the application with the JIT compiler and bootstraps the application's root module (AppModule) to run in the browser. You can also use the AOT compiler without changing any code by appending the --aot flag to the CLI build and serve commands.
polyfills.ts  |  Provides polyfill scripts for browser support.
styles.sass  |  Lists CSS files that supply styles for a project. The extension reflects the style preprocessor you have configured for the project.
test.ts  |  The main entry point for your unit tests, with some Angular-specific configuration. You don't typically need to edit this file.

_Inside the src/ folder, the app/ folder contains your project's logic and data. Angular components, templates, and styles go here._

SRC/APP/ FILES  |  PURPOSE
--------------  |  --------
app/app.component.ts  |  Defines the logic for the app's root component, named AppComponent. The view associated with this root component becomes the root of the view hierarchy as you add components and services to your application.
app/app.component.html  |  Defines the HTML template associated with the root AppComponent.
app/app.component.css  |  Defines the base CSS stylesheet for the root AppComponent.
app/app.component.spec.ts  |  Defines a unit test for the root AppComponent.
app/app.module.ts  |  Defines the root module, named AppModule, that tells Angular how to assemble the application. Initially declares only the AppComponent. As you add more components to the app, they must be declared here.