---
title: Using CSS Transitions
---
## Using CSS Transitions

CSS Transitions are used to create smooth movement of the elements in a website. They require less code than CSS animations and tend to be less complex.

Transitions take an element from one CSS value to another. Here's an example:

```
.transition-me {
  width: 150px;
  height: 50px;
  background: blue;
}

.transition-me:hover {
  width: 100px;
  height: 150px;
  background: red;
}
```

![Without CSS Transition](https://i.imgur.com/Yl0Bxwn.gif)

Without a transition, this element will double in width as soon as the user hovers over it. But we might want a smoother movement. We can add a transition like so:

```
.transition-me {
  width: 150px;
  height: 50px;
  background: blue;
  transition: 0 0.3s all ease;
}
```

![With CSS Transition](https://i.imgur.com/wgscRNa.gif)

The `transition` CSS property is short-hand for several possible properties:

```
transition: transition-delay transition-duration transition-property transition-timing-function
```

### `transition-delay`
This is the time before the transition begins in seconds,
```
div {
  transition-delay: 3s;
}
```

### `transition-duration`
The duration of the transition.
```
div {
  transition-duration: 3s; // transition will take 3 seconds
}
```

### `transition-property`
This describes the CSS property which is transitioning, the default value `all` will mean that all properties that change will be transitioned. For multiple transition properties, use a comma-separated list.
```
div {
  transition-property: width, height; // transition is applied to width and height
  transition-property: all // transition is applied to all CSS properties
}
```

### `transition-timing-function`
The timing function lets us control the speed of the transition. Several keywords can be used with generic timing functions, or you can specify a [cubic bezier](https://www.w3schools.com/cssref/func_cubic-bezier.asp).
```
div {
  transition-timing-function: linear; // speed of transition remains constant
  transition-timing-function: cubic-bezier(0,0,1,1); // cubic-bezier of the same thing
}
```
For more options available in this property, check out the [W3Schools page on transition-timing-function](https://www.w3schools.com/cssref/css3_pr_transition-timing-function.asp). Also there's a handy [online cubic-bezier tool](http://cubic-bezier.com).


## More about Using CSS Transitions

* [W3 Schools CSS Transitions](https://www.w3schools.com/css/css3_transitions.asp)
* [MDN CSS Transitions Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
* [All you need to know about CSS Transitions by Alex MacCaw](https://blog.alexmaccaw.com/css-transitions)
