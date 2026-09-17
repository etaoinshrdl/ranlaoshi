📚 Ranlaoshi - Interactive Lesson Authoring Tool

Version: v1.0.9 Lite
Date: 2026-09-13

Ranlaoshi is a powerful, single-page HTML application that lets teachers build, customize, and deliver interactive lessons entirely within their browser. No server, no accounts, no installations—just pure HTML, CSS, and JavaScript.

It combines a drag-and-drop slide editor with a comprehensive student management system (gradebook, attendance, points, merits) and an immersive presentation mode.

✨ Key Features

🛠️ Slide Editor

Rich Canvas Elements: Add and manipulate Text, Images, Shapes (Rectangles, Lines, Arrows), Tables, Equations (LaTeX), Video Embeds, and Labels.
Drag & Drop: Intuitive movement with snap-to-grid and alignment guides for pixel-perfect layouts.
Multi-Select & Grouping: Shift/Ctrl-click to select multiple elements, then Group them so they move together. Ungroup anytime.
Z-Index Control: Bring elements forward or send them backward; lock elements to prevent accidental edits.
Undo/Redo: Full history stack (up to 50 states) with Ctrl+Z / Ctrl+Y.
Text Elements

Inline Math: Type $...$ in any text element to render inline KaTeX equations on the fly. Use the ∑ button to insert equations directly from the library.
Bullet Lists: Toggle bullet formatting with a configurable bullet character (•, -, *, ▸, ○, ■).
Border Controls: Per-element border width, radius, and color.
Reveal Order: Mark text as Hidden in Presentation and assign a reveal order to build up diagrams progressively.
Interactive Exercises

Multiple Choice Questions (MCQ): Mark correct answers and reveal them during presentation.
Fill-in-the-Blanks: Drag-and-drop words from a word bank into the passage. Supports shuffled word banks and duplicate answers.
Matching Exercises: Click-to-match items between two columns with colored feedback and a live score. Optional shuffle. Generates SVG connection lines.
True / False: Statements with True/False chips, check answers, and reset. Statements are edited via modal.
Team Scoreboard: Live team scoring with +/− buttons, student assignment, shuffle, reset, and winner detection. Scores reset when the presentation ends.
Equation Editor

Side Panel Editor: Live LaTeX preview, symbol toolbar (fractions, roots, Greek letters, chemistry via mhchem), and style controls (display mode, font size, color, background, alignment).
Equation Library: Save, load, search, rename, and delete equations. Persisted in IndexedDB.
Inline Insertion: Insert equations into text elements as $latex$ at the cursor position.
Image Tools

Upload: Store images as blobs in IndexedDB (no external hosting).
Crop Mode: Interactive crop rectangle with 8 resize handles, aspect-ratio lock (Shift), and double-click reset.
Fit to Image: Auto-size an image element to its natural dimensions.
Label Lines: Attach labels to images with draggable connection lines and endpoint handles.
Table Tools

Configurable Rows/Columns: Add or delete rows/columns; toggle header row/column.
Resize Handles: Drag column/row borders to resize proportionally.
Distribute: Evenly distribute selected rows or columns.
Cell Formatting: Per-cell text alignment, vertical alignment, font size, text color, and background color.
Keyboard Navigation: Arrow keys move between cells; Tab advances; Enter commits; Esc cancels.
Inline Math: Table cells render KaTeX ($...$ and $$...$$).
Shapes & Lines

Shapes: Rectangle, Line, Arrow with fill color, opacity, border, and rotation.
Endpoint Handles: Drag line/arrow endpoints; lock start or end to pivot rotation around a fixed point.
Rotation: Drag the rotation handle; snaps to 0°/90°/180°/270° within 5°.
Reset Endpoints: One-click restore to default orientation.
🎬 Presentation Mode

Full-Screen Delivery: Focused, distraction-free slide presentation.
Clock & Timer: Toggle a live clock and a start/stop/reset stopwatch.
Label Reveal: Reveal hidden text elements one at a time (R key or 🔍 button) or all at once (🔓).
Glossary Panel: Open a searchable glossary panel (📖) with terms, definitions, and Chinese translations.
Live Student Actions:

Take Attendance: 5-state segmented buttons (Present, Late, Absent–Unauthorized, Absent–Authorized, Absent–Medical) with instant save.
Award Points: Session-buffered point awarding with reason selection and live running totals.
Class Selection: Choose a class group from the toolbar to enable attendance and points actions.
Session Recording: Tracks time spent per slide and logs sessions for progress reports.
MCQ Reveal: Click MCQ answers to reveal correct/incorrect feedback.
Team Scoreboard: Interactive scoring with winner banner and game-end toggle.
📊 Student Management

Groups & Roster: Organize students into classes/groups. Add students manually or paste a list (one per line with optional Chinese name).
Student Detail View: Per-student tabs for Gradebook, Attendance, Quick Points, Progress, and Information.
Information Tab: Editable name, Chinese name, email, student ID, and notes.
Export Student Report: Generate a PDF report with assessment scores, attendance summary, and metrics.
Gradebook

Assessment Columns: Add/edit/remove assessment definitions with max score, category, and date.
Categories & Weights: Define weighted categories that sum to 100%.
Grade Scale: Fully configurable letter-grade thresholds (default: A*, A, B, C, D, F).
Category Averages: Automatic per-category averages for categories with ≥2 assessments.
Class Averages: Per-assessment and overall class means.
Keyboard Navigation: Arrow keys/Enter/Tab move between scores; Ctrl+D fills down.
Weighted Average & Letter Grade: Computed per student and displayed live.
Attendance

Session Model: Each attendance column is a (date, label) session — e.g. "2026-09-13 · Lesson 1".
5-State Cycle: Click a cell to cycle through Present → Late → Absent (Unauthorized) → Absent (Authorized) → Absent (Medical) → unset.
Recurring Schedule: Generate sessions from a start/end date + weekly weekday selection.
Date Range Filter: From/To date pickers plus Last 7 / Last 30 / All presets.
Bulk Actions: Set all students to Present / Late / Absent (with reason) for a selected session.
Summary Cards: Total days, attendance %, lates, and counts by absence reason.
Legend: Color-coded legend for all five states.
Notes: Optional per-record notes (displayed in tooltips).
Quick Points

Point Logs: Every award is logged with timestamp, amount, reason, source, and note.
Reasons: Participation, Behavior, Attitude, Homework, Quiz, Assignment, Presentation, Other.
Week/Month Summaries: Rolling 7-day and 30-day point totals.
Batch Award: Award points to every student in a group at once.
Delete Logs: Remove individual log entries with automatic total recalculation.
Merits System

Merit Conversion: Convert quick points into formal merits at a configurable rate (default: 3 points = 1 merit).
Merit Logs: Tracks merits awarded, points spent, rate, and source.
Merit Settings: Configure points-per-merit per course.
Direct Awards: Award merits without spending points when needed.
Progress Tracking

Session Logs: Each presentation session records date, start/end time, and per-slide time spent.
Resume: Resume a presentation from the last slide a group reached.
Session History: View all sessions with total time and per-session actions.
CSV Export: Export a session report with per-slide time breakdown.
Clear Progress: Reset all progress and session logs for a group.
💾 Data Persistence

All data (courses, slides, images, equations, templates, student records) is stored locally in your browser using IndexedDB.
No external database required; your data stays on your machine.
Auto-Save: Changes are debounced and saved incrementally (only dirty courses are written).
Migration: Automatically migrates data from the legacy LectureManagerDB_v2 database on first run.
🚀 Getting Started

Prerequisites

A modern web browser (Chrome, Firefox, Edge, Safari).
No server or internet connection is required (except to load external libraries via CDN).
Installation & Launch

Download the Ranlaoshi v1.0.9 Lite.html file.
Double-click the file to open it in your browser.
First Steps

Create a Course: Click the + button in the course selector.
Add a Lecture: Click ➕ Add ▾ → 📚 + Lecture in the sidebar.
Add a Topic: Click ➕ Add ▾ → 🗂 + Topic.
Add a Slide: Click ➕ Add ▾ → 📄 + Slide and choose a template.
Add Elements: Use the toolbar to add text, images, shapes, tables, or interactive exercises to the canvas.
Present: Click the ▶ Present button to view your slides in full-screen mode.
🧩 Slide Templates

Quick Start

Template	Description
Blank	Empty canvas with no elements.
Title	Large title and subtitle centered on the slide.
Text + Image	Image on the right, text on the left.
Advanced

Template	Description
Annotated Diagram	Centered image with 5 pre-placed labels ready for line attachment.
MCQ	Question with four answer options (A–D) marked as MCQ answers.
Fill in the Blanks	Passage with draggable word bank.
Matching	Two-column click-to-match exercise.
Glossary	Editable term/definition/Chinese table that can generate matching exercises.
True / False	Three statements with True/False buttons and answer checking.
Team Scoreboard	Two-team live scoring board with member management.
My Templates

Save any slide as a reusable template via File → 💾 Save as Template. My Templates appear in the Add Slide modal and can be renamed or deleted. Images are duplicated so each template is self-contained.

🧩 Dependencies

This project relies on the following open-source libraries (MIT license), all of which are loaded via CDN:

Library	Version	Purpose
html2canvas	1.4.1	Rendering slides for PDF export.
jsPDF	2.5.1	Generating downloadable PDFs of the lecture.
KaTeX	0.16.10	Rendering LaTeX equations in slides and the equation editor.
KaTeX mhchem	0.16.10	Chemistry notation support (\ce{}).
⌨️ Keyboard Shortcuts

Editor

Shortcut	Action
Ctrl + Z / Ctrl + Y	Undo / Redo
Ctrl + C / Ctrl + V / Ctrl + D	Copy / Paste / Duplicate (Element or Slide)
Delete / Backspace	Delete selected element
Arrow Keys	Move selected element by 1%
Ctrl + A (in Lectures view)	Select all slides in topic
Escape	Deselect element / clear slide selection
Shift / Ctrl + Click	Toggle multi-selection of elements
Shift + Click (table cell)	Expand rectangular cell selection
Ctrl + Enter (in text editor)	Insert line break with current bullet
Escape (in text editor)	Cancel inline edit
Table Editing

Shortcut	Action
Arrow Keys	Move between cells
Shift + Arrow	Extend cell selection
Tab	Move to next cell
Enter	Commit cell edit
Escape	Cancel cell edit
Presentation

Shortcut	Action
Arrow Right / Arrow Left	Next / Previous slide
R	Reveal next hidden label
Escape	Exit presentation mode
Gradebook

Shortcut	Action
Arrow Keys / Enter / Tab	Navigate between score cells
Ctrl + D	Fill down current value
🗂️ Project Structure (Single File Architecture)

Despite its extensive features, the entire application is contained within a single HTML file. The architecture follows a classic MVC pattern:

Data Layer: IndexedDB for persistent storage (courses, images, equations, UI state).
State Management: appState (persistent app state) and Session (transient UI state) objects manage runtime state, history (undo/redo), and transient UI states (drag, resize, edit, crop, presentation).
Rendering Layer: Property-driven renderers per element type (renderTableElement, renderMatchingElement, renderTrueFalseElement, renderTeamScoreboardElement, renderGlossarySlide, etc.).
Event Delegation: A central click handler dispatches all data-action attributes, keeping the code DRY and reducing listener churn.
Property Schemas: PROPERTY_SCHEMAS drives the properties panel — each element type declares which inputs map to which properties, enabling generic population and change handling.
Snapshots: Deep-cloned serializable snapshots power undo/redo while excluding volatile data (object URLs, DOM refs).

🤝 Contributing

This is an open-source project released under the MIT License. Contributions, issues, and feature requests are welcome!

Fork the repository.
Create your feature branch (git checkout -b feature/AmazingFeature).
Commit your changes (git commit -m 'Add some AmazingFeature').
Push to the branch (git push origin feature/AmazingFeature).
Open a Pull Request.
⚖️ License

Distributed under the MIT License. See the LICENSE file for more information.

Summary: You are free to use, modify, distribute, and sell this software, provided you retain the original copyright notice. This library uses external dependencies that are also under the MIT License.

📧 Contact

For questions, feedback, or support, please open an issue on the GitHub repository.

Happy Teaching! 🍎
