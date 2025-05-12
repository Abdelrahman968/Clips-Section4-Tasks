# CLIPS Rule-Based System Tasks

This repository contains two CLIPS programs demonstrating rule-based systems for processing person data. Each task defines a `person` template, sample facts, and a rule to evaluate specific conditions.

## Task 1: Hair Color Check

### Description
Task 1 defines a `person` template with `name`, `age`, and `hair-color` attributes. A rule (`check_color`) identifies individuals with hair colors that are neither black nor brown and prints the hair color.

### Files
- `section4-task1.txt`: CLIPS code and execution output.

### Template
- **name**: Multislot (SYMBOL or STRING, 2-4 elements).
- **age**: Integer (20-25).
- **hair-color**: Symbol.

### Facts
Three sample people:
- John Doe (age 22, blonde hair).
- Jane Smith (age 24, red hair).
- Alex Black (age 21, black hair).

### Rule
- **check_color**: Matches people with hair color not black or brown, prints the color.

### Output
Running the rule outputs:
```
Hair color is: red
Hair color is: blonde
```

## Task 2: Age Range Check

### Description
Task 2 defines a `person` template with `name` and `age` attributes. A rule (`check_age`) identifies individuals aged between 20 and 25 (inclusive) and prints their names with a confirmation message.

### Files
- `section4-task2.txt`: CLIPS code and execution output.

### Template
- **name**: Multislot (SYMBOL or STRING, 2-4 elements).
- **age**: Integer (20-25).

### Facts
Three sample people:
- Abdelrahmna Ayman (age 22).
- Ahmed Elsayed (age 24).
- Tark Ebrahim (age 21).

### Rule
- **check_age**: Matches people with age > 20 and ≤ 25, prints their name and a message.

### Output
Running the rule outputs:
```
(Tark Ebrahim) is between 20 and 25 years old.
(Ahmed Elsayed) is between 20 and 25 years old.
(Abdelrahmna Ayman) is between 20 and 25 years old.
```

## Running the Code
1. Install CLIPS (version 6.30 or compatible).
2. Load the respective `.txt` file in the CLIPS environment.
3. Execute `(reset)` to initialize facts.
4. Execute `(run)` to apply the rules.
5. View the output in the CLIPS console.

## Notes
- Both tasks use CLIPS 6.30 (3/17/15).
- Ensure the CLIPS environment is set up to handle the provided templates and rules.
- The output order may vary due to CLIPS' internal fact processing.
