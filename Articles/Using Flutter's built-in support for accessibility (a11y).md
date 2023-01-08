# Using Flutter's built-in support for accessibility (a11y)

One of the key features of Flutter is its built-in support for accessibility or “a11y” for short. In this article, we will discuss what a11y is, how to use Flutter’s built-in support for it to create mobile apps that are more accessible to users with disabilities, and lastly introduce a tool to check and improve a11y to your Flutter app.

## What is accessibility (a11y)?

Accessibility, or a11y, refers to the design of digital products, such as websites or mobile apps, to be usable by people with disabilities. This includes individuals with visual, auditory, physical, cognitive, or neurological disabilities.

There are several ways in which a digital product can be made more accessible. These include:

- Providing alternative text for images and other non-text content
- Ensuring that the product can be used with a keyboard or other assistive technologies
- Using color contrast ratios to make text and other content more readable
- Providing captions or transcripts for audio and video content
- Allowing users to adjust font sizes and other visual settings

## Why is a11y important?

Accessibility is important because it allows people with disabilities to use digital products. This includes people who are blind or have low vision, people who are deaf or have hearing loss, people who have difficulty using their hands, people who have difficulty reading, and people who have difficulty concentrating or remembering.

According to the [World Health Organization](https://www.who.int/teams/noncommunicable-diseases/sensory-functions-disability-and-rehabilitation/world-report-on-disability), 15% of the world’s population has some form of disability. This means that 1 billion people in the world have a disability. So it is important to make digital products accessible to this large group of people.

This not only helps to ensure that these individuals have equal access to information and services, but it also makes the product more usable for everyone. For example, if you make your product accessible to people who are blind, you will also make it more usable for people who are using their mobile devices in bright sunlight. And if you make your product accessible to people who have difficulty using their hands, you will also make it more usable for people who are using their mobile devices while driving.

## How does Flutter support a11y?

Flutter supports accessibility by providing a set of built-in widgets and other tools that make it easier to create accessible mobile apps. These include:

The Semantics widget, which allows developers to specify alternative text for images and other non-text content
The Focus widget, which allows developers to specify which elements in the app should be focusable and how they should respond when they receive focus
The ExcludeSemantics widget, which allows developers to exclude specific elements from the semantics tree
The Accessibility widget, which allows developers to specify additional accessibility properties for an element, such as the label, value, and description

How to use Flutter's built-in support for accessibility

- The **Semantics widget**, which allows developers to specify alternative text for images and other non-text content.

- The **Focus widget**, which allows developers to specify which elements in the app should be focusable and how they should respond when they receive focus.

- The **ExcludeSemantics widget**, which allows developers to exclude specific elements from the semantics tree
  Example: Creating an accessible button.

### How to use Flutter’s built-in support for accessibility

Using Flutter’s built-in support for accessibility is easy, developers can easily create mobile apps that are more accessible to users with disabilities.

_Example: Creating an accessible button_

In this example, we create an accessible button that can be used to increase the font size of the text in an app. We use the Semantics widget to specify alternative text for the button, and the Focus widget to specify that the button should be focusable and how it should respond when it receives focus.

Check out this DartPad: https://dartpad.dev/?id=df3346c83644ac78562748ea4afe3206

The dart pad code above creates a button that can be used to increase the font size of the text widget. The button is created using the Focus widget. The Focus widget allows developers to specify which elements in the app should be focusable and how they should respond when they receive focus. We have specified that the button should be focusable and how it should respond when it receives focus. When the button receives focus, it will increase the font size of the text widget by 2.0.

We have specified that the Semantics widget button should have the label “Increase font size”. This label will be used by assistive technologies, such as screen readers, to describe the button to users.

_Example: Creating an accessible image_

In this example, we create an accessible image that can be used to display a logo. We will use the Semantics widget to specify alternative text for the image, and the ExcludeSemantics widget to exclude the image from the semantics tree.

Check out this DartPad: https://dartpad.dev/?id=a8bacadc5c1e8e767253a48f7f03705d

The dart pad code above creates an accessible image that can be used to display a logo. The image is created using the FlutterLogo widget. The FlutterLogo widget is a built-in widget that displays the Flutter logo. We have specified that the image should have the label “Flutter logo”. This label will be used by assistive technologies, such as screen readers, to describe the image to users.

We have specified that the image should be excluded from the semantics tree. This means that the image will not be included in the semantics tree, and therefore it will not be described by assistive technologies, such as screen readers.

## Adding a tool to check and improve a11y to your Flutter app

[RebelAppStudio](https://rebelappstudio.com/) has created a tool that can be used to check and improve the accessibility of your Flutter app. The tool is called [accessibility_tools](https://pub.dev/packages/accessibility_tools), and it is available as a [Flutter package](https://twitter.com/RebelAppStudio/status/1605938025426452480). The tool can be used to check the accessibility of your app, and it can also be used to automatically fix some of the accessibility issues that are found.

RebelAppStudio made the tool easy to use and can be added to your Flutter app in just a few steps following the instructions on the package’s README page.

It was discussed at #flutterVikings and this is a must-have package for flutter developers. — Tim Sneath
