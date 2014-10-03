fabric.ext
==========

An extension of fabricjs. Intends to implement objects and events missed in fabricjs.

###How to use

####Reference the fabric.canvasex.js in your html:
```html
<script src="scripts/fabric.canvasex.js"></script>
```

####Create a canvasex object and use it:
#####Events
```javascript
<script>
  var canvas = new fabric.CanvasEx('c');
  canvas.on('mouse:dblclick', function (options) {
    console.log('mouse:dblclick');
  });
  
  var rect = new fabric.Rect({
    left: 100,
    top: 100,
    fill: 'red',
    width: 300,
    height: 300
  });
  
  rect.on('object:dblclick', function (options) {
    console.log('object:dblclick');
  });
  
  canvas.add(rect);
</script>
```
####Supported Events and Objects:
#####Events
######canvas:
```javascript
// Double click
canvas.on('mouse:dblclick', function (options) {
});

// Mouse right button down
canvas.on('mouse:down', function (options) {
  if (options.e.which === 3) {
    console.log('Canvas right mouse down.');
  }
});
```
######object:
```javascript
// Double click
rect.on('object:dblclick', function (options) {
});

// Mouse right button down
rect.on('mousedown', function (options) {
  if (options.e.which === 3) {
    console.log('Object right mouse down.');
  }
});

```
