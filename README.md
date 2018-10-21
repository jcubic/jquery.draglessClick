# jquery.draglessClick

Better jQuery click event that's not invoked when you drag or select text

[![npm](https://img.shields.io/badge/npm-1.0.0-blue.svg)](https://www.npmjs.com/package/jquery-dragless-click)
![bower](https://img.shields.io/badge/bower-1.0.0-yellow.svg)

## Usage:

```javascript
$(function() {
    $('p').on('draglessClick', function handler(e) {
        // e is real click event from browser
        alert("You've really clicked this item");
        $(this).off('draglessClick', handler);
    });
    $('.container').on('draglessClick', 'ul li', function() {
       alert("You've clicked on li element");
    });
});
```

`draglessClick` event use mousedown, mouseup and click events added to element and mousemove added to windows object.

NOTE: names of the events in jQuery are case sensitive so draglessclick will not work.

## Demo

https://codepen.io/jcubic/pen/QZxRLd

## License

Released under [MIT](https://github.com/jcubic/jquery.draglessClick/blob/master/LICENSE) license
Copyright (c) 2018 [Jakub Jankiewicz](https://jcubic.pl/me)
