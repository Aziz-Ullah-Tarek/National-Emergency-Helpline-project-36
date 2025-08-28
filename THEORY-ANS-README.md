# JavaScript DOM & Events – Theory Notes

## 1. Difference between `getElementById`, `getElementsByClassName`, and `querySelector` / `querySelectorAll`

- **`getElementById`** – Selects a specific element by its ID. An ID must be unique in HTML, so it always returns one element.

- **`getElementsByClassName`** – Selects all elements with a certain class. Returns an HTMLCollection (array-like).  
  To work with a single element, you can use an index (e.g., `[0]`) or loop through it using `for...of`.

- **`querySelector` / `querySelectorAll`** – Select elements using CSS selectors.  
  - `querySelector()` → Returns the first matching element.  
  - `querySelectorAll()` → Returns all matching elements as a NodeList.

---

## 2. How to create and insert a new element into the DOM?

```javascript
const div = document.createElement('div');
document.body.appendChild(div);

3. What is Event Bubbling and how does it work?

Event bubbling is when an event starts from the target element and propagates upward through its parent elements, then the document, and finally the window.

Flow: Child → Parent → Document → Window

4. What is Event Delegation in JavaScript? Why is it useful?

Event delegation is a pattern where a single event listener is attached to a parent element and uses event bubbling to handle events on its child elements.

Benefits:

Keeps logic in one place

Saves memory by reducing the number of event listeners

Works with dynamically added elements

5. Difference between preventDefault() and stopPropagation()

preventDefault() – Prevents the default browser behavior (e.g., prevent form submission or link navigation).

stopPropagation() – Stops the event from bubbling up the DOM tree, but does not prevent default behavior.