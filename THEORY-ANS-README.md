
## **1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?**

- **getElementById** – It selects specifically one element by its ID. The ID must be unique in HTML, so it's easy to select.  
- **getElementsByClassName** – It selects all elements with a certain class. It behaves like an array. To select a single element, use an index (e.g., `[0]`) or a loop.  
- **querySelector / querySelectorAll** – These select elements using CSS selectors.  
  - `querySelector()` → selects the first matching element.  
  - `querySelectorAll()` → selects all matching elements as a NodeList.  

---

## **2. How do you create and insert a new element into the DOM?**

- You create an element using `document.createElement(tagName)`.  
- Insert it into the DOM using `appendChild()` or similar methods.  
- You can also set `innerText` or other properties before inserting.  

Example (conceptual, not code block for GitHub PDF-style view):  
- Create a div element  
- Append it to the body  

---

## **3. What is Event Bubbling and how does it work?**

- Event Bubbling is when an event starts from the targeted element and propagates upward through its parent elements, up to the document and window.  
- Flow: **Child → Parent → Document → Window**

---

## **4. What is Event Delegation in JavaScript? Why is it useful?**

- Event Delegation is a pattern where you attach **one listener to a parent element** and use event bubbling to handle events for all child elements.  

**Benefits:**  
- Saves memory by reducing the number of event listeners  
- Keeps logic in one place  
- Works even for dynamically added elements  

---

## **5. What is the difference between preventDefault() and stopPropagation() methods?**

- **preventDefault()** – Prevents the default browser behavior for an event. It stops the browser’s built-in action.  
- **stopPropagation()** – Stops the event from bubbling further in the DOM tree. It does not affect default browser behavior.  
