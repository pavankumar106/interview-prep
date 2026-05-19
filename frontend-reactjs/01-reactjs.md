## 1. What is React and why is it efficient?

    React is a JavaScript library used for building user interfaces,
    especially single-page applications. It allows developers to
    create reusable UI components and manage application state
    efficiently.

    React is considered efficient mainly because of the Virtual DOM.
    Instead of updating the real DOM directly whenever data changes,
    React creates a virtual copy of the DOM, compares the changes
    using a diffing algorithm, and updates only the modified parts in
    the real DOM. This reduces unnecessary DOM manipulations and
    improves performance.

    Another reason React is efficient is its component-based
    architecture, which promotes code reusability, maintainability,
    and easier debugging. React also supports one-way data binding,
    making data flow predictable and easier to manage in large
    applications.

## 2. How does React work internally?

    React works internally using a component-based architecture
    and a Virtual DOM mechanism.

    When a React application is rendered, React creates a Virtual
    DOM, which is a lightweight JavaScript representation of the real
    DOM. Whenever the state or props of a component change, React
    creates a new Virtual DOM tree and compares it with the previous
    one using a process called reconciliation.

    React uses a diffing algorithm to identify the exact changes
    between the old and new Virtual DOM. Instead of updating the
    entire real DOM, React updates only the changed elements. This
    process improves performance because real DOM operations are
    expensive.

    React components follow a unidirectional data flow, where data
    moves from parent to child components through props. State
    changes trigger re-rendering of affected components.

    Internally, React also uses Fiber architecture, which helps React
    prioritize updates, pause rendering work, and improve
    responsiveness for complex applications.

## 3. explain Virtual DOM in react and how it improves performance

    React uses a Virtual DOM, which is a lightweight JavaScript representation of the real DOM. When state changes, React creates a new Virtual DOM tree and compares it with the previous one using a diffing algorithm. It identifies only the changed elements and updates only those parts in the real DOM. This minimizes expensive DOM operations and improves rendering performance.

    Updating the real DOM is expensive because:
    - Browser must recalculate layout
    - Repaint UI
    - Reflow elements
    - Re-render affected nodes

    How VDOM Works
    - Initial render → React creates Virtual DOM
    - State changes
    - React creates a new Virtual DOM
    - React compares old vs new VDOM
    - Finds only changed nodes
    - Updates only those parts in real DOM

    This comparison process is called: Reconciliation
