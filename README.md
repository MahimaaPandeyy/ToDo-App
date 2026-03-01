# ToDo-App
students = []  

while True:
    print("\n1. Add Student")
    print("2. View All Students")
    print("3. Search Student")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        name = input("Enter student name: ")
        roll = input("Enter roll number: ")
        marks = int(input("Enter marks: "))

       
        student = {
            "Name": name,
            "Roll No": roll,
            "Marks": marks
        }

        students.append(student)  
        print("Student added successfully!")

    elif choice == "2":
        if len(students) == 0:
            print("No student records found.")
        else:
            print("Student Records:")
            for s in students:
                print("Name:", s["Name"])
                print("Roll No:", s["Roll No"])
                print("Marks:", s["Marks"])
                print("--------------------")

    elif choice == "3":
        search_name = input("Enter student name to search: ")
        found = False

        for s in students:
            if s["Name"].lower() == search_name.lower():
                print("Student Found!")
                print("Roll No:", s["Roll No"])
                print("Marks:", s["Marks"])
                found = True
                break

        if not found:
            print("Student not found.")

    elif choice == "4":
        print("Exiting program...")
        break

    else:
        print("Invalid choice. Try again.")
