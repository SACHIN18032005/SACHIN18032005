Student management system 

class Student:
    def __init__(self, roll_no, name, age, course):
        self.roll_no = roll_no
        self.name = name
        self.age = age
        self.course = course

class StudentManagementSystem:
    def __init__(self):
        self.students = []

    def add_student(self, roll_no, name, age, course):
        student = Student(roll_no, name, age, course)
        self.students.append(student)
        print(f"Student {name} added successfully!")

    def display_students(self):
        if not self.students:
            print("No students found.")
        else:
            print(f"{'Roll No':<10}{'Name':<20}{'Age':<5}{'Course':<10}")
            for student in self.students:
                print(f"{student.roll_no:<10}{student.name:<20}{student.age:<5}{student.course:<10}")

    def search_student(self, roll_no):
        for student in self.students:
            if student.roll_no == roll_no:
                print(f"Student found: {student.name}, Age: {student.age}, Course: {student.course}")
                return student
        print("Student not found.")
        return None

    def update_student(self, roll_no, name=None, age=None, course=None):
        student = self.search_student(roll_no)
        if student:
            if name:
                student.name = name
            if age:
                student.age = age
            if course:
                student.course = course
            print("Student details updated successfully!")

    def delete_student(self, roll_no):
        student = self.search_student(roll_no)
        if student:
            self.students.remove(student)
            print(f"Student {student.name} removed successfully!")

# Main menu to interact with the system
def main():
    system = StudentManagementSystem()

    while True:
        print("\n--- Student Management System ---")
        print("1. Add Student")
        print("2. Display Students")
        print("3. Search Student")
        print("4. Update Student")
        print("5. Delete Student")
        print("6. Exit")
        choice = input("Enter your choice: ")

        if choice == '1':
            roll_no = input("Enter roll number: ")
            name = input("Enter name: ")
            age = input("Enter age: ")
            course = input("Enter course: ")
            system.add_student(roll_no, name, age, course)
        elif choice == '2':
            system.display_students()
        elif choice == '3':
            roll_no = input("Enter roll number to search: ")
            system.search_student(roll_no)
        elif choice == '4':
            roll_no = input("Enter roll number to update: ")
            name = input("Enter new name (leave blank to keep unchanged): ")
            age = input("Enter new age (leave blank to keep unchanged): ")
            course = input("Enter new course (leave blank to keep unchanged): ")
            system.update_student(roll_no, name if name else None, age if age else None, course if course else None)
        elif choice == '5':
            roll_no = input("Enter roll number to delete: ")
            system.delete_student(roll_no)
        elif choice == '6':
            print("Exiting system. Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
