What is event bubbling in JavaScript?

Be sure to touch on:

- Generally speaking, how does it work? 
- which events bubble?
- `event.target` vs `this`
- How can you stop a bubbling event?

---

When an event happens on an element, it first runs the event handlers on the element, then on the element's parent, then on its parent, and on up through all the ancestors.

For instance:
```html
<form onclick="alert('form')">FORM
  <div onclick="alert('div')">DIV
    <p onclick="alert('p')">P</p>
  </div>
</form>
```

Clicking on the innermost `<p>P</p>` element would cause 3 different alerts to show: "p", "div", and "form" as the event bubbles up to all the parent elements.

Not all events bubble, but most do. The `focus` event is an example of one that does not bubble.

Within an event handler, `event.target` refers to the original element that caused the event, and `this` refers to the "current" element.

The primary method to stop bubbling is `event.stopPropagation()`. 
