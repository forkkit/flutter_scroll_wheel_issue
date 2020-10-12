# flutter_web_scrollwheel

Demonstrates an issue with PointerScrollEvent scrollDelta reporting differently on different browsers. 

Using a mouse with a wheel, try scrolling one notch on the listview. In Chrome it'll move a less than the white padding between items. In Firefox it will move more than the white padding.

We compensate for this in Rive by looking at the deltaMode reported by the browser, however this requires custom js code to report the value to Flutter, it would be nice if Flutter normalized this internally.