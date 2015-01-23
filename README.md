# Theseus module for AngularJS

[AngularJS](https://angularjs.org/) module wrapping the [Theseus](https://github.com/argo-rest/theseus) API client.

## Usage

This adapter is implemented as an ES6 module which can be installed
with [jspm](https://jspm.io) and loaded via
[SystemJS](https://github.com/systemjs/systemjs) as follows:

``` javascript
import 'theseus-angular';

import angular from 'angular';

var mod = angular.module('example', ['theseus']);

mod.factory('exampleFactory', ['theseus.client', function(client) {
  var root = client.resource('http://api.example.com');
  return root.follow('light').get();
}]);
```
