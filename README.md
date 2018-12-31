# Angular 6 CLI - Cheatsheet
  
## Introduction
  
This cheat sheet has been created during a John Papa Tutorial on Plural Sight. This summary does not cover all possible  
commands at all. They are just notes I consider as useful.  
  
You can find more necessary information here on the **official Angular CLI** webpage.  
> Visit _cli.angular.io_
  
## Table of content

1. [Generate new Applications](#Generate-new-App)
2. [CLI Configuration & Setup](#CLI-Configuration)
3. [Linting](#Linting)
4. [Generating Code from Blueprints](#Blueprints)
5. [Building and Serving](#Building-and-Serving)
6. [Unit and End2End Tests](#Testing)
7. [Tooling & Features)(#Tools-and-Features)

## Generate new App

### Help
Let me see all possible commands and their shortcuts how to generate a new App.  

```typescript
ng new --help
```
Or just display all possible commands in general.  
```typescript
ng --help
```

### Skip installation
Generate the app and skips the **npm install**  

```typescript
ng new ngtest --skip-install
```
### Verify
Verify that all is well on our environment

```typescript
ng-v
```

### Dry run
Don't create the files but report them  

```typescript
ng new my-app --dry-run
```

### Dependency
The following command shows the installed cli without any dependency.  

```npm
npm list -g @angular/cli --depth=0
```

### Prefix
This command allows you to define your own personal prefix.  

```typescript
ng new my-app --prefix [your_prefix_name]
```

### Skip Test
Add this option to prevent the CLI to add .spec files to each component.  

```typescript
ng new my-app --skip-tests
```

### Sass Style
This command allows you to add scss as your default style extention.  

```typescript
ng new my-app --style scss
```
  
### Git
Do not add the project to git.  
```typescript
ng new my-app --skip-git
```
  
### Routing
Add an own routing module to the project  
```typescript
ng new my-app --routing
```

## CLI Configuration

### Configuration
Use the _angular.json_ file path to define your (global) config file settings.  
```typescript
ng config [what_ever]
```
## Linting
tbd

### Help
This command shows all available option for linting a project.  

```typescript
ng lint my-app --help
```

### Style the lint output
With the following flag you can format and color your lint output in an easier readable format.  
```typescript
ng lint my-app --format stylish
```

### Fix code
By adding the following flag any detected errors are going to be fixed itslef and immediately applied.
```typescript
ng lint my-app --fix
```

## Generate Blueprints

With this feature you can generate code from a blueprint by using aliases.  
  
> Use the out-of-the-box blueprints
  
  
### Generate Component

```typescript
ng generate component customer  
ng g c customer
```
### Generate Directive
```typescript
ng generate directive search 
ng g d search
```
### Generate Pipe
```typescript
ng generate pipe init-caps 
ng g p init-caps 
```
### Generate Class
```typescript
ng generate class customer-model
ng g cl customer-model
```

### Generate Interface
```typescript
ng generate interface orders
ng g i orders
```

### Generate Enum
```typescript
ng generate enum gender
ng g e gender
```

### Generate Modules
```typescript
ng generate module sales -module app.module
ng g m sales -m app.module
```
## Routing Blueprints

### Generate Component  
A new app with module & routing module
```typescript
ng new sales --routing
```

New module plus a routing module. Afterwards create a new component within this admin module.
```typescript
ng g m admin --routing
ng g c admin/users
```

## Building and Serving

> Use the ng <command> **--help** flag to get 
> an overview which options are availbale for this specific command.

### Webpack Analyzer

Installing
```javascript
npm install webpack-bundle-analyzer --save-de
```
By building with the stats flag the output can be examed.
```typescript
ng build --stats-json
```

Add an additional script within the _package.json_ file to allow automated build option.
```json
"stats": "npx webpack-bundle-analyzer dist/angular-routing/stats.json",
```

With the following command a graphical view of webpack is generated and displayed here: _http://127.0.0.1:8888/_
```javascript
npm run stats
```
---
### Common ng build options

Generates a source map while building the solution. (Default on Dev-build)
```typescript
ng build --source-map
```

Provides an _ahead of time_ compilation.
```typescript
ng build --aot
```

Provides an the option to _watch_ and _rebuild_ the dist solution.
```typescript
ng build --watch // (-w)
```

Create an optimized production build.
```typescript
ng build --prod // (-p)
```
---
### Common ng serve options

> All options from **ng build** are available as well for serving.

Define a different port to listen on while serving.
```typescript
ng serve --port
```

Enables the live reloader (can be done via config file as well.
```typescript
ng serve --live-reload // 
```

Servers using https protocol / or certificate
```typescript
ng serve --ssl
```

Allows you to configurate your proxy settings.
```typescript
ng serve --proxy-config
```
---
### Common ng add options

Add new capabilities to existing app.
```typescript
ng add [package]
ng add @angular/material
```
## Testing

### Standard run
Run to test all defined specs within this application.
```typescript
ng test <options>
```

### Code coverage flag
Generates a code coverage report (default false)
```typescript
ng test --code-coverage
```

### Progress Log flag
Logs the test progress to the console (default true)
```typescript
ng test --progress
```

### Sourcemap flag
Enables debuger tests by generating source maps (default true).
```typescript
ng test --sourcemaps
```

### Watch flag
Runs the test once and watchs for changes and re-runs the test (default true).  
Set to false for single test runs.
```typescript
ng test --watch
```
## Tools and Features

### Update
```typescript
ng update
```

