---
layout: post
title: ComboBox or Select, which one to pick?
author: AdrianVasiliu
---

As announced in this [previous post](http://ibm-js.github.io/2014/10/24/0.4.0-counting.html), 
the [deliteful](http://ibm-js.github.io/deliteful) project now includes includes a preview of
the [ComboBox](https://github.com/ibm-js/deliteful/blob/master/docs/ComboBox.md) widget. 
This short note aims to:
* Explain how the new widget complements the already
existing [Select](https://github.com/ibm-js/deliteful/blob/master/docs/Select.md) widget, and
* Provide a guidance about the criteria for choosing which of the two widgets fits better.

The `ComboBox` and `Select` widgets share a number of characteristics:
* Allow to select one or more items among a number of options (in single or multiple 
selection modes).
* Are store-based: the widget renders data provided by a data store object.
* Are form-aware: inherits from [FormWidget](https://github.com/ibm-js/delite/blob/master/docs/FormWidget.md).

On the other side, they also differ by other features, which are complementary.

`ComboBox`:
* Allows the full customization of the rendering of the options (including with 
[List](https://github.com/ibm-js/deliteful/blob/master/docs/list/List.md#categorized-items)).
* Allows the interactive filtering of the options by entering one or more characters.

All these features are (by leveraging 
[List](https://github.com/ibm-js/deliteful/blob/master/docs/list/List.md)

Finally, here is a quick guide for picking the most appropriate widget depending
on the needs of your app:
* Pick `Select` if:
  * You need text-only rendering of options, and
  * The number of options stays below a reasonable limit (from an ergonomical point of view,
  ideally not more than dozens or a few hunderds at most), and
  * You do not need to the interactive filtering capability (for a small number
  of options this feature is usually not mandatory). 
* Pick `ComboBox` if:
  * You need full customization of options (text-only is not good enough), or
  * The number of options is very high hence you need to benefit from the features
  provided by the `List` subclass 
  [PageableList](https://github.com/ibm-js/deliteful/blob/master/docs/list/PageableList.md), or
  * You need interactive filtering of the options.

