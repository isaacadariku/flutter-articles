Using Flutter's NotificationListener widget to handle app-wide notifications

Flutter’s NotificationListener widget allows developers to create app-wide notifications that can be handled by widgets throughout the app. This can be useful for situations where a change in one part of the app needs to trigger a change in another part, or for communicating between widgets that are not directly connected in the widget tree.

To use the [NotificationListener](https://api.flutter.dev/flutter/widgets/NotificationListener-class.html) widget, you first need to create a subclass of the Notification class. This subclass should contain any data that you want to pass through the notification. For example:

```
class MyNotification extends Notification {
  final String message;

  MyNotification(this.message);
}
```

Next, you can create a widget that listens for this specific notification using the NotificationListener widget. Inside the NotificationListener, you can specify a callback function that will be triggered when the notification is received. This callback function should take in a BuildContext and the notification object as arguments:

```
NotificationListener<MyNotification>(
  onNotification: (notification) {
    // Handle the notification here
  },
  child: ..., // The widget that will receive the notification
)
```

To send a notification, you can use the [dispatch method](https://api.flutter.dev/flutter/widgets/Notification/dispatch.html) on the BuildContext object. This method takes in the notification object as an argument:

```
context.dispatchNotification(MyNotification('Hello'));
```

If we print the message from the notification in the callback function, we should see the following output on the console:

```
Notification received: Hello
```

You can find the full source code for this example on DartPad:

[Run the demo](https://dartpad.dev/?id=a224a222605834cdc86b672ca0b5b866)
