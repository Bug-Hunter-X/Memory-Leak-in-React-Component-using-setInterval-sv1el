# React setInterval Memory Leak
This repository demonstrates a common mistake in React: using setInterval within useEffect without proper cleanup. This leads to a memory leak because the interval continues to run even after the component unmounts.

## Bug
The `bug.js` file contains a React component that uses setInterval to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## Solution
The `bugSolution.js` file provides a corrected version of the component. It uses the return function from useEffect to clear the interval before the component unmounts, preventing the memory leak.

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and go to `http://localhost:3000`.
5. Observe the counter increasing.
6. Navigate away from the page or refresh it. You can see the leak in the browser's developer tools.