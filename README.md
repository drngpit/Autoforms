# 📄 Autoforms

## 📌 Overview

**Autoforms** is a Google Apps Script project that automates the processing of Google Form submissions by:

* Generating PDFs from form entries (certificates and write-ups).
* Sending personalized emails with those PDFs attached to participants.

This is especially useful for events like student lectures, workshops, or participation tracking where certificates and summaries must be generated automatically.

---

## 🚀 Features

✔️ Automatically generate a **Certificate of Participation** PDF

✔️ Create a **Write-Up PDF** based on form responses

✔️ Send automated **emails** with both PDFs attached

✔️ Works with Google Apps Script (easy deployment with Google Workspace)

---

## 📁 Repository Contents

| File              | Description                                                    
| ----------------- | -------------------------------------------------------------- 
| `script.js`       | Google Apps Script that handles PDF generation & email sending 
| Example Documents | Templates and sample certificates used in PDF generation       
| Misc assets       | Write-up examples, lecture certificates, images, docs

---

## 🧠 How It Works

The core logic in `script.js` does the following:

1. **Listen to form submission**
2. **Replace placeholders** in Google Docs templates with submitted values
3. **Generate two PDFs**:

   * Certificate of Participation
   * Write-Up based on topic information
4. **Email the participant** with both PDFs attached

The script uses:

* `DriveApp` and `DocumentApp` for PDF file creation
* `GmailApp.sendEmail()` to deliver final results to the form respondent

(read the full script to see all methods used)

---

## 📥 Setup & Installation

To get this working:

1. Create a **Google Form** that collects:

   * Full Name
   * Email
   * Topic Title
   * Topic Description
2. Create Google Doc templates with placeholders like `{name}`, `{topic}`, `{content}`.
3. Add the template IDs and folder IDs into the script where indicated.
4. Open **Google Apps Script** → paste `script.js`.
5. Enable necessary Google APIs:

   * Drive API
   * Gmail API
6. Save and run the script, granting permissions as required.

---

## 💡 Example Email Sent

```text
To: participant@example.com  
Subject: Bite-Sized Wisdom: Quick Lectures By First Year CSE(Cybersecurity) Students

Thank you for participating!  
Your Certificate of Participation and Writing Assignment have been attached.
```

---

## 📌 Customization

You can modify:

* The email subject and body text
* Template format and placeholders
* Folder structure for output PDFs
* Additional validation and form fields

---

## 🛠 Tools Used

* JavaScript (Apps Script)
* Google Workspace (Forms, Docs, Drive, Gmail)

---

## 📄 License

[GNU General Public License v3.0 (GPL-3.0)](https://www.gnu.org/licenses/gpl-3.0.txt)

