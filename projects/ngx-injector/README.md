# ngxInjector

ngxInjector is a simple and lightweight Angular module build to dynamically injecting components into the DOM.

## Installation

##### Install via [NPM](http://www.npmjs.org):
  ```bash
  npm install @hangar42/ngx-injector
  ```
  or manually [download](https://github.com/Hangar42-de/ngx-injector/archive/master.zip) it.

## Usage

##### 1. Include InjectorModule as a dependency in your desired module:
  ```javascript
  import {InjectorModule} from 'ngx-injector';
  ...
  imports: [
    InjectorModule,
    ...
   ]
  ```

##### 2. Use The InjectorService
 ```javascript
  import {InjectorService} from 'ngx-injector';
  import {SomeComponent} from '../some.component';
  ...

  constructor(private injectorService: InjectorService){}
  
  public someFunction(){
    const params = {
      ... properties you want to inject in the component
    }
    this.injectorService.injectComponent(SomeComponent, params);
  }
  ```

## Development

* Clone the repo or [download](https://github.com/Hangar42-de/ngx-injectorf/archive/master.zip) it
* Install dependencies: ``npm install``
* Run ``ng build --project ngx-injector``
* Run ``ng serve``

## License

GPLv3 [Link](https://github.com/Hangar42-de/ngx-injector/blob/master/LICENSE/)

## Maintainers

- [Hangar 42](https://hangar42.de)
- [Dennis Rösner](https://rösner.de)
