# Angular 6 CLI - Cheatsheet
  
## Introduction
  
This cheat sheet is based on a John Papa Tutorial on Plural Sight.
  
> You can find more necessary information here: cli.angular.io

## Commands

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

The following command shows the installed cli without any dependency.  

```npm
npm list -g @angular/cli --depth=0
```

### Prefix
This command allows you to define your own personal prefix for 
```typescript
ng new my-app --prefix [your_prefix_name]
```
  
