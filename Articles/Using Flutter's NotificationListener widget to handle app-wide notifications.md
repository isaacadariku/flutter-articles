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

# Conclusion

The NotificationListener widget can be used to listen for notifications from any widget in the app, not just the widget that is a direct parent of the NotificationListener. This means that you can use the NotificationListener widget to listen for notifications from widgets that are not directly connected to the widget tree. For example, if you have a widget that is a direct child of the root widget, you can use the NotificationListener widget to listen for notifications from that widget from any other widget in the app.

Using the NotificationListener widget can be a powerful way to communicate between widgets in a Flutter app and make your code more modular and reusable. It’s a useful tool to have in your toolkit when developing Flutter apps.

If you have any questions or comments reach out to me on [Twitter](https://twitter.com/AdarikuIsaac) or please leave them below. And if you found this article useful, please share it with your friends and colleagues.

Read the full article [here](https://bit.ly/flutter-notification)
