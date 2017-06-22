# bakers-dozen Style Guide

This is the style guide for use the the bakers-dozen semester project.

## Filenames

Filenames for components should follow these guidelines.  Note some files you cannot change (bower.json, manifest.json, etc.)

* Filenames for components should be in lisp-case. Similar to snake_case but using a "-" instead of "\_".
* Component filenames should be in all lowercase.

## Classes

These guidlines should be followed when creating a JavaScript Classes

* Class names should be in `PascalCase` or `UpperCamelCase` format.
* Class names should be descriptive of the component that is being created.

## Methods

Methods within classes should conform to the following:

* Method names should be in `lowerCamelCase` format.
* Method names should be descriptive of what their function is.
* JavaScript does not have "private" methods but for methods intended for private, internal use, prefix their name with an underscore. Any methods whose name does not begin with an underscore is understood to be part of the class's supported public API. If you must call a "private" method from outside an object consider this a code smell.

## Properties/Variables

Properties of objects should follow the following standards

* Properties should be in `lowerCamelCase`.
* Make the property name descriptive of what it represents.
* Tend to add JSDoc-style comments on the line above them for easy documentation generation.

## Anonymous Functions

Follow these guidelines for creating functions:

* If a function will be used in more than one area attempt to steer away from using an anonymous function.
