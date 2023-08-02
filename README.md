# Flutter_doc_CokBK_GES_Handle_taps
 https://docs.flutter.dev/cookbook/gestures/handling-taps
Handle taps
===========

1.  [Cookbook](https://docs.flutter.dev/cookbook)
2.  [Gestures](https://docs.flutter.dev/cookbook/gestures)
3.  [Handle taps](https://docs.flutter.dev/cookbook/gestures/handling-taps)

You not only want to display information to users, you want users to interact with your app. Use the [`GestureDetector`](https://api.flutter.dev/flutter/widgets/GestureDetector-class.html) widget to respond to fundamental actions, such as tapping and dragging.

info Note: To learn more, watch this short Widget of the Week video on the GestureDetector widget:

This recipe shows how to make a custom button that shows a snackbar when tapped with the following steps:

1.  Create the button.
2.  Wrap it in a `GestureDetector` that an `onTap()` callback.

content_copy

```
// The GestureDetector wraps the button.
GestureDetector(
  // When the child is tapped, show a snackbar.
  onTap: () {
    const snackBar = SnackBar(content: Text('Tap'));

    ScaffoldMessenger.of(context).showSnackBar(snackBar);
  },
  // The custom button
  child: Container(
    padding: const EdgeInsets.all(12),
    decoration: BoxDecoration(
      color: Colors.lightBlue,
      borderRadius: BorderRadius.circular(8),
    ),
    child: const Text('My Button'),
  ),
)
```

[](https://docs.flutter.dev/cookbook/gestures/handling-taps#notes)Notes
-----------------------------------------------------------------------

1.  For information on adding the Material ripple effect to your button, see the [Add Material touch ripples](https://docs.flutter.dev/cookbook/gestures/ripples) recipe.
2.  Although this example creates a custom button, Flutter includes a handful of button implementations, such as: [`ElevatedButton`](https://api.flutter.dev/flutter/material/ElevatedButton-class.html), [`TextButton`](https://api.flutter.dev/flutter/material/TextButton-class.html), and [`CupertinoButton`](https://api.flutter.dev/flutter/cupertino/CupertinoButton-class.html).
