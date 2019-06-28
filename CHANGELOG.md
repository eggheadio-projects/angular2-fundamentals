# Changelog

All notable changes to “Get Started with Angular” will be documented in this file.

ran npm install and npm start

ran into `The serve command requires to be run in an Angular project, but a project definition could not be found.`

found this stack overflow that solves the issue: https://stackoverflow.com/questions/53096996/angular-cli-error-the-serve-command-requires-to-be-run-in-an-angular-project-b

suggests running this command:

`ng update @angular/cli --migrate-only --from=4.1.1`

that command needs all the dependencies to be updated

ran `ng update --all` to update

added `@angular-devkit/schematics` and `@angular/cli` to the project because updated dependencies need

ran `ng update @angular/cli --migrate-only --from=4.1.1` again

ran into this error:
```
(app.assets || []).map is not a function
```

removed `assets: "assets"` from `angular-cli.json` and re-ran `ng update` command

Ran npm install: errors out again

installed `webpack`

run npm install again now ran into this error:

```
Cannot find module 'webpack/lib/removeAndDo'
```

We've added and removed a good number of packages, going to delete `node_modules` and `package-lock.json` and `npm install` again

deleted `angular-cli` as this package was accidentally added in place of `@angular-cli`

ran `npm start`, ran into this error:

```
Cannot find module '@angular/compiler-cli'
Error: Cannot find module '@angular/compiler-cli'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:582:15)
    at Function.Module._load (internal/modules/cjs/loader.js:508:25)
    at Module.require (internal/modules/cjs/loader.js:637:17)
    at require (internal/modules/cjs/helpers.js:22:18)
```

installed `@angular/compiler-cli`

ran npm start again and ran into this error:
```
ERROR in The Angular Compiler requires TypeScript >=3.4.0 and <3.5.0 but 3.5.2 was found instead
```

re-installing TypeScript@3.4.2

Angular compiles and errors out with this message:

```
ERROR in src/app/app.module.ts(4,28): error TS2307: Cannot find module '@angular/http'
```

In `src/app/app.module.ts` changed `@angular/http` import to `@angular/common/http`

looked at deprecation guide for `@angular/http` https://angular.io/guide/deprecations#angularhttp

`Replace HttpModule with HttpClientModule (from @angular/common/http) in each of your modules.`




## 1.0.0
- Code is compatible with codesandbox.
- The instructor's github repo had all the lesson code from the beginning of each lesson rather than the end.
- `webpack-cli` now has to be added as a devDependency.

### Added

- This file.
- .JSON output file
- All the lesson code as subfolders within the main branch, rather than as individual branches.

### Changed

- Update `@angular/common#4.1.1->7.2.12`.
- Update `@angular/core#4.1.1->7.2.12`.
- Update `@angular/compiler#4.1.1->7.2.12`.
- Update `@angular/forms#4.1.1->7.2.12`.
- Update `@angular/http#4.1.1->7.2.12`.
- Update `@angular/platform-browser#4.1.1->7.2.12`.
- Update `@angular/platform-browser-dynamic#4.1.1->7.2.12`.
- Update `@angular/router#4.1.1->7.2.12`.
- Update `core-js#2.4.1->3.0.1`.
- Update `rxjs#5.0.0->6.4.1`.
- Update `ts-helpers#1.1.1->1.1.2`.
- Update `zone.js#0.8.10->0.9.0`.
- Breaking Change: For the update from core-js 2.4.1 -> 3.0.1, the polyfills.ts import from "core-js/es6/" and "core-js/es7/" deprecated for all modules. Changed to "core-js/features/".

### Removed
- Code that the Master branch consisted of, as it was identical to the code for lesson 13.
- all the branches which previously stored lesson code

