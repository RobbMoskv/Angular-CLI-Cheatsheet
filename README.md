# Angular 6 CLI - Cheatsheet
  
## Introduction
  
This cheat sheet has been created during a John Papa Tutorial on Plural Sight. This summary does not cover all possible  
commands at all. They are just notes I consider as useful.  
  
You can find more necessary information here on the **official Angular CLI** webpage.  
> Visit _cli.angular.io_

## Commands - Generate a new Angular Application

### Help
Let me see all possible commands and their shortcuts how to generate a new App.  

```typescript
ng new --help
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

## Commands - CLI Configuration

### Configuration
Use the _angular.json_ file path to define your (global) config file settings.  
```typescript
ng config [what_ever]
```
## Commands - Linting
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
