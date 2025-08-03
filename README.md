# 📊 Student Performance Monitor – n8n Workflow

This n8n workflow automates the process of monitoring student performance by integrating Google Sheets, Slack, and Twilio. It identifies students with low attendance or poor exam scores and sends timely notifications to both students and their parents.

---

## 🚀 Features

- ✅ Automatically triggers when new student data is added to a Google Sheet
- 📉 Checks for low attendance or low exam scores using conditional logic
- 💬 Sends alerts to students via Slack if Slack ID is available
- 📲 Sends SMS or WhatsApp messages to parents using Twilio
- ⚙️ Gracefully exits when students meet performance requirements

---

## 🧩 Nodes Used

- **Google Sheets Trigger**: Monitors new rows (student data) added
- **If Node**: Evaluates attendance and exam score conditions
- **Slack Node**: Sends alert messages to students with Slack IDs
- **Twilio Node**: Sends SMS/WhatsApp messages to parents
- **No Operation Node**: Ends the workflow if no action is needed

---

## 📁 Input Format (Google Sheets)

| Student Name | Attendance (%) | Exam Score | Parent Phone | Slack ID   |
|--------------|----------------|------------|--------------|------------|
| Atulk        | 60             | 35         | +91600660XXXX| @john.doe  |

---

## 🔔 Notification Criteria

- **Low Attendance**: Less than 75%
- **Low Score**: Less than 40%

These thresholds can be adjusted in the **If Node** conditions.

---

## 🛠 Requirements

- n8n installed locally or via cloud
- Connected Google Sheet with student data
- Valid Slack Bot token with chat:write scope
- Twilio account with messaging enabled

---

## 📦 Deployment

1. Open your n8n instance
2. Import the `.json` workflow file
3. Set up credentials for Google Sheets, Slack, and Twilio
4. Save and activate the workflow

---


---

## 🙋‍♂️ Author

Created by Atul Kuamr – Automating student performance alerts with n8n.
