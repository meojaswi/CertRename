# Manifest (or Unbulk) // The Last-Mile Certificate Matrix Utility

A blazing fast, **100% client-side browser utility** designed to solve the painful "last mile" of bulk certificate generation. 

When generating certificates at scale using tools like Canva Bulk Create, Adobe InDesign, or Google Slides Mail Merge, you are typically left with two flawed options upon export: a single massive multi-page PDF, or a ZIP folder of generic, sequentially numbered images/PDFs (`Untitled_1.pdf`, `Untitled_2.pdf`). Organizers are then forced to open every single file, read the name, and manually rename them before distribution.

**Manifest** bridges this exact gap. It acts as the tool-agnostic missing link: upload your exported certificate assets along with the original participant spreadsheet, match them deterministically by row order via an interactive alignment ledger, and download a perfectly organized ZIP archive with custom, structured filenames in seconds.

---

## ⚡ Key Features

- **Zero-Backend Architecture:** Built entirely with client-side JavaScript processing engines (`pdf-lib`, `JSZip`, `PapaParse`, `SheetJS`). Your files **never** leave your local computer. 
- **Absolute Data Privacy:** 100% secure by design. Ideal for educational institutions, corporations, and fests handling sensitive student/participant parameters.
- **Deterministic Alignment Ledger:** Includes a split-screen matrix view that maps each spreadsheet entry to its corresponding document frame or file node. Cross-reference row 1 with page 1 explicitly before pulling the trigger—preventing layout or naming mismatches.
- **Smart Matrix Mapping:** Seamlessly extracts text columns (e.g., `Full Name`, `Registration ID`) to instantly synthesize dynamic, production-ready filenames.
- **Tool-Agnostic Engine:** Works flawlessly whether your files come from Canva, Figma, InDesign, Microsoft Word, or PowerPoint. Accepts a multi-page PDF or a ZIP archive of images/PDFs.

---

## 🛠️ The Technology Stack

- **Core Structure:** HTML5 / CSS3 (Self-contained, ledger-inspired minimalist aesthetic using system-serif typography)
- **PDF Manipulation:** `pdf-lib` (Extracts, isolates, and splits discrete binary byte streams in browser memory)
- **Decompression & Archiving:** `JSZip` (Asynchronously parses incoming ZIPs and compiles the renamed package)
- **Data Parsing:** `PapaParse` (For lightweight RFC 4180 compliant CSV parsing) & `SheetJS / xlsx` (For reading Excel binary sheet streams directly)

---

## 📦 Local Deployment & Usage

Because Manifest is a completely self-contained browser utility, it requires zero server setup, zero node modules, and no external dependencies. 

### Option 1: Quick Run
1. Download the `manifest.html` file from this repository.
2. Double-click the file to open it directly in **any** modern web browser.
3. Use it entirely offline if desired.

### Option 2: Production Hosting
Simply drop the `manifest.html` file into GitHub Pages, Vercel, Netlify, or Cloudflare Pages. It costs **$0/month** to scale to millions of users since all computing overhead is distributed directly to the user's browser client.

---

## 🧭 How It Works (Step-by-Step)

1. **Upload Assets:** Drop in your single multi-page PDF or your ZIP archive containing your sequentially ordered certificates.
2. **Bind the Ledger:** Upload the exact same CSV or Excel sheet used during your initial generation phase.
3. **Map the Target:** Select the specific column header representing the naming parameter (e.g., `Full Name`).
4. **Audit the Matrix:** Use the **Structural Alignment Matrix** to verify page numbers line up perfectly with recipient names.
5. **Execute:** Click `Execute Batch Renaming & Compile ZIP Archive`. The browser will download a clean ZIP archive with customized filenames ready for distribution pipelines.

---

## 🎯 Portfolio & Project Context

This project serves as an architectural case study in building **Workflow Wedges** and **Client-Side Micro-utilities**. Instead of over-engineering a heavy, database-driven full-stack application with authentication and cloud storage overhead, Manifest solves a real-world, high-friction bottleneck with zero hosting footprint, absolute data privacy, and zero infrastructure costs. 

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.