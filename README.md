from fpdf import FPDF

# Display all available modules
help('modules')

# Initialize FPDF class instance
pdf = FPDF()

# Add a page to the PDF
pdf.add_page()

# Set the font for the title
pdf.set_font('Arial', 'B', 16)
pdf.cell(200, 10, txt="Resume", ln=True, align='C')

# Insert name
pdf.ln(10)  # Line break
pdf.set_font('Arial', 'B', 14)
pdf.cell(200, 10, txt="Deepak Boddula", ln=True, align='C')

# Include contact information
pdf.set_font('Arial', '', 12)
pdf.cell(200, 10, txt="Email: deepakboddula12@gmail.com", ln=True, align='C')

# Add Objective section
pdf.ln(10)  # Line break
pdf.set_font('Arial', 'I', 12)
objective = ("A highly motivated and committed undergraduate with a strong foundation in Python, Java, SQL, and data analysis. "
             "Keen to leverage my skills to contribute to innovative projects and grow in a dynamic, forward-thinking environment.")
pdf.multi_cell(0, 10, txt=f"Objective:\n{objective}")

# Include Education section
pdf.ln(10)  # Line break
pdf.set_font('Arial', 'B', 12)
pdf.cell(200, 10, txt="Education", ln=True, align='L')
pdf.set_font('Arial', '', 12)
pdf.cell(200, 10, txt="Bachelor of Technology (B.Tech) in Electronics and Communication Engineering (ECE) - JNTUH University", ln=True, align='L')

# List Skills
pdf.ln(10)  # Line break
pdf.set_font('Arial', 'B', 12)
pdf.cell(200, 10, txt="Skills", ln=True, align='L')
pdf.set_font('Arial', '', 12)
pdf.cell(200, 10, txt="• Python\n• Java\n• SQL", ln=True, align='L')

# Include Experience section
pdf.ln(10)  # Line break
pdf.set_font('Arial', 'B', 12)
pdf.cell(200, 10, txt="Experience", ln=True, align='L')
pdf.set_font('Arial', '', 12)
pdf.multi_cell(0, 10, txt="• Currently pursuing undergraduate studies, enhancing my knowledge in computer programming, data analysis, and software development.")

# Include Certifications
pdf.ln(10)  # Line break
pdf.set_font('Arial', 'B', 12)
pdf.cell(200, 10, txt="Certifications", ln=True, align='L')
pdf.set_font('Arial', '', 12)
pdf.cell(200, 10, txt="• IBM Data Analysis with Python", ln=True, align='L')

# Add Declaration
pdf.ln(10)  # Line break
pdf.set_font('Arial', 'I', 12)
declaration = ("I hereby declare that the details provided are accurate to the best of my knowledge and belief.")
pdf.multi_cell(0, 10, txt=f"Declaration:\n{declaration}")

# Save the generated PDF
pdf.output("Deepak_Boddula_Resume.pdf")

print("The resume has been successfully generated.")
 




TASK-2

class TaskManager:
    def __init__(self):
        self.tasks = {}
        self.task_id_counter = 1

    def show_tasks(self):
        if not self.tasks:
            print("No tasks to display.")
        else:
            for task_id, (description, status) in self.tasks.items():
                print(f"{task_id}. {description} - {status}")

    def create_task(self, description):
        self.tasks[self.task_id_counter] = (description, "Pending")
        self.task_id_counter += 1
        print(f"New task added: {description}")

    def delete_task(self, task_id):
        if task_id in self.tasks:
            del self.tasks[task_id]
            print(f"Task {task_id} has been deleted.")
        else:
            print(f"Task {task_id} not found.")

    def modify_task(self, task_id, new_description):
        if task_id in self.tasks:
            self.tasks[task_id] = (new_description, self.tasks[task_id][1])
            print(f"Task {task_id} has been updated to: {new_description}")
        else:
            print(f"Task {task_id} not found.")

    def mark_task_completed(self, task_id):
        if task_id in self.tasks:
            description, _ = self.tasks[task_id]
            self.tasks[task_id] = (description, "Completed")
            print(f"Task {task_id} marked as completed.")
        else:
            print(f"Task {task_id} not found.")

    def set_task_reminder(self, task_id, reminder_time):
        if task_id in self.tasks:
            print(f"Reminder set for Task {task_id} at {reminder_time}.")
        else:
            print(f"Task {task_id} not found.")


def main():
    task_manager = TaskManager()

    while True:
        print("\nMenu:")
        print("1. View tasks")
        print("2. Add task")
        print("3. Remove task")
        print("4. Update task")
        print("5. Complete task")
        print("6. Set reminder")
        print("7. Exit")

        print("\nTasks:")
        task_manager.show_tasks()

        choice = input("Choose an option (1-7): ")

        if choice == '1':
            task_manager.show_tasks()
        elif choice == '2':
            task_description = input("Enter task description: ")
            task_manager.create_task(task_description)
        elif choice == '3':
            task_id = int(input("Enter task ID to remove: "))
            task_manager.delete_task(task_id)
        elif choice == '4':
            task_id = int(input("Enter task ID to update: "))
            new_description = input("Enter new task description: ")
            task_manager.modify_task(task_id, new_description)
        elif choice == '5':
            task_id = int(input("Enter task ID to mark as completed: "))
            task_manager.mark_task_completed(task_id)
        elif choice == '6':
            task_id = int(input("Enter task ID to set reminder for: "))
            reminder_time = input("Enter reminder time: ")
            task_manager.set_task_reminder(task_id, reminder_time)
        elif choice == '7':
            print("Exiting program...")
            break
        else:
            print("Invalid choice, please try again.")


if __name__ == "__main__":
    main()
