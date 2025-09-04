# Crime-record-management-system
A simple console based c++ project for managing online crime records
class Student:
    def __init__(self, student_id, name, age, room_number):
        self.student_id = student_id
        self.name = name
        self.age = age
        self.room_number = room_number

    def __str__(self):
        return f"ID: {self.student_id}, Name: {self.name}, Age: {self.age}, Room: {self.room_number}"

class online crime resource management system:
    def __init__(self):
        self.students = []

    def add_student(self, student):
        self.students.append(student)
        print(f"Student {student.name} added successfully.")

    def remove_student(self, student_id):
        for student in self.students:
            if student.student_id == student_id:
                self.students.remove(student)
                print(f"Student {student.name} removed successfully.")
                return
        print("Student not found.")

    def display_students(self):
        if not self.students:
            print("No students in the online crime resource management system.")
        else:
            print("List of students in the online crime resource management system:")
            for student in self.students:
                print(student)

    def find_student(self, student_id):
        for student in self.students:
            if student.student_id == student_id:
                return student
        return None

def main():
    hostel = online crime resource management system()
    while True:
        print("\nonline crime management system")
        print("1. Add Student")
        print("2. Remove Student")
        print("3. Display Students")
        print("4. Find Student")
        print("5. Exit")
        
        choice = input("Enter your choice: ")
        
        if choice == '1':
            student_id = input("Enter student ID: ")
            name = input("Enter student name: ")
            age = input("Enter student age: ")
            room_number = input("Enter room number: ")
            student = Student(student_id, name, age, room_number)
            hostel.add_student(student)
        
        elif choice == '2':
            student_id = input("Enter student ID to remove: ")
            hostel.remove_student(student_id)
        
        elif choice == '3':
            hostel.display_students()
        
        elif choice == '4':
            student_id = input("Enter student ID to find: ")
            student = hostel.find_student(student_id)
            if student:
                print("Student found:")
                print(student)
            else:
                print("Student not found.")
        
        elif choice == '5':
            print("Exiting the system. Goodbye!")
            break
        
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
