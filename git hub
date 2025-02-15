#include <iostream>
#include <vector>
#include <string>

using namespace std;

struct Task
{
    string description;
    bool completed;
};

void addTask(vector<Task> &tasks);
void viewTasks(const vector<Task> &tasks);
void markTaskCompleted(vector<Task> &tasks);

int main()
{
    vector<Task> tasks;
    int choice;

    while (true)
    {
        cout << "\nToDo App\n";
        cout << "1. Add Task\n";
        cout << "2. View Tasks\n";
        cout << "3. Mark Task Completed\n";
        cout << "4. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice)
        {
        case 1:
            addTask(tasks);
            break;
        case 2:
            viewTasks(tasks);
            break;
        case 3:
            markTaskCompleted(tasks);
            break;
        case 4:
            cout << "Exiting...\n";
            return 0;
        default:
            cout << "Invalid choice. Please try again.\n";
        }
    }

    return 0;
}

void addTask(vector<Task> &tasks)
{
    Task newTask;
    cout << "Enter task description: ";
    cin.ignore();
    getline(cin, newTask.description);
    newTask.completed = false;
    tasks.push_back(newTask);
    cout << "Task added successfully!\n";
}

void viewTasks(const vector<Task> &tasks)
{
    if (tasks.empty())
    {
        cout << "No tasks available.\n";
    }
    else
    {
        for (size_t i = 0; i < tasks.size(); ++i)
        {
            cout << i + 1 << ". " << tasks[i].description;
            if (tasks[i].completed)
            {
                cout << " [Completed]";
            }
            cout << endl;
        }
    }
}

void markTaskCompleted(vector<Task> &tasks)
{
    int taskNumber;
    cout << "Enter task number to mark as completed: ";
    cin >> taskNumber;

    if (taskNumber > 0 && taskNumber <= tasks.size())
    {
        tasks[taskNumber - 1].completed = true;
        cout << "Task marked as completed!\n";
    }
    else
    {
        cout << "Invalid task number. Please try again.\n";
    }
}