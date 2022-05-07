# honeyDo App

 A simple browser based to do app for managing ones tasks

 Technologies: HTML, CSS, JavaScript
 
 ## Add Items
 
 To store tasks, input was converted into a string and stored into the browsers memory. That way closing the window wouldn't lose your tasks.

 ![honeyDo - Add Items](https://user-images.githubusercontent.com/98543446/167230927-1cf95703-f2a1-4a9a-a652-65afdafe8911.gif)
 
 ```
 function add() {
    /* This takes the inputed task and creates a variable of it */
    var task = document.getElementById('task').value;

    var todos = get_todos();
    /* This add a new task to the end of the array */
    todos.push(task);
    /* this converts the task input to a JSON string*/
    localStorage.setItem('todo', JSON.stringify(todos));
    document.getElementById("task").value = "";
    show();
}
 ```

## Delete Items

Removing items was simple as clicking the 'x' next to items, spliced it out of Array.

![honeyDo - delete items](https://user-images.githubusercontent.com/98543446/167230943-d7c75148-74ca-4981-adb4-3608859f29c7.gif)
