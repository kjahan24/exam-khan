
Below is a complete **README.md** for your project.

````markdown

# Fake News Detection System, Presented by: Khan Sajahan, Mobile: 01777075686

## Project Overview

The **Fake News Detection System** is a Python Flask-based web application that analyzes news content and provides a risk-based evaluation. The system checks whether a news article may be reliable, biased, misleading, or needs further verification.

This project is designed for an AI Engineering practical assignment. It does not claim that any news is 100% fake or 100% real. Instead, it provides a safe and explainable analysis using rule-based logic.

---

## Project Objective

The main objective of this project is to build a simple web application where a user can paste a news link or full news text, and the system will analyze the content based on reliability and bias indicators.

The system provides:

- Reliability Score
- Bias Risk Score
- Google News coverage signal
- Main reasons behind the result
- Positive reliability signals
- Verification suggestions

---

## Core Features

### 1. News Text Analysis

Users can paste full news text into the input box. The system analyzes the text and detects warning signs such as:

- Suspicious or emotional words
- Serious political or security claims
- Allegation-based language
- Missing date or author information
- Weak source or evidence signals

---

### 2. News URL Input

Users can also paste a news URL. The system tries to extract article text from the link.

Note: Some websites block automatic article extraction or load content using JavaScript. For best results, users should paste the full news text.

---

### 3. Reliability Score

The system calculates a **Reliability Score** from 0 to 100.

Example:

```text
Reliability Score: 70 / 100
````

A higher reliability score means the news has more positive reliability signals.

---

### 4. Bias Risk Score

The system calculates a **Bias Risk Score** from 0 to 100.

Example:

```text
Bias Risk Score: 30 / 100
```

A higher bias risk score means the article may contain more warning signs, emotional wording, weak evidence, or one-sided claims.

---

### 5. Google News Coverage Signal

The system includes a Google News coverage check as a supporting signal.

Example outputs:

```text
Google Search Result: Found in 2 news sources.
```

or

```text
Google Search Result: No matching news coverage found in Google News.
```

Important: No Google News result does not prove that the news is fake. It only means the claim needs further verification.

---

### 6. Explainable Result

The system shows the reasons behind the result. This makes the project more transparent and easier to understand.

Example:

```text
Main Reasons:
- No clear author or reporter signal was detected.
- Few reliability indicators were found.
- Serious crime, political, security, or allegation-based keywords were found.
```

---

## Technology Used

* Python
* Flask
* Requests
* BeautifulSoup
* HTML
* CSS
* Rule-based analysis logic

---

## Project Structure

```text
fake_news_detection/
│
├── main.py
├── README.md
└── .venv/
```

### File Description

| File / Folder | Description                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------- |
| `main.py`     | Main Flask application file containing backend logic, HTML template, and analysis functions |
| `README.md`   | Project documentation file                                                                  |
| `.venv/`      | Virtual environment folder                                                                  |

---

## Setup Instructions

### Step 1: Create Project Folder

Create a folder named:

```text
fake_news_detection
```

Open this folder in PyCharm.

---

### Step 2: Create Virtual Environment

Create a virtual environment inside the project folder.

In PyCharm Terminal:

```bash
python -m venv .venv
```

Activate it if needed.

For Windows:

```bash
.venv\Scripts\activate
```

---

### Step 3: Install Required Packages

Run this command in the terminal:

```bash
pip install flask requests beautifulsoup4 lxml
```

---

### Step 4: Create Main Python File

Create a file named:

```text
main.py
```

Paste the project code inside this file.

---

### Step 5: Run the Project

Run the Flask application:

```bash
python main.py
```

If the project runs successfully, the terminal will show:

```text
Running on http://127.0.0.1:5000
```

---

### Step 6: Open in Browser

Open this URL in your browser:

```text
http://127.0.0.1:5000
```

---

## How to Use

1. Open the web application.
2. Paste a news URL or full news text.
3. Click the **Analyze News** button.
4. View the result:

   * Reliability Score
   * Bias Risk Score
   * Google News Result
   * Main Reasons
   * Positive Signals
   * Verification Suggestions

For best results, paste the full news article text.

---

## Result Categories

| Bias Risk Score | Result                                     |
| --------------- | ------------------------------------------ |
| 0–30            | Low Bias Risk / More Reliable              |
| 31–60           | Medium Bias Risk / Needs Verification      |
| 61–100          | High Bias Risk / Needs Strong Verification |

---

## Clean Code Principles Used

The code follows basic clean code principles:

* Functions are used for separate tasks.
* Variable names are meaningful.
* Comments are added to explain important logic.
* The main analysis logic is separated into reusable functions.
* The user interface and backend logic are kept organized in one file for simplicity.

---

## Main Functions

### `clean_text(text)`

Cleans extra spaces and formats the input text.

### `is_valid_url(url)`

Checks whether the provided URL is valid.

### `fetch_news_from_url(url)`

Tries to extract news article text from a given URL.

### `has_date(text)`

Checks whether the article contains a date or time reference.

### `has_author_signal(text)`

Checks whether the article includes an author, reporter, or correspondent signal.

### `get_google_news_coverage(query)`

Checks whether similar news appears in Google News RSS results.

### `analyze_news(news_text, news_url)`

Main function that calculates the reliability score, bias risk score, reasons, and final result.

---

## Important Notes

This project gives a risk-based analysis only. It does not guarantee that a news article is completely fake or completely true.

The system is mainly designed for educational purposes and AI Engineering practice.

Google News coverage is used only as a supporting verification signal. It should not be treated as the final truth.

---

## Future Improvements

Possible future improvements include:

* Machine learning-based fake news classification
* Better Bangla language processing
* Real Google Search API integration
* Source credibility database
* Fact-checking website integration
* User history and report export feature
* More advanced bias detection model

---

## Conclusion

The Fake News Detection System is a simple but practical AI Engineering project. It demonstrates how a web application can analyze news content using rule-based logic and provide explainable results.

This project helps users understand whether a news article may be reliable, biased, misleading, or in need of stronger verification.

```
# Fake News Detection System
## Project Demo Video
Watch the demo video here:: https://drive.google.com/file/d/1qnrmhxy5C7CO9Z4x8sqdNmDLpDnEP4Zy/view?usp=sharing
