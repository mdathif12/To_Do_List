# Ex03 To-Do List using JavaScript
## Date:18/03/2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
   
    <title>Todo Application</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f0f8ff;
            color: #333;
        }
        header, footer {
            text-align: center;
            padding: 15px;
            background-color: #4caf50;
            color: white;
            border-radius: 8px;
        }
        .todo-container {
            max-width: 400px;
            margin: 20px auto;
            padding: 20px;
            background-color: #ffffff;
            border: 2px solid #4caf50;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .todo-input {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 2px solid #4caf50;
            border-radius: 4px;
        }
        .todo-list {
            list-style: none;
            padding: 0;
        }
        .todo-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px;
            margin-bottom: 5px;
            background-color: #f9f9f9;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .todo-item.completed {
            text-decoration: line-through;
            color: gray;
        }
        .todo-buttons button {
            padding: 5px 10px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .todo-buttons button:first-child {
            background-color: #4caf50;
            color: white;
        }
        .todo-buttons button:last-child {
            background-color: #f44336;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>Todo Application</h1>
    </header>

    <div class="todo-container">
        <h2>Manage Your Tasks</h2>
        <input type="text" id="todo-input" class="todo-input" placeholder="Add a new task">
        <ul id="todo-list" class="todo-list"></ul>
    </div>

    <footer>
        <p>&copy; @CopyRight 2025. All rights reserved.212223220058</p>
    </footer>

    <script>
        const todoInput = document.getElementById('todo-input');
        const todoList = document.getElementById('todo-list');

        function addTodo() {
            const task = todoInput.value.trim();
            if (task === '') return;

            const li = document.createElement('li');
            li.className = 'todo-item';

            const span = document.createElement('span');
            span.textContent = task;

            const buttonsDiv = document.createElement('div');
            buttonsDiv.className = 'todo-buttons';

            const completeBtn = document.createElement('button');
            completeBtn.textContent = 'Complete';
            completeBtn.onclick = () => {
                li.classList.toggle('completed');
            };

            const deleteBtn = document.createElement('button');
            deleteBtn.textContent = 'Delete';
            deleteBtn.onclick = () => {
                todoList.removeChild(li);
            };

            buttonsDiv.appendChild(completeBtn);
            buttonsDiv.appendChild(deleteBtn);

            li.appendChild(span);
            li.appendChild(buttonsDiv);

            todoList.appendChild(li);
            todoInput.value = '';
        }

        todoInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                addTodo();
            }
        });
    </script>
</body>
</html>
```


## OUTPUT
![Screenshot 2025-03-18 132425](https://github.com/user-attachments/assets/2bbe75d2-cd54-4593-98ad-8da567e1d136)

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
