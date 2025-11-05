# 🌐 DOM Manipulation — Beginner to Advanced

This repository documents my **complete learning journey** of mastering **DOM Manipulation in JavaScript** — from basic node selection to advanced dynamic UI creation.

I’m following a structured, project-based roadmap where each lesson includes theory, live examples, and assignments to reinforce understanding.

---

## 📘 Table of Contents

1. [About the Project](#about-the-project)
2. [What I’m Learning](#what-im-learning)
3. [Concepts Covered](#concepts-covered)
4. [Assignments & Projects](#assignments--projects)
5. [How to Practice](#how-to-practice)
6. [Learning Resources](#learning-resources)
7. [My Progress](#my-progress)
8. [License](#license)

---

## 🧠 About the Project

This repo is my **personal DOM Manipulation learning notebook**, built lesson by lesson through examples, explanations, and real projects.  
It’s designed to go from **zero → mastery** in how the browser DOM works, how to traverse, modify, and dynamically update web pages using pure JavaScript (no frameworks).

---

## 💡 What I’m Learning

- How the **Document Object Model (DOM)** represents web pages.
- Selecting, traversing, and modifying elements using JavaScript.
- Creating, inserting, and removing elements dynamically.
- Managing events and user interactions.
- Writing clean, reusable, and performant DOM code.

---

## 🧩 Concepts Covered

### 🟢 **Lesson 1 — Selecting Nodes & Reading/Writing Content**
- `getElementById`, `getElementsByClassName`, `querySelector`, `querySelectorAll`
- Working with `textContent`, `innerText`, and `innerHTML`
- Reading/writing attributes and dataset values
- ⚡ Assignment: Shuffle the text content of list items

### 🟡 **Lesson 2 — Creating, Inserting & Removing Elements**
- `createElement`, `append`, `prepend`, `insertBefore`, `replaceWith`, `remove`
- Difference between `innerHTML` and Node-based operations
- Using `DocumentFragment` for batching
- ⚡ Assignment: Dynamic Tag Creator — add/remove interactive tags
- Event delegation for efficient event handling

### 🟠 **Upcoming Lessons**
- DOM Traversal & Forms (`parentElement`, `children`, `nextElementSibling`)
- Event Handling Deep Dive (delegation, bubbling, capturing)
- Custom Events, Throttling, and Debouncing
- Component Patterns (creating reusable DOM widgets)
- Performance Optimization & Accessibility (ARIA roles, reflows)
- DOM Testing (with Jest + jsdom)

---

## 🧮 Assignments & Projects

| # | Lesson | Assignment | Key Concepts |
|---|---------|-------------|---------------|
| 1 | Selecting Nodes | Shuffle text of a list | DOM selection, `querySelectorAll`, Fisher–Yates shuffle |
| 2 | Creating Elements | Dynamic Tag Creator | `createElement`, `append`, `remove`, Event Delegation |
| 3 | Traversal | Highlight parent-child paths | DOM tree traversal |
| 4 | Forms | Signup with validation | Form validation API |
| 5 | Events | Todo list with delegation | Bubbling, event handling |
| 6 | Performance | 1000-node render test | DocumentFragment, reflows |

---

## 🧰 How to Practice

1. Use **VS Code** with **Live Server** extension to test each `.html` file.  
2. Create a new folder for each lesson:  
3. For each lesson:
- Read the concepts section.
- Recreate the code examples manually.
- Complete the assignment.
- Write short notes about what you learned.

---

## 📚 Learning Resources

- **MDN Web Docs** — [DOM API Reference](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)
- **JavaScript.info** — [DOM Manipulation Guide](https://javascript.info/dom-nodes)
- **freeCodeCamp** — [Manipulating the DOM](https://www.freecodecamp.org/learn)
- Chrome DevTools — Elements Panel & Event Breakpoints
- My AI mentor (ChatGPT) — used for interactive lessons, code reviews, and deep explanations

---

## 🚀 My Progress

| Date | Topic | Status |
|------|--------|--------|
| ✅ | Lesson 1: DOM Selection | Completed |
| ✅ | Lesson 2: Creating & Inserting Elements | Completed |
| 🔜 | Lesson 3: DOM Traversal | In Progress |
| ⏳ | Lesson 4–5: Events & Forms | Coming Soon |

---

## 🧑‍💻 Example Code Snippet

```js
// Example: Shuffle list text content
const listItems = document.querySelectorAll("#itemList li");
const button = document.getElementById("shuffleBtn");

function shuffleArray(arr) {
for (let i = arr.length - 1; i > 0; i--) {
 const j = Math.floor(Math.random() * (i + 1));
 [arr[i], arr[j]] = [arr[j], arr[i]];
}
return arr;
}

button.addEventListener("click", () => {
const texts = Array.from(listItems).map(li => li.textContent);
const shuffled = shuffleArray(texts);
listItems.forEach((li, i) => li.textContent = shuffled[i]);
});
