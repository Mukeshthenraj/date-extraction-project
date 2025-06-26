# 📅 Date Extraction and Normalization

This project extracts and normalizes messy medical note dates using regular expressions and Python. It handles multiple date formats, visualizes yearly counts, and provides sorted output in a readable file.

## ✨ Features

- ✅ Extraction of diverse date formats (e.g., `mm/dd/yy`, `Mar 20, 2009`, `20 March 2009`, `6/2008`, `2010`)
- ✅ Normalization of dates with assumptions for missing day or month
- ✅ Sorting based on extracted datetime
- ✅ Detection of unmatched lines (lines with no valid date)
- ✅ Output saved to file: `sorted_dates_output.txt`
- ✅ Bar plot visualization of number of notes per year (`year_distribution.png`)
- ✅ Notebook-based interactive version included (`assignment1.ipynb`)
- ✅ Clean structure: Modular scripts in `scripts/`

## 🧠 Motivation

Medical notes often contain date entries in inconsistent formats. This script provides a flexible method to detect, normalize, and sort them, helping with downstream medical data analysis tasks.

---

## ▶️ How to Run

### 1. Install dependencies
```bash
pip install pandas numpy matplotlib
```

### 2. Folder Structure

```
project_root/
│
├── assets/
│   └── dates.txt                  # Raw input text file (500 medical notes)
│
├── scripts/
│   ├── extract_dates.py           # Main script to extract and sort dates
│   └── find_unmatched.py          # Helper script to find unmatched lines
│
├── date_extraction_project.py     # Combined main version
├── assignment1.ipynb              # Notebook with visualization
├── sorted_dates_output.txt        # Sorted lines with extracted date
├── year_distribution.png          # Bar chart of entries per year
├── README.md
```

### 3. Run the script

```bash
# Main execution
python date_extraction_project.py
```

---

## 🧪 Assumptions in Date Handling

- `xx/xx/xx` is parsed as `mm/dd/yy`
- Years with two digits are treated as 1900s
- If the day is missing, it defaults to `1`
- If the month is missing, it defaults to `January`

---

## 📊 Visualization

The script generates a bar chart showing the distribution of medical notes over the years. The chart is saved as `year_distribution.png`.

---

## 📤 Output File

The file `sorted_dates_output.txt` contains all 500 lines sorted by detected date with line numbers for easier review.

---

## 👤 Author

**Mukesh Thenraj**

---

## 📜 License

This project is open for educational and non-commercial use.
