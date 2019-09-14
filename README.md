# Angular Component

A component controls a patch of screen called a view. They are the most basic building block of an UI in an Angular application. An Angular application is a tree of Angular components. **Angular components are a subset of directives.** Unlike directives, components always have a template and only one component can be instantiated per an element in a template.

Components are defined using the `@component` decorator. A component has a `selector`, `template`, `style` and other properties, using which it specifies the metadata required to process the component.


# Understanding Component

For understanding component, let's take the refrence of root-component i.e. `app.component`.
In `src/app/`, you will find four different files for root-component as listed below
* `app.component.css`
* `app.component.html`
* `app.component.spec.ts`
* `app.component.ts`


## Let's open the `app.component.ts` file and go through it.

```javascript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'Angularlearning';
}
```
* the first thing that you will notice is a class named as `AppComponent` with a decorator `@Component`
* the decorator is used to let Angular know that the corresponding class will act as an Angular Component.
* to configure the component, we will need to pass the metadata in the `@Component` decorator. The metadata has properties such as `selector`, `templateUrl`, `styleUrls` and many more. You can find the list of other properties and there significance in the [offical docs of compoent](https://angular.io/api/core/Component)


# Creating a custom Component
Here we will be creating a basic custom component for displaying "hello world!". We will using angular-cli for creating our very first custom component.

So, first open your porject in vs-code. Then open the terminal window of vs-code and hit the command `ng generate component helloworld`. Once the command is executed, you will see some messages in the terminal as shown below

```
CREATE src/app/helloworld/helloworld.component.html (25 bytes)
CREATE src/app/helloworld/helloworld.component.spec.ts (656 bytes)
CREATE src/app/helloworld/helloworld.component.ts (285 bytes)
CREATE src/app/helloworld/helloworld.component.css (0 bytes)
UPDATE src/app/app.module.ts (412 bytes)
````

The message says that few new has been created viz. - `helloworld.component.html, helloworld.component.spec.ts, helloworld.component.ts, helloworld.component.css` and **`app.module.ts` has been updated**

* In `src/app/` directory, you will find a new directory has been created - named similar to our new component name i.e. `helloworld` inside which, the above four files will be present.
* In `app.module.ts` file, our new component will be automatically imported and will be be passed in the `decalarations` array of `@NgModule` decorator metadata
Above steps are done my anuglar-cli for you, when you create a component through it.

## Displaying our custom component
* Open the template file of our component i.e. `helloworld.component.html`. You will find a default content (`<p>helloworld works!</p>`) in this file. Change it to `<h1>Hello World!</h1>` and save the file.
* now, open the `ts` file of our component i.e. `helloworld.component.ts` and look for the selector value from it. The selector value would be `app-helloworld`.
* now, open our root-component's template file i.e. `app.component.html`. It will have some default content which is of no use for us; so, delete it. Then open-close a `html tag` whose name is same as that of our component selector i.e. `<app-helloworld></app-helloworld>` and save the file.
* now, serve our angular app using `ng serve --open` command and you will find that `Hello World!` text been displayed on browser.