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