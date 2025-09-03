# Ex04 Simple Calculator - React Project
## Date:03.09.2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM

### Calculator.jsx
```
import React, { useState } from 'react';
import './Calculator.css';
const Calculator = () => {
  const [input, setInput] = useState('');
  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };
  const handleClear = () => setInput('');
  const handleEqual = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput('Error');
    }
  };
  return (
    <div className="calculator">
      <input type="text" value={input} readOnly />
      <div className="buttons">
        {['7','8','9','/','4','5','6','*','1','2','3','-','0','.','=','+'].map((btn) =>
          btn === '='
            ? <button key={btn} onClick={handleEqual}>{btn}</button>
            : <button key={btn} onClick={() => handleClick(btn)}>{btn}</button>
        )}
        <button className="clear" onClick={handleClear}>C</button>
      </div>
    </div>
  );
};
export default Calculator;
```

### Calculator.css
```
body, html {
  height: 100%;
  margin: 0;
  background-color: #222; 
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.calculator {
  background: #fff;
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.3);
  width: 280px;
}
.calculator input {
  width: 100%;
  height: 60px;
  font-size: 24px;
  text-align: right;
  border-radius: 8px;
  border: 1px solid #ccc;
  margin-bottom: 20px;
  padding: 10px;
  box-sizing: border-box;
  background-color: #333;
  color: white;
  font-weight: bold;
}
.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
}
.buttons button {
  height: 60px;
  font-size: 20px;
  border: none;
  border-radius: 10px;
  background-color: #f0f0f0;
  color: #333;
  cursor: pointer;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: background-color 0.2s ease;
}
.buttons button:hover {
  background-color: #ddd;
}
button.clear {
  grid-column: span 4;
  background-color: #ff4b4b;
  color: white;
  font-weight: bold;
  box-shadow: 0 2px 6px rgba(255, 75, 75, 0.5);
}
button.clear:hover {
  background-color: #e03e3e;
}
```

### App.jsx
```
import React from 'react';
import Calculator from './Calculator';
import './App.css'; 
function App() {
  return (
    <div className="App">
      <h1 style={{ textAlign: 'center' }}>Simple Calculator</h1>
      <Calculator />
      <footer className="footer">
        <p>© 2025 Dharunyadevi S. All rights reserved.</p>
      </footer>
    </div>
  );
}
export default App;
```

### App.css
```
.App {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  align-items: center;
  background-color: #222; 
  color: white;
  padding: 20px;
  box-sizing: border-box;
}
.footer {
  margin-top: auto;
  padding: 10px 0;
  font-size: 0.9rem;
  color: #aaa;
  text-align: center;
  width: 100%;
}
```

## OUTPUT

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6759c88b-1e69-47e4-aa05-32eebc969909" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/62ea5b1c-bab7-490f-b53a-0c0dc5e29917" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0f6c0293-74b9-431d-900d-39790aeecd70" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
