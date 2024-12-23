# Selenium Automation for Attendance Tracking

This project automates logging into the **Azerbaijan Technical University (AZTU)** student portal to extract attendance data for specific courses using Selenium WebDriver.

## Features
- Logs in to the AZTU student portal using credentials from a `.env` file.
- Navigates to the attendance section of a specified course.
- Extracts attendance dates and statuses.
- Saves the extracted data into a CSV file.

## Prerequisites

### Software Requirements
- Python 3.7+
- Google Chrome browser and ChromeDriver

### Python Libraries
- `selenium`
- `python-dotenv`
- `csv`

### Environment Setup
Ensure you have a `.env` file in the root directory with the following variables:
```
USERNAME=your_username_here
PASSWORD=your_password_here
```
Replace `your_username_here` and `your_password_here` with your AZTU student portal credentials.

### WebDriver Setup
Download the appropriate version of ChromeDriver for your system from [ChromeDriver Download](https://sites.google.com/chromium.org/driver/). Ensure the ChromeDriver is added to your system's PATH.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/SakoAkk/Python-Lab3.git
   cd Python-Lab3
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```


3. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Update the `.env` file with your AZTU portal credentials.
2. Run the script:
   ```bash
   python main.py
   ```
   
3. The extracted attendance data will be saved in `attendance_data.csv` in the current working directory.

## Script Flow
1. **Login**: Opens the AZTU student portal and logs in using the provided credentials.
2. **Navigation**:
   - Clicks on the menu icon.
   - Opens the student section.
   - Navigates to the course section and selects "Python proqramlaşdırma dili."
   - Opens the attendance page.
3. **Data Extraction**:
   - Extracts attendance dates and their corresponding statuses.
   - Formats and saves the data in a CSV file.

## Output
- `attendance_data.csv`: A CSV file containing two columns:
  - `Tarix` (Date)
  - `İştirak` (Attendance Status)

### Example Output
```csv
Tarix,İştirak
12/01,i/e
12/02,q/b
```

## Error Handling
- The script includes exception handling for common issues like elements not being found or timeouts.
- If an error occurs, a descriptive message will be printed in the console.

## Notes
- Ensure a stable internet connection.
- If the portal layout changes, the script may need updates to its locators.
