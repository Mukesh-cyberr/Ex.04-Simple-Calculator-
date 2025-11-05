# Ex04 Simple Calculator - React Project
## Date:05-11-2025

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
app.jsx
```
// App.jsx
import React, { useState } from 'react';
import './App.css';

function App() {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    if (value === '=') {
      try {
        setInput(eval(input).toString());
      } catch {
        setInput('Error');
      }
    } else if (value === 'C') {
      setInput('');
    } else {
      setInput(input + value);
    }
  };

  return (
    <div className="calculator">
      <h2>Simple React Calculator</h2>
      <input type="text" value={input} readOnly />
      <div className="buttons">
        {['7','8','9','/','4','5','6','*','1','2','3','-','0','.','=','+','C'].map((btn) => (
          <button key={btn} onClick={() => handleClick(btn)}>{btn}</button>
        ))}
      </div>

      <footer>
        <p>Developed by <b>Your Name</b> | Reg. No: <b>Your Register Number</b></p>
      </footer>
    </div>
  );
}

export default App;

```
app.css
```.calculator {
  width: 250px;
  margin: 80px auto;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
  text-align: center;
}

input {
  width: 90%;
  padding: 10px;
  margin-bottom: 10px;
  font-size: 1.2em;
  text-align: right;
}

.buttons button {
  width: 50px;
  height: 50px;
  margin: 5px;
  font-size: 1.1em;
  border-radius: 10px;
  cursor: pointer;
}

footer {
  margin-top: 20px;
  font-size: 0.9em;
  color: #555;
}


```

## OUTPUT
<img width="1920" height="1020" alt="Screenshot 2025-11-05 051857" src="https://github.com/user-attachments/assets/ec060b0d-fc05-452c-9358-00bb883afd26" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
