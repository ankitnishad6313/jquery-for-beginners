# Beginner-Friendly jQuery Notes

## jQuery Syntax

### Basic Syntax of jQuery:

```javascript
$(document).ready(function () {});

jQuery(document).ready(function () {});

// Only in body tag
$(function () {});

// In Javascript
document.getElementByTagName("h1");

// In jQuery
$("h1");

// Id Selector
document.getElementById("para");

$("#para");
```

---

## Mouse Events

1. **`click()`**: Triggered when an element is clicked.
2. **`dblclick()`**: Triggered when an element is double-clicked.
3. **`mouseover()` / **`mouseenter()`**: Triggered when the mouse pointer enters the element.
4. **`mouseout()` / **`mouseleave()`**: Triggered when the mouse pointer leaves the element.
5. **`contextmenu()`**: Triggered when the right mouse button is clicked (context menu).

---

## Keyboard Events

1. **`keypress()`**: Triggered when a key is pressed (deprecated in recent versions).
2. **`keydown()`**: Triggered when a key is pressed down.
3. **`keyup()`**: Triggered when a key is released.

---

## Get and Set Methods

1. **`html()`**: Gets or sets the HTML content of an element.
2. **`text()`**: Gets or sets the text content of an element.
3. **`val()`**: Gets or sets the value of form elements like input and select.
4. **`data()`**: Gets or sets data attributes associated with the element.
5. **`attr()`**: Gets or sets attributes of the element.

---

## Form Events

1. **`focus()`**: Triggered when an element gains focus.
2. **`blur()`**: Triggered when an element loses focus.
3. **`select()`**: Triggered when text is selected in a text field.
4. **`change()`**: Triggered when the value of an element changes.
5. **`submit()`**: Triggered when a form is submitted.
6. **`reset()`**: Triggered when a form is reset.

---

## Window Events

1. **`load()`**: Triggered when the entire page (including images) has loaded (removed in jQuery > 3).
2. **`unload()`**: Triggered when the page is unloaded (removed in jQuery > 3).
3. **`resize()`**: Triggered when the window is resized.
4. **`scroll()`**: Triggered when the window or an element is scrolled.

---

## jQuery Methods

### Visibility Methods

1. **`hide()`**: Hides the selected element.
2. **`show()`**: Shows the hidden element.
3. **`toggle()`**: Toggles between hiding and showing the element.

### Content Manipulation Methods

1. **`empty()`**: Removes all child elements from the selected element.
2. **`remove()`**: Removes the selected element itself, including its child elements.
3. **`append()`**: Inserts content at the end of the selected element.
4. **`prepend()`**: Inserts content at the beginning of the selected element.
5. **`after()`**: Adds content immediately after the selected element.
6. **`before()`**: Adds content immediately before the selected element.

### CSS Manipulation

1. **`css()`**: Gets or sets CSS properties of an element.

   **Example:**
   ```javascript
   $(".box").css("background-color", "blue");
   ```

### CSS Class Methods

1. **`addClass()`**: Adds a class to the selected element.
2. **`removeClass()`**: Removes a class from the selected element.
3. **`toggleClass()`**: Toggles a class on or off.

### Event Binding and Removal

1. **`on()`**: Attaches an event handler to the selected elements.
2. **`off()`**: Removes an event handler from the selected elements.

### Other Methods

1. **`clone()`**: Creates a copy of the selected element, including child elements and attributes.
2. **`appendTo()`**: Inserts the selected elements into another target element at the end.
3. **`prependTo()`**: Inserts the selected elements into another target element at the beginning.
4. **`wrap()`**: Wraps the selected elements inside a specified structure (e.g., `<div>`).
5. **`unwrap()`**: Removes the parent structure from the selected elements.
6. **`replaceWith()`**: Replaces the targeted elements with either HTML elements or strings.
7. **`replaceAll()`**: Replaces the targeted elements with only HTML elements.

---

## Dimensions and Position

1. **`height()`** and **`width()`**: Return the element's height and width.
2. **`innerHeight()`** and **`innerWidth()`**: Include padding.
3. **`outerHeight()`** and **`outerWidth()`**: Include padding, border, and margin.
4. **`position()`**: Returns the element's position relative to its parent.
5. **`offset()`**: Returns the element's position relative to the document.

---

## Fading Effects

1. **`fadeIn()`**: Fades the element into view.
2. **`fadeOut()`**: Fades the element out of view.
3. **`fadeToggle()`**: Toggles between fading in and out.
4. **`fadeTo()`**: Fades the element to a specific opacity.

---

## Traversal Methods

### Ancestor Methods

1. **`parents()`**: Selects all ancestor elements of the selected element.
2. **`parent()`**: Selects the immediate parent of the selected element.
3. **`parentsUntil()`**: Selects all ancestor elements up to a stopping point.
4. **`offsetParent()`**: Returns the first positioned ancestor element.
5. **`closest()`**: Selects the closest ancestor matching the selector.

### Descendant Methods

1. **`children()`**: Selects all immediate children of the selected element.
2. **`find()`**: Selects all descendant elements of the selected element.

### Sibling Methods

1. **`next()`**: Selects the immediate next sibling of the selected element.
2. **`nextAll()`**: Selects all next siblings of the selected element.
3. **`nextUntil()`**: Selects all next siblings up to a stopping point.
4. **`prev()`**: Selects the immediate previous sibling of the selected element.
5. **`prevAll()`**: Selects all previous siblings of the selected element.
6. **`prevUntil()`**: Selects all previous siblings up to a stopping point.

---

## Animation Methods

1. **`animate()`**: Performs a custom animation by changing CSS properties.

   **Example:**
   ```javascript
   $(".box").animate({
     width: "200px",
     height: "100px"
   }, "slow", function() {
     console.log("Animation complete!");
   });
   ```

2. **`stop()`**: Stops the currently running animation.

   **Example:**
   ```javascript
   $(".box").stop(true, true);
   ```

### Iteration

1. **`each()`**: Iterates over a set of elements and applies a function to each.

   **Example:**
   ```javascript
   $("li").each(function(index) {
     console.log("Item " + index + ": " + $(this).text());
   });
   ```

### Method Chaining

1. Method chaining allows multiple jQuery methods to be executed on the same element in a single statement.

   **Example:**
   ```javascript
   $(".box")
     .css("background-color", "blue")
     .fadeIn()
     .animate({ width: "300px" });
