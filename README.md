# React Native: Accessing State Before Initialization

This repository demonstrates a common error in React Native applications where a state variable is accessed before it has been initialized. This leads to a runtime error, typically a `TypeError` or `Cannot read properties of undefined (reading '...something...')`.

## The Problem

The `bug.js` file contains a React component that attempts to render data from the state before the data has been fetched and set. This results in an error because `this.state.data` is initially `null`.

## The Solution

The `bugSolution.js` file provides a solution using conditional rendering.  This ensures that the component only renders the data once it's available.  Alternatively, the optional chaining operator (`?.`) could also be used to handle the case where the state variable is `null` or `undefined`.

## How to Run

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `react-native run-android` or `react-native run-ios` to run the app on your device or simulator.