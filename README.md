### TO-DO-LIST:

### HTML:
```
<!DOCTYPE html>
<html lang="en">
    <link rel="stylesheet" href="do.css">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>To-Do List</h1>
        <input type="text" id="taskInput" placeholder="Enter a new task">
        <button id="addTaskBtn">Add Task</button>
        <ul id="taskList"></ul>
    </div>
    <script src="todo.js"></script>
</body>
</html>
```
### CSS:
```
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 300px;
    text-align: center;
}

h1 {
    margin-bottom: 20px;
}

input {
    width: calc(100% - 22px);
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    width: 100%;
    padding: 10px;
    background-color: #28a745;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #218838;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    background-color: #f4f4f4;
    margin: 5px 0;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

li button {
    background-color: #dc3545;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    padding: 5px 10px;
}

li button:hover {
    background-color: #c82333;
}
```
### JAVASCRIPT:
```
document.getElementById('addTaskBtn').addEventListener('click', function() {
    const taskInput = document.getElementById('taskInput');
    const taskText = taskInput.value.trim();
    
    if (taskText === '') {
        alert('Please enter a task');
        return;
    }

    addTaskToList(taskText);
    taskInput.value = '';
});

function addTaskToList(taskText) {
    const taskList = document.getElementById('taskList');
    const taskItem = document.createElement('li');

    taskItem.textContent = taskText;

    const deleteBtn = document.createElement('button');
    deleteBtn.textContent = 'Delete';
    deleteBtn.addEventListener('click', function() {
        taskList.removeChild(taskItem);
    });

    taskItem.appendChild(deleteBtn);
    taskList.appendChild(taskItem);
}
```
###  OUTPUT:
![Screenshot (16)](https://github.com/chandruiyappan/To-do-list/assets/123877158/adf18e3e-1d20-407a-bef0-82431cced6db)
![Screenshot (17)](https://github.com/chandruiyappan/To-do-list/assets/123877158/53986503-d7a6-4bc9-aba2-0f58ca82bac6)
