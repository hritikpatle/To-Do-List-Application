# To-Do-List-Application
Task Class: Represents a task with attributes such as description, due date, and completion status.

ToDoList Class: Manages a list of tasks, allowing users to add tasks and display them.

Usage
Create an instance of the ToDoList class.
Add tasks using the add_task method.
Display tasks using the display_tasks method.
The application provides a basic command-line interface with options to add tasks, display tasks, and quit the program.
class Task:
    def __init__(self,description,due_date):
        self.description = description
        self.due_date  = due_date
        self.completed = False
        
class ToDoList:
    def __init__(self):
        self.tasks = []
        
    def add_task(self,task):
        self.tasks.append(task)
    def display_task(self):
        for index, task in enumerate(self,task, start=1):
            status = "Done" if task>completed else "Not Done"
            print(f"{index}. {task.description} (Due:{task.due_date}) - {status}")
todo_list = ToDoList()

while True:
    print("\n1.Add Task\n2.Display Task\n3. Quit")
    choice = input("Enter your choice(1/2/3):")
    
    if choice == "1":
        description = input("Enter task description:")
        due_date = input("Enter due date:")
        task = Task(description, due_date)
        todo_list.add_task(task)
    elif choice == "2":
        todo_list.display_tasks()
    elif choice == "3":
        break
    else:
        print("Invalid choice.Please try again.")
            
