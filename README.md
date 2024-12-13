# React Component State Not Updating After Prop Change

This repository demonstrates a common bug in React components where the state fails to update correctly after a prop change. The issue stems from using the wrong lifecycle method (`componentDidMount` instead of `componentDidUpdate`) to handle prop updates.

## Problem

The `BuggyComponent.js` file contains a React component that attempts to update its state based on a prop value. However, it uses `componentDidMount`, which only executes once when the component mounts.  Subsequent prop changes won't trigger an update, leading to stale data being rendered.

## Solution

The `FixedComponent.js` file demonstrates the correct solution. It uses `componentDidUpdate` to detect prop changes and update the state accordingly. This ensures that the component renders the correct data even after receiving new props.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.