### **14.2 Grading Calculator - Descriptive Notes**

#### **Objective:**
The goal is to develop a **Grading Calculator** that will:
1. Take the user's input for marks (or grades).
2. Calculate the final grade based on predefined grade thresholds.
3. Display the final grade to the user.

---

### **Flow of the Grading Calculator:**

1. **Game Introduction:**
   - The program begins by explaining the grading system to the user. 
   - The grading system may include letter grades such as:
     - **A** for marks between 90 to 100
     - **B** for marks between 80 to 89
     - **C** for marks between 70 to 79
     - **D** for marks between 60 to 69
     - **F** for marks below 60.
   - The user is prompted to enter their marks, which should be a number between 0 and 100.

2. **User Input:**
   - The user is asked to input their marks. This value will be used to determine the grade.
   - Input should be validated to ensure it’s a valid number (i.e., it should be a float or integer) and falls within the valid range (0 to 100). If the input is invalid, the program should prompt the user to re-enter valid marks.

3. **Grade Calculation:**
   - Once the user provides valid input, the program will calculate the grade based on predefined thresholds:
     - If the marks are between 90 and 100, the grade will be **A**.
     - If the marks are between 80 and 89, the grade will be **B**.
     - If the marks are between 70 and 79, the grade will be **C**.
     - If the marks are between 60 and 69, the grade will be **D**.
     - If the marks are below 60, the grade will be **F**.

4. **Displaying the Final Grade:**
   - After calculating the grade, the program will display the **final grade** to the user. This will be one of the letter grades (A, B, C, D, or F), based on the marks provided.
   
5. **Edge Case Handling:**
   - The program will handle cases where the user enters invalid marks, such as:
     - A number that is outside the valid range (0 to 100). In this case, an error message should be displayed, and the program should request valid input.
     - Non-numeric input (e.g., if the user types text or characters). The program should catch this error and notify the user that they need to enter a numeric value.

6. **Exit or Restart:**
   - After displaying the grade, the program can provide an option to either **exit** or **restart** the grading process. This will allow users to input new marks and calculate a new grade.
   - Optionally, the program could allow for multiple inputs and compute average grades over several subjects, but that can be an enhancement for future iterations.

7. **Feedback (Optional):**
   - The program could be designed to offer **feedback** based on the grade, such as:
     - **A**: “Excellent performance!”
     - **B**: “Good job, keep going!”
     - **C**: “Fair performance, aim for better.”
     - **D**: “Needs improvement.”
     - **F**: “Fail, try harder next time.”

---