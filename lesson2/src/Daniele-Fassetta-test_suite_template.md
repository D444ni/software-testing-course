# TEST_SUITE_TEMPLATE.md — Manual Test Suite (PlanningPoker)

> **Fill this file during the lab.**  
> Do not modify the implementation code.

## Group Info

- **Date:** 09 March 2026 
- **Members:**
  - Daniele Fassetta

---

## Program Under Test (PUT)

- **Repository / Folder:**  
- **File:** `planning_poker.py`  
- **Method:** `identify_extremes(estimates)`

### Short description (in your own words)

Write 2–3 lines about what the method is supposed to do.
The method receives a list of estimates of the form [dev. name, est. value] and
identify the two extremes of a planning poker session (lowest estimate and highest estimate).

---

## Assumptions / Preconditions

List any assumptions you are making about inputs or environment (if none, write “None”).

-  None

---

## Test Suite

Fill the table below. Add more rows if needed.

> **Inputs format suggestion:** represent estimates as a list of pairs, e.g.  
> `[("Alice", 5), ("Bob", 3), ("Charlie", 8)]`

| ID | Description | Preconditions | Inputs | Expected Output | Observed Output | Outcome (Pass/Fail) | Notes |
|---|------------|--------------|-------|----------------|----------------|--------------------|------|
| TC01 | Min in first position | List is not empty. | `[("Alice", 2), ("Bob", 5), ("Charlie", 8)]` | `["Alice", "Charlie"]` |  |  |  |
| TC02 | Max in first position | List contains values where the maximum is at index 0. | `[("Alice", 10), ("Bob", 3), ("Charlie", 5)]` | `["Bob", "Alice"]` |  |  |  |
| TC03 | All identical estimates | List contains at least two estimates with the same value. | `[("Alice", 5), ("Bob", 5), ("Charlie", 5)]` | `["Alice", "Alice"]` |  |  | |
---

## Notes on Oracles (Expected Output)

Explain briefly how you decided the expected outputs (your “oracle”):

-  TC1: I just looked at the numbers and expect the program to work correctly
-  TC2: I just looked at the numbers and expect the program to work correctly
-  TC3: I expect the system to pick two times the value "Alice" since is the first min and max in the list 

---

## Reflection (short)

Answer briefly (5–10 lines total):

1. What guided your choice of test cases? Possible failure scenarios.
- Testing the input bounds for a programs can show unexpected behaviors of the execution (for TC1 and TC2)
- See if the program produces consistent outputs in a specific situation (for TC3) 
2. How confident are you in the method after running (or reasoning about) your test suite? The method of finding all possible bugs and failure situations by hand is not a good way to proceed in software testing
3. What would you test next if you had more time? Probably other possible observable bug situations to verify is the program works correctly in different scenarios. For example, what could happen with invalid data? what is we submit a single pair? etc.
