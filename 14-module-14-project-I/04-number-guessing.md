### **14.4 Number Guessing Game - Descriptive Notes**

#### **Objective:**
Create a **Number Guessing Game** where the user guesses a randomly generated number within a specified range. The game will provide feedback on each guess and track the number of attempts until the correct guess is made.

---

### **Flow of the Number Guessing Game:**

1. **Game Introduction:**
   - Explain the rules of the game to the user: they need to guess a randomly generated number within a specific range (e.g., 1 to 100).
   - Inform the user that after each guess, feedback will be provided if the guess is too high, too low, or correct.

2. **Generate Random Number:**
   - The program generates a random number within a specified range (e.g., between 1 and 100) that the user needs to guess.

3. **User Input:**
   - The user is prompted to enter their guess (a number within the given range).
   - Input validation ensures the user enters a valid number.

4. **Providing Feedback:**
   - After each guess, the program will compare the guess to the generated number:
     - If the guess is too high, the program will display "Too high!"
     - If the guess is too low, the program will display "Too low!"
     - If the guess is correct, the program will display "Correct!" and end the game.

5. **Setting Up a Loop:**
   - The game will use a loop to allow multiple attempts. The user will keep guessing until they guess correctly.
   - Each guess will trigger feedback and prompt the user to try again.

6. **Tracking the Number of Attempts:**
   - The program will track the number of guesses made by the user.
   - After the correct guess, the program will display the total number of attempts it took the user to guess the correct number.

7. **Ending the Game:**
   - Once the user guesses the correct number, the game will end and display a message showing how many attempts it took to guess the number correctly.

---