# Simple-to-do-list
tasks = []

def add_task(task):
    tasks.append(task)

def show_tasks():
    for i, task in enumerate(tasks, 1):
        print(f"{i}. {task}")

if __name__ == "__main__":
    while True:
        action = input("Add / Show / Quit: ").lower()
        if action == 'add':
            task = input("Enter task: ")
            add_task(task)
        elif action == 'show':
            show_tasks()
        elif action == 'quit':
            break
        else:
            print("Unknown action")
