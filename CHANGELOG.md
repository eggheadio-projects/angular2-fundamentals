\# Changelog

All notable changes to “Get Started with Angular” will be documented in this file. 

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

