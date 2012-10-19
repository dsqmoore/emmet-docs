---
layout: page
title: Select Item
menuOrder: 5
---
Action is similar to [“Go to Edit Point”](/actions/go-to-edit-point/), but selects important code parts.

In HTML, these are tag name, full attribute and attribute value. For class attribute, it also selects distinct classes.

<div class="movie-def">
|&lt;section&gt;
	&lt;p&gt;&lt;/p&gt;
	&lt;div class="main footer"&gt;&lt;/div&gt;
&lt;/section&gt;
~~~
run: {command: 'emmet.select_next_item', times: 7} ::: “Select Next Item” (Cmd-.)
wait: 1000
run: {command: 'emmet.select_previous_item', times: 6} ::: “Select Previous Item” (Cmd-,)
</div>

In CSS, it matches selector, full property and property value. For complex values and functions like `1px solid red` or `url(image.jpg)` also selects part of it.

<div class="movie-def">
|body {
	border: 1px solid black;
	background: url(image.jpg) #ccc no-repeat;
}
~~~
run: {command: 'emmet.select_next_item', times: 12} ::: “Select Next Item” (Cmd-.)
wait: 1000
run: {command: 'emmet.select_previous_item', times: 11} ::: “Select Previous Item” (Cmd-,)
~~~
mode: text/css
</div>