# Angular Upgrades

## 8 -> 8(latests)

First upgrade to the latest in angular 8

> ng update @angular/core@8 @angular/cli@8

## 8 -> 9

> ng update @angular/core@9 @angular/cli@9

```Javascript
// last line removed in the main.ts file.
// export { renderModule, renderModuleFactory } from '@angular/platform-server';
```

## 9 -> 10

> ng update @angular/core@10 @angular/cli@10

## 10 -> 11

> ng update @angular/core@11 @angular/cli@11

- Failure occurred:

```
npm ERR! ERESOLVE could not resolve
npm ERR!
npm ERR! While resolving: ngxupgrades@0.0.0
npm ERR! Found: @angular-devkit/build-angular@0.1002.4
npm ERR! node_modules/@angular-devkit/build-angular
npm ERR!   dev @angular-devkit/build-angular@"~0.1102.19" from the root project
npm ERR!
npm ERR! Could not resolve dependency:
npm ERR! dev @angular-devkit/build-angular@"~0.1102.19" from the root project
npm ERR!
npm ERR! Conflicting peer dependency: @angular/compiler-cli@11.2.14
npm ERR! node_modules/@angular/compiler-cli
npm ERR!   peer @angular/compiler-cli@"^11.0.0 || ^11.2.0-next" from @angular-devkit/build-angular@0.1102.19
npm ERR!   node_modules/@angular-devkit/build-angular
npm ERR!     dev @angular-devkit/build-angular@"~0.1102.19" from the root project
npm ERR!
npm ERR! Fix the upstream dependency conflict, or retry
npm ERR! this command with --force, or --legacy-peer-deps
npm ERR! to accept an incorrect (and potentially broken) dependency resolution.
npm ERR!
npm ERR! See C:\Users\ssargent\AppData\Local\npm-cache\eresolve-report.txt for a full report.
```

required a force install

> npm i @angular/compiler-cli@11.2.14 -D -f

re built the app

> ng b

Running the app the Angular Cli timed out.

I had to update the npm start command:

```
"start": "echo Starting... && ng serve",
```

## 11 -> 12

> ng update @angular/core@12 @angular/cli@12

Error received:

```
npm ERR! code ERESOLVE
npm ERR! ERESOLVE could not resolve
npm ERR!
npm ERR! While resolving: ngxupgrades@0.0.0
npm ERR! Found: @angular-devkit/build-angular@0.1102.19
npm ERR! node_modules/@angular-devkit/build-angular
npm ERR!   dev @angular-devkit/build-angular@"~12.2.18" from the root project
npm ERR!
npm ERR! Could not resolve dependency:
npm ERR! dev @angular-devkit/build-angular@"~12.2.18" from the root project
npm ERR!
npm ERR! Conflicting peer dependency: @angular/compiler-cli@12.2.16
npm ERR! node_modules/@angular/compiler-cli
npm ERR!   peer @angular/compiler-cli@"^12.0.0" from @angular-devkit/build-angular@12.2.18
npm ERR!   node_modules/@angular-devkit/build-angular
npm ERR!     dev @angular-devkit/build-angular@"~12.2.18" from the root project
npm ERR!
npm ERR! Fix the upstream dependency conflict, or retry
npm ERR! this command with --force, or --legacy-peer-deps
npm ERR! to accept an incorrect (and potentially broken) dependency resolution.
npm ERR!
npm ERR! See C:\Users\ssargent\AppData\Local\npm-cache\eresolve-report.txt for a full report.

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\ssargent\AppData\Local\npm-cache\_logs\2022-11-15T23_19_01_792Z-debug-0.log
✖ Package install failed, see above.
```

Required a force install:

> npm i @angular-devkit/build-angular@12.2.18 -f -D

Rebuilt:

> ng b

## 12 -> 13

## 13 -> 14
