
# Applicant Filtering Workflow (n8n)

This repository contains an n8n automation workflow for managing and filtering job applicants' data.
The workflow receives incoming JSON payloads via a webhook, stores raw applicant data, and applies multiple filters (experience, salary, portfolio, skills, and custom logic) to generate structured datasets for recruitment purposes.

---

## 📌 Features

- Webhook integration – Accepts incoming applicant data in JSON format.
- Raw data storage – Saves all applicants into a Google Sheet for record keeping.
- Filtering system:
    - Experience filter → Filters applicants based on years of experience.
    - Salary filter → Filters applicants based on expected salary range.
    - Portfolio filter → Keeps applicants who have provided a portfolio link.
    - Skills filter → Filters applicants based on required skills (Python or JS).
    - Complex filter → Allows for combined, custom filtering rules.
- Google Sheets integration – Saves both raw and filtered applicant data in separate sheets for easy review.

---

## 📂 Workflow Overview

1. Webhook – Receives applicant data via a POST request.

2. Raw applicants data – Saves all incoming data into Google Sheets.

3. Filters – Processes applicants against predefined criteria:
    - Experience
    - Expected Salary
    - Skills
    - Complex/custom logic
4. Filtered data storage – Saves filtered results into separate Google Sheets.

---

## 📝 JSON Example

```json
{
  "position": "AI developer",
  "fullname": "John Doe",
  "email": "user@test.com",
  "phone": "+481234567",
  "linkedin": "https://linkedin.com/in/johndoe",
  "experience_years": 3,
  "skills": ["Python", "TensorFlow", "n8n"],
  "portfolio": "https://johndoe.dev",
  "cover_letter": "I am very motivated to join your company and contribute to AI projects.",
  "availability": "immediately",
  "expected_salary": "4000"
}
```

---

## 🖼️ Visual Overview

![Alt Text](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExaHY4MTQ5NmM2cG1pcWdrYWd1cjRwcnMxNXJuaGxheW1yZm10NHp0diZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/D0tZAp4Rs4j96jnnew/giphy.gif)

---

## 🚀 Usage

1. Import the workflow into your n8n instance.
2. Configure your Google Sheets credentials.
3. Adjust the filters according to your recruitment needs:
    - Minimum experience
    - Maximum salary
    - Required skills
    - Portfolio requirement
    - Custom rules

---

## 🛠️ Tech Stack

- n8n – Automation platform
- Google Sheets – Data storage and filtering results
- Webhook – API entry point for applicants

--- 

### 📄 Download or View the Workflow

👉 [Click here to view `workflow.json`](./workflow.json)

You can import this file directly into your n8n instance.