

## 1. Difference between `getElementById`, `getElementsByClassName`, and `querySelector` / `querySelectorAll`

- **`getElementById`** – Selects a specific element by its ID. An ID must be unique in HTML, so it always returns one element.

- **`getElementsByClassName`** – Selects all elements with a certain class. Returns an HTMLCollection (array-like).  
  To work with a single element, you can use an index (e.g., `[0]`) or loop through it using `for...of`.

- **`querySelector` / `querySelectorAll`** – Select elements using CSS selectors.  
  - `querySelector()` → Returns the first matching element.  
  - `querySelectorAll()` → Returns all matching elements as a NodeList.

---

## 1. How to create and insert a new element into the DOM?

```javascript
const div = document.createElement('div');
document.body.appendChild(div);


3.What is Event Bubbling and how does it work?
when an event starts from the targeted element and then propagates upward through its parent elements in the DOM tree - all the up to document and window calls Event Bubling,it works step-by-step.

Event goes from child → parent → document → window

4.What is Event Delegation in JavaScript? Why is it useful?
Its a pattern where attach one listener to their parent and use event bubbling to handle events for all children.many It can keep logic in one place.it saves memory by reducing the number of event listeners.

5.What is the difference between preventDefault() and stopPropagation() methods?
preventDefault() - Prevents the default browser behavior for an event.It stops the browser’s built-in action.

stopPropagation() - Stops the event from bubbling further in the DOM tree.It does not affect default browser behavior.