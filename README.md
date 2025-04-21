# To-Do-list
by using html created to do list
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Smart To-Do App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      padding: 20px;
    }
    .container {
      max-width: 400px;
      margin: auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
    }
    input[type="text"] {
      width: 80%;
      padding: 10px;
      margin-bottom: 10px;
    }
    button {
      padding: 10px;
      cursor: pointer;
    }
    ul {
      list-style: none;
      padding: 0;
    }
    li {
      background: #e0e0e0;
      margin: 5px 0;
      padding: 10px;
      border-radius: 5px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>📝 My To-Do List</h2>
    <input type="text" id="taskInput" placeholder="Enter a task" />
    <button onclick="addTask()">Add Task</button>
    <ul id="taskList"></ul>
  </div>

  <script>
    function addTask() {
      let taskInput = document.getElementById("taskInput");
      let taskText = taskInput.value.trim();
      if (taskText !== "") {
        let li = document.createElement("li");
        li.textContent = taskText;
        document.getElementById("taskList").appendChild(li);
        taskInput.value = "";
      }
    }
  </script>
</body>
</html>

