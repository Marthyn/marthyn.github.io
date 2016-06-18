---
layout: post
title:  "Property or Observes? EmberJS Explained"
date:   2014-04-06
excerpt: "While programming for Learning Spaces I had a lot of trouble choosing when to use `.property(‘property to observe’)` or `.observes(‘property to observe’)`"
tag:
- ember
- javascript
- emberjs
comments: true
---

While programming for Learning Spaces I had a lot of trouble choosing when to use `.property(‘property to observe’)` or `.observes(‘property to observe’)`

They behave the same, as in they run whenever the property between the `’ ‘ ` changes. But there’s a difference and you should know that difference.

Basically when you only manipulate other things you need `observes` and if you return something which you need later you need to use `property`

So let’s say you have a BookController with some properties.

```
App.BookController = Ember.ObjectController.extend({
 setPage: function() {
 var pageNumber = this.get(‘pageNumber’);
 this.set(‘page’, this.store.find(‘page’, pageNumber));
 }.observes(‘pageNumber’),

 footNotes = function() {
 return this.get(‘page.footNotes’)
 }.property(‘page’),

 copyright = function() {
 return ‘(c) Marthyn Olthof — Learning Spaces’;
 }.property(),
});


setPage: function () {
 var pageNumber = this.get(‘pageNumber’);
 this.set(‘page’, this.store.find(‘page’, pageNumber));
}.observes(‘pageNumber’),
```


This is a function which sets the page property, but it doesn’t return anything. Therefor we can just use the ```observes(‘pageNumber’)```. Which runs every time the property ```pageNumber``` changes. But it’s impossible to bind this to a view!

```
footNotes = function () {
 return this.get(‘page.footNotes’);
}.property(‘page’),
```

Here `footNotes` is a property which returns the footnotes of a page. To update this property everytime the page changes and bind it to a view. We use `property(‘page’)` with a binding to the property `page`. So everytime the page property changes the footnotes change too. Also you can now bind this to your view as such `{{footNotes}}`

```
copyright = function() {
 return ‘(c) Marthyn Olthof — Learning Spaces’;
}.property(),
```


Finally we have a property which doesn’t change at all. Therefor we use `property()` without any binding. We can bind this to a view with {{copyright}} and it will not change unless the controller is initialized again.

For review, here is a table:

![table](https://cdn-images-1.medium.com/max/1600/1*a--CwXE1k8H1LEvfQ9E-rA.png)    
