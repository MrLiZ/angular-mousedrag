Angular Mouse Drag Directive
===========

Simple AngularJS directive for handling mouse dragging events. If you are not interested in complicated drag & drop directives and looking for a simple lightweight directive for handling mousedrag events, that's the directive for you!

## Usage

HTML:
```html
<script src="ng-mousedrag.min.js"></script>

<div ng-controller="MyCtrl">
  <div id="draggable" ng-mousedrag="onMouseDrag($event);" style="position:absolute"></div>
</div>
```

JS:
```js
angular.module('myApp', ['angularFileUpload']);
var MyCtrl = [ '$scope', function($scope) {
  $scope.onMouseDrag = function ($event) {
    var draggableObject = document.getElementById('draggable');
    draggableObject.style.top = $event.pageY;
    draggableObject.style.left = $event.pageX;
  }
}];
```
