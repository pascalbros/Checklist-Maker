# Checklist Maker

A lightweight, browser-based **procedure card and checklist editor** for creating clean, printable A5 checklists.

Build your checklist in the editor, preview the final layout live, and export it as **PNG or A5 PDF**. You can also save your checklist as Markdown and import it again later.

## ✨ Features

- 📝 Create and edit checklist titles and sections
- ➕ Add, remove, and reorder sections
- ☑️ Add checklist items with confirmation values
- 🎨 Customize section title colors
- 📐 Choose between **1, 2, or 3 columns**
- 📦 Switch between **Standard** and **Compact** density
- 👀 Live A5 print-card preview
- 📄 Export checklists as **A5 PDF**
- 🖼️ Export checklists as **PNG**
- 💾 Export checklist data as **Markdown (`.md`)**
- 📥 Import previously exported Markdown checklists
- 📱 Responsive editor layout for smaller screens
- 🌐 Runs entirely in the browser — no backend required

## 🚀 Demo

Because this is a static HTML application, it can be hosted on services such as:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Any standard web server

## 🛠️ Getting Started

### Run from GitHub

Run it [from here](https://pascalbros.github.io/Checklist-Maker)

### Run locally

No installation, build process, or local server is required.

Simply download or clone the repository and open `index.html` directly in your browser:

```text
checklist-maker/
├── index.html
└── README.md
```

You can either:

1. Double-click `index.html`, or
2. Right-click it and choose **Open with** your preferred browser.

The application runs entirely in the browser.

> **Note:** The app loads `html2canvas` and `jsPDF` from CDNs, so an internet connection is required for PNG and PDF export. The editor itself is otherwise client-side.

No build step or package installation is required.

## 📖 How to Use

### 1. Enter a checklist title

Give your checklist a descriptive title, for example:

```text
DRONES — NORMAL PROCEDURES
```

### 2. Add sections

Create sections such as:

- Before Leaving Home
- At the Flight Site
- Before Takeoff
- Before Landing
- After Flight

Each section can contain any number of checklist items.

### 3. Add checklist items

Every item contains two parts:

```text
Item                  Confirmation
-----------------------------------
Drone Batteries       CHARGED
Transmitter           CHARGED
GPS                   READY
Home Point            SET
```

The preview automatically formats these as a compact procedure card with dotted leaders.

### 4. Customize the layout

Choose:

- **1 column**
- **2 columns**
- **3 columns**

You can also switch between:

- **Standard**
- **Compact**

The application automatically distributes sections between columns based on their rendered height.

If the content no longer fits on one A5 page, the application displays an overflow warning.

### 5. Export

Use the export buttons to generate:

- **PNG** — useful for images and digital sharing
- **PDF · A5** — suitable for printing

You can also export the editable checklist as Markdown.

## 💾 Markdown Format

The application uses a simple Markdown-based format so checklists can be stored in Git and edited by hand.

Example:

```markdown
# Drones — Normal Procedures

## Before leaving home
- Drone Batteries :: CHARGED
- Transmitter :: CHARGED
- Drone :: CHECKED
- Goggles :: CHECKED

## At the flight site
- Weather :: CHECKED
- Airspace :: CHECKED
- Flight Area :: CLEAR

## Before takeoff [color=#1F3D2B]
- Propellers :: CHECKED
- Battery :: CONNECTED
- GPS :: READY
- Home Point :: SET
```

Section colors can optionally be stored using:

```text
[color=#RRGGBB]
```

The application also accepts `|` as an alternative separator when importing checklist items.

## 🧩 Technology

This project is intentionally simple and dependency-light.

### Frontend

- HTML5
- CSS3
- Vanilla JavaScript

### External libraries

The application loads:

- **html2canvas** — used to render the checklist preview for PNG/PDF export
- **jsPDF** — used to generate A5 PDF files

These libraries are loaded directly from CDN sources in the HTML file.

## 🏗️ Project Structure

```text
checklist-maker/
├── checklist-app.html
└── README.md
```

The application is currently implemented as a single self-contained HTML file containing the UI, styles, and JavaScript logic.

## 🔒 Privacy

Checklist content is processed locally in the browser.

There is no application backend, database, account system, or server-side checklist storage in the current implementation.

Exported Markdown files can be stored wherever you prefer, including directly in a Git repository.

## 🎯 Example Use Cases

Checklist Maker can be used for:

- Drone flight procedures
- Aviation procedure cards
- Equipment checklists
- Pre-operation inspections
- Workshop procedures
- Field-work checklists
- Photography equipment checklists
- Production and studio workflows
- Maintenance procedures
- Personal preparation checklists

## ⚠️ Limitations

The current application is intentionally lightweight.

- Checklist data is not automatically persisted between browser sessions.
- Import/export is based on the application's Markdown format.
- PDF and PNG generation happens in the browser.
- The application depends on the external CDN-hosted `html2canvas` and `jsPDF` libraries.
- The current preview is designed specifically around a single A5 portrait page.

## 🤝 Contributing

Contributions are welcome.

If you'd like to improve the project:

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/my-improvement
```

3. Make your changes
4. Test the application in a browser
5. Commit your changes

```bash
git commit -m "Add my improvement"
```

6. Push the branch

```bash
git push origin feature/my-improvement
```

7. Open a Pull Request

## 📄 License

Add your preferred open-source license here.

For example, if you choose the MIT License:

```text
MIT License
```

See the repository's `LICENSE` file for the complete license text.

---

**Checklist Maker** — create clean, printable procedure cards directly in your browser.