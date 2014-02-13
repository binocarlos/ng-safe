ng-safe
=======

angular $scope safe apply as a component

## installation

```
$ component install binocarlos/ng-safe
```

## usage

```js
angular.module('myApp', [
	require('ng-safe')
])

.controller('MyAppCtrl', function($scope, $safeApply){

	// run some code outside angular scope
	// safely inject it without triggering 'digest already in progress' errors
	run_external_code(function(return_value){

		$safeApply($scope, function(){
			$scope.return_value = return_value;
		})

	})
})

```

## $safeApply($scope, fn)

This is returned as a factory into your controller.  Pass the scope and a function that will write values to that scope.



## license

MIT