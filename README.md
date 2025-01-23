# Membership Management Project

## Project Overview
This project manages membership data by separating active and inactive members into separate files. It consists of functions for generating test data, cleaning membership records, and validating the output. The project is written in Python and uses basic file handling and list comprehensions to achieve its objectives.

---

## Features
- **Generate Membership Files:** Create test data files for active and inactive members.
- **Clean Membership Records:** Move inactive members from the main membership file to an inactive file.
- **Validation Mechanism:** Ensure the output files conform to the expected structure and data integrity.

---

## File Structure
- **members.txt:** Stores all membership data.
- **inactive.txt:** Stores data for inactive members.
- **testWrite.txt:** Used for testing the cleaning process (active members).
- **testAppend.txt:** Used for testing the cleaning process (inactive members).

---

## Functions
### 1. `genFiles(current, old)`
Generates two files:
- `current` (e.g., `members.txt`): Contains a mix of active and inactive members.
- `old` (e.g., `inactive.txt`): Contains only inactive members.

**Parameters:**
- `current`: Path to the active members file.
- `old`: Path to the inactive members file.

### 2. `cleanFiles(currentMem, exMem)`
Cleans the membership records by moving inactive members from the `currentMem` file to the `exMem` file.

**Parameters:**
- `currentMem`: Path to the file containing all members.
- `exMem`: Path to the file for inactive members.

### 3. `testMsg(passed)`
Returns a message indicating whether the test passed or failed.

**Parameter:**
- `passed`: Boolean value indicating the test result.

---

## How to Run
1. Clone this repository.
2. Ensure Python 3.x is installed on your system.
3. Run the script:
   ```bash
   python membership_management.py
   ```
4. View the output in the respective files:
   - `members.txt` (active members)
   - `inactive.txt` (inactive members)

---

## Testing
The project includes a built-in testing mechanism to validate the functionality of the `cleanFiles` function.
1. Files `testWrite.txt` and `testAppend.txt` are generated for testing.
2. The cleaning function processes these files.
3. The results are compared to the original data to ensure correctness.

Run the script and check the console output for test results.

---

## Example Output
### Active Members
```plaintext
Membership No  Date Joined  Active  
12345          2020-12-15  yes     
67890          2019-07-11  yes     
```

### Inactive Members
```plaintext
Membership No  Date Joined  Active  
54321          2018-03-10  no      
09876          2017-09-22  no      
```

---

## Dependencies
- Python 3.x
- No external libraries required

---

## Author
Siddharth B N

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

