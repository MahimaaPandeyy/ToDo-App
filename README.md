# ToDo-App
students = []  

tasks = [] 
def add-task():
    title = input("Title: ") 
    deadline = input("Deadline: ") 
    tasks.append([title, deadline, False]) 
    
def view-tasks(): 
   for i in range(len(tasks)): 
      status = "Done" if tasks[i] [2] else 
"Not Done" 
       print(i+1, tasks[i][0], "-", tasks[i][1], "-", status) 
       
def mark_done(): 
   view-tasks() 
   num = int(input("Task number: ")) - 1 
   tasks[num][2] = True

   
