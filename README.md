# 🧑‍🏫 Ranlaoshi - Interactive Lesson Authoring Tool

**Version:** v1.0.1 Lite  
**Date:** 2026-08-23  

**Ranlaoshi** is a powerful, single-page HTML application that lets teachers build, customize, and deliver interactive lessons entirely within their browser. No server, no accounts, no installations—just pure HTML, CSS, and JavaScript.

It combines a drag-and-drop slide editor with a comprehensive student management system (gradebook, attendance, points) and an immersive presentation mode.

![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)

---

## ✨ Key Features

### 🛠️ Slide Editor
- **Rich Canvas Elements**: Add and manipulate **Text**, **Images**, **Shapes** (Rectangles, Lines, Arrows), **Tables**, **Equations** (LaTeX), **Video Embeds**, and **Labels**.
- **Drag & Drop**: Intuitive movement with **snap-to-grid** and alignment guides for pixel-perfect layouts.
- **Interactive Exercises**:
  - **Multiple Choice Questions (MCQ)**: Mark correct answers and reveal them during presentation.
  - **Fill-in-the-Blanks**: Drag-and-drop words from a word bank into the passage.
  - **Matching Exercises**: Click to match items from one column to another.
- **Equation Editor**: Live LaTeX preview with a built-in equation library to save and reuse formulas.
- **Glossary Slides**: Create term-definition tables that students can access during presentations.

### 🎯 Presentation Mode
- **Full-Screen Delivery**: Focused, distraction-free presentation of your slides.
- **Clock & Timer**: Keep track of time with a visible clock and stopwatch.
- **Label Reveal**: Configure labels to appear one by one (e.g., for diagram annotation).
- **Live Student Actions**: Take attendance and award points to selected student groups in real-time.
- **Glossary Access**: Students can pull up the slide's glossary on demand.

### 📊 Student Management
- **Groups & Roster**: Organize students into classes/groups.
- **Gradebook**: Create weighted assessment categories and enter scores directly.
- **Attendance**: Mark daily attendance with bulk actions and date filters.
- **Quick Points**: Award points to individuals or entire batches with custom reasons.
- **Progress Tracking**: Automatically logs presentation sessions to track student progress.

### 💾 Data Persistence
- All data (courses, slides, images, equations, student records) is stored locally in your browser using **IndexedDB**.
- No external database required; your data stays on your machine.

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari).
- No server or internet connection is required (except to load external libraries via CDN).

### Installation & Launch
1. Download the `Ranlaoshi v.1.0.1 lite.html` file.
2. Double-click the file to open it in your browser.

### First Steps
1.  **Create a Course**: Click the `+` button in the course selector.
2.  **Add a Lecture**: Click `+ Lecture` in the sidebar.
3.  **Add a Topic**: Click `+ Topic` inside the lecture.
4.  **Add a Slide**: Click `+ Slide` and choose a template (e.g., "Blank", "Title", "MCQ").
5.  **Add Elements**: Use the toolbar to add text, images, shapes, tables, or interactive exercises to the canvas.
6.  **Present**: Click the **▶ Present** button to view your slides in full-screen mode.

---

## 🧩 Dependencies

This project relies on the following open-source libraries (MIT license), all of which are loaded via CDN:

| Library | Version | Purpose |
| :--- | :--- | :--- |
| **html2canvas** | 1.4.1 | Rendering slides for PDF export. |
| **jsPDF** | 2.5.1 | Generating downloadable PDFs of the lecture. |
| **KaTeX** | 0.16.10 | Rendering LaTeX equations in slides and the equation editor. |

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| `Ctrl + Z` / `Ctrl + Y` | Undo / Redo |
| `Ctrl + C` / `Ctrl + V` / `Ctrl + D` | Copy / Paste / Duplicate (Element or Slide) |
| `Delete` / `Backspace` | Delete selected element |
| `Arrow Keys` | Move selected element by 1% |
| `Arrow Up/Down` (in Lectures view) | Navigate to previous/next slide |
| `Esc` | Exit presentation mode or deselect element |

---

## 🗂️ Project Structure (Single File Architecture)

Despite its extensive features, the entire application is contained within a single HTML file. The architecture follows a classic MVC pattern:
- **Data Layer**: IndexedDB (via `idb` API) for persistent storage.
- **State Management**: `appState` and `Session` objects manage runtime state, history (undo/redo), and transient UI states (drag, resize, edit).
- **UI Layer**: Dynamically rendered `#sidebar`, `#canvas`, and properties panels based on the current state.

---

## 🤝 Contributing

This is an open-source project released under the MIT License. Contributions, issues, and feature requests are welcome!

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## ⚖️ License

Distributed under the **MIT License**. See the `LICENSE` file for more information.

**Summary**: You are free to use, modify, distribute, and sell this software, provided you retain the original copyright notice. This library uses external dependencies that are also under the MIT License.

---

## 📧 Contact

For questions, feedback, or support, please open an issue on the GitHub repository.

**Happy Teaching!** 🍎
