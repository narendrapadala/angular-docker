# DockerApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.1.3.

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

## Run commands
docker build -t asbp/sample-angular-app:version-1.0 --build-arg ENV=dev -f Dockerfile .
docker ps -f name=docker-sample-angular-app -q | xargs --no-run-if-empty docker container stop
docker container ls -a -fname=docker-sample-angular-app -q | xargs -r docker container rm
docker run --expose=1012 -p 1012:80 -d --name docker-sample-angular-app asbp/sample-angular-app:version-1.0
