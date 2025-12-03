Our ADD final presentation for Semester - 1
🟦 1. Project Overview
The Smart Voice-Enabled Notes App is a mobile application developed using MIT App Inventor.
It allows users to:

Create, edit, delete, and search notes

Convert speech to text

Scan barcodes to auto-create notes

Categorize notes

Persist all data using TinyDB

Maintain project assets using GitHub version control

This project demonstrates the integration of mobile sensors, persistent storage, UI/UX design, and version control best practices.

🟦 2. Problem Statement
Students often struggle to maintain organized notes across different subjects and tasks.
Traditional typing-based note-taking is slow and inefficient when users are multitasking.

This application solves the problem by enabling:

Voice-based note entry

Barcode-based quick note generation

Categorization for clean organization

Search for quick retrieval

Offline storage

🟦 3. Objectives
Objective

Description

Voice-to-Text Notes

Allow users to add notes hands-free

Barcode Scanning

Create notes quickly from scanned text

Efficient Storage

Store all notes using TinyDB

Categorization

Organize notes into categories

Search

Find notes instantly

Version Control

Maintain project changes in GitHub

🟦 4. System Requirements
Functional Requirements
Create new notes

Edit and delete existing notes

Search notes by keywords

Voice input through SpeechRecognizer

Barcode scanning using BarcodeScanner

Data persistence using TinyDB

Categorization of notes

Non-Functional Requirements
User-friendly interface

Minimal response time

Optimized for mobile screens

Offline functionality

Reliable TinyDB storage

🟦 5. System Architecture


+---------------------------+
|        User               |
+---------------------------+
             |
             v
+---------------------------+
|         UI Layer          |
| (Buttons / Forms / Lists) |
+---------------------------+
             |
             v
+---------------------------+
|     Logic & Blocks Layer  |
| CRUD • Search • Voice •   |
| Barcode • Categorization  |
+---------------------------+
             |
             v
+---------------------------+
|      TinyDB Storage       |
+---------------------------+
             |
             v
+---------------------------+
|  Device Services (Sensors)|
| SpeechRecognizer • Barcode|
+---------------------------+
🟦 6. Use Case Diagram


        +-----------+
        |   User    |
        +-----------+
         /    |     \
        /     |      \
Create Notes  |    Edit Notes
 Search Notes |    Delete Notes
 Categorize Notes
 Scan Barcode
🟦 7. Data Flow Diagram (DFD – Level 1)


User → [Create Note] → App Logic → TinyDB → Save Note
User → [Search Note] → App Logic → Filter → Display List
User → [Scan Barcode] → BarcodeScanner → App Logic → Add Note
User → [Voice Input] → SpeechRecognizer → ContentBox
🟦 8. UI Mockups (Figma / App Inventor)
Screen 1 – Home
Search bar

ListView of notes

“+ Add Note” button

Screen 2 – Add/Edit Note
Title TextBox

Content TextBox

Category Dropdown

Voice Button

Scan Barcode Button

Save Button

(Insert screenshots here)

🟦 9. MIT App Inventor Component List
User Interface
TextBox → TitleBox, ContentBox, SearchBox

ListView → NotesListView

Button → AddNoteButton, SaveButton, VoiceButton, ScanButton

Spinner → CategorySpinner

Label → Section headers

Non-Visible Components
TinyDB → TinyDB1

SpeechRecognizer → SpeechRecognizer1

BarcodeScanner → BarcodeScanner1

Notifier → Notifier1

🟦 10. App Logic (Block Explanation)
Create Note
User types or speaks content

App builds dictionary {title, content, category, id, time}

Stored inside TinyDB under tag "notes"

Search Function
Filters list based on title/content substring

Voice Input
Uses SpeechRecognizer.AfterGettingText

Appends spoken text to ContentBox.Text

Barcode Scanning
Uses BarcodeScanner.AfterScan

Fills TitleBox automatically

Edit/Delete
NotesListView retrieves selected note

Updates TinyDB values

🟦 11. Block Code (Paste Screenshot)
Insert your block images here:

📎 Save Note Block
📎 Search Block
📎 Voice Input Block
📎 Barcode Scan Block
📎 Edit/Delete Block

I can generate CLEAN block images if you want.

🟦 12. GitHub Version Control Workflow


1. Create repository
2. Commit MIT App Inventor .aia file
3. Commit screenshots, diagrams, and documentation
4. Use branches:
      - voice-feature
      - barcode-feature
      - ui-redesign
5. Merge after testing
6. Push final build
🟦 13. Conclusion
The Smart Voice-Enabled Notes App successfully integrates:

Voice recognition

Barcode scanning

CRUD operations

Categorization

Search

Offline storage

Professional version control

This project demonstrates real-world mobile development skills using an intuitive, block-based platform.