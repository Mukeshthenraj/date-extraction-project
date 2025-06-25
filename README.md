# 📅 Date Extraction and Normalization

This project extracts and normalizes messy medical note dates using regular expressions and Python. It handles multiple date formats and sorts them chronologically based on predefined assumptions.

## ✨ Features

- ✅ Extraction of diverse date formats (e.g., `mm/dd/yy`, `Mar 20, 2009`, `20 March 2009`, `6/2008`, `2010`)
- ✅ Normalization of dates with assumptions for missing day or month
- ✅ Sorting based on extracted datetime
- ✅ Detection of unmatched lines (lines with no valid date)
- ✅ Clean structure: Modular scripts

## 🧠 Motivation

Medical notes often contain date entries in inconsistent formats. This script provides a flexible method to detect, normalize, and sort them, helping with downstream medical data analysis tasks.

---

## ▶️ How to Run

### 1. Install dependencies
```bash
pip install pandas numpy
```

### 2. Folder Structure

```
project_root/
│
├── assets/
│   └── dates.txt                # Raw input text file (500 medical notes)
│
├── extract_dates.py             # Main script to extract and sort dates
├── find_unmatched.py           # Helper script to find lines with no valid date
├── README.md
```

### 3. Run the scripts

```bash
# Extract and sort dates
python extract_dates.py

# Find lines without matched dates
python find_unmatched.py
```

---

## 🧪 Assumptions in Date Handling

- `xx/xx/xx` is parsed as `mm/dd/yy`
- Years with two digits are treated as 1900s
- If the day is missing, it defaults to `1`
- If the month is missing, it defaults to `January`

---

## 📌 Sample Formats Supported

```
04/20/2009     → Apr 20, 2009  
Mar 20, 2009   → Mar 20, 2009  
20 March 2009  → Mar 20, 2009  
6/2008         → Jun 1, 2008  
2009           → Jan 1, 2009
```

---

## 👤 Author

**Mukesh Thenraj**

---

## 📜 License

This project is open for educational and non-commercial use.
