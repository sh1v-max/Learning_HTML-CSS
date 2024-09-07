# CSS Media Types
====================================

CSS Media Types are used to apply different styles based on different types of devices or screen sizes. They allow you to create responsive designs that adapt to different devices such as desktops, laptops, tablets, and mobile phones.

### Common Media Types

The most common media types used are:

* `all`: Applies to all devices.
* `screen`: Applies to computer screens.
* `print`: Applies to printed documents.
* `speech`: Applies to speech synthesizers.

### Media Queries

Media queries are used to apply different styles based on different devices or screen sizes. They consist of a media type and one or more expressions that check for the conditions of a particular media feature.

The syntax of a media query is `@media <media-type> <media-feature> { /* CSS rules */ }`.

The most commonly used media features are:

* `max-width` and `min-width`: To apply styles based on the maximum or minimum width of the screen.
* `max-height` and `min-height`: To apply styles based on the maximum or minimum height of the screen.
* `orientation`: To apply styles based on the orientation of the device.

Example of a media query using `max-width`:

