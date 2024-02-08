class Task:
    def __init__(self, name):
        self.name = name
        self.completed = False

    def complete(self):1
        self.completed = True

    def __str__(self):
        return self.name


class ToDoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)

    def print_tasks(self):
        for task in self.tasks:
            print(f"{task.name} {'(completed)' if task.completed else ''}")

    def mark_complete(self, task_name):
        for task in self.tasks:
            if task.name == task_name:
                task.complete()
                break

    def remove_task(self, task_name):
        self.tasks = [task for task in self.tasks if task.name != task_name]


def main():
    to_do_list = ToDoList()

    while True:
        print("\n1. Add Task")
        print("2. Print Tasks")
        print("3. Mark Task Complete")
        print("4. Remove Task")
        print("5. Quit")

        command = input("Enter command: ")

        if command == "1":
            task_name = input("Enter task name: ")
            to_do_list.add_task(Task(task_name))
        elif command == "2":
            to_do_list.print_tasks()
        elif command == "3":
            task_name = input("Enter task name: ")
            to_do_list.mark_complete(task_name)
        elif command == "4":
            task_name = input("Enter task name: ")
            to_do_list.remove_task(task_name)
        elif command == "5":
            break
        else:
            print("Invalid command")


if __name__ == "__main__":
    main()
