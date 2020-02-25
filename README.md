
https://relaxed-hodgkin-68afc6.netlify.com/


Scully and Angular Static site generator:

Reference:

1.Create a Static Site Using Angular & Scully (with Tara Z. Manicsic) — Learn With Jason 1,218 views •18 Dec 2019

https://www.youtube.com/watch?v=ugTx-14jRrI&t=3107s



Commands:


cd projects

cd scully-angular-jamstack-sites

ng --version

 ng new jamgularOne

? Would you like to add Angular routing? Yes
? Which stylesheet format would you like to use? SCSS   [ https://sass-lang.com/
documentation/syntax#scss  

krishna@krishna-Lenovo-G50-70:~/projects/scully-angular-jamstack-sites$
cd jamgularOne

krishna@krishna-Lenovo-G50-70:~/projects/scully-angular-jamstack-sites/jamgularOne$
ng serve --open

 ng g m home --route home --module app.module.ts

 ng g m users --route users --module app.module.ts

ng g m about --route about --module app.module.ts

krishna@krishna-Lenovo-G50-70:~/projects/scully-angular-jamstack-sites/jamgularOne$
ng g c user/users

**************************************************************************************
app-routing.module.ts

import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';


const routes: Routes = [{ path: '', loadChildren: () => import('./home/home.module').then(m => m.HomeModule) }, { path: 'users', loadChildren: () => import('./users/users.module').then(m => m.UsersModule) }, { path: 'about', loadChildren: () => import('./about/about.module').then(m => m.AboutModule) }];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
***********************************************************************************************************

ng serve --port 4204

ng build

ng add @scullyio/init

npm i @scullyio/ng-lib

 npm run scully

Static site:

https://relaxed-hodgkin-68afc6.netlify.com/





# JamgularOne

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.2.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
