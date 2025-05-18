

```markdown
# 🧪 Attendance System Platform Testing (SQA Final Project)

This project is the final assignment for the **Software Quality Assurance** course. The goal is to automate testing for a student **Attendance Management System**, covering UI, API, and performance testing.

## 🔧 Tech Stack

- **Python 3.11+**
- **Selenium** – for browser-based UI testing
- **Pytest** – test framework for unit and integration testing
- **requests** – for REST API testing
- **Locust** – for performance/load testing
- **HTMLTestRunner** – generates HTML test reports
- **Google Chrome + WebDriver**


---

## 🚀 Running UI Tests (Selenium + Pytest)

### Install dependencies

```bash
pip install -r requirements.txt
````

### Run UI tests and generate HTML report

```bash
pytest tests/test_ui_attendance.py --html=reports/ui_report.html
```

---

## 📡 Running API Tests

File: `test_api_attendance.py`

Tested endpoints:

* `POST /api/attendance` — Add new attendance entry
* `GET /api/attendance` — Fetch all entries
* `PUT /api/attendance/{id}` — Update existing entry
* `DELETE /api/attendance/{id}` — Delete an entry

Run the tests:

```bash
pytest tests/test_api_attendance.py --html=reports/api_report.html
```

---

## ⚡ Performance Testing with Locust

File: `locustfile.py`

### Start Locust:

```bash
locust
```

Then go to:

```
http://localhost:8089
```

### Example test configuration:

* **Host:** `http://localhost:5000`
* **Number of Users:** `50`
* **Spawn Rate:** `5 users/second`

Tested endpoints:

* `GET /api/attendance`
* `POST /api/attendance`
* `PUT /api/attendance/{id}`
* `DELETE /api/attendance/{id}`

---

## 📝 Sample Attendance Entry (JSON)

```json
{
  "_id": "6644b0d6a6d0c176adbee01c",
  "student_id": 123,
  "status": "Present",
  "timestamp": "2025-05-15T10:45:00"
}
```

---

## 📌 Suggestions for Improvement

* Add login/authentication testing
* Integrate into CI/CD pipeline (e.g., GitHub Actions)
* Add negative test cases (invalid data)

---

## 👨‍💻 Author

* **Name:** \[Your Name]
* **Course:** Software Quality Assurance, 2025
* **Instructor:** \[Instructor’s Name]

```

---

Would you also like me to generate the `requirements.txt` for you based on your current setup?
```
