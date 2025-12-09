# grycon

Graph-based (GCN) malware analysis tool for PDF and Office documents (Word / Excel).  
Grycon takes a document, extracts static features (entropy, URLs, JavaScript, VBA, embedded objects, etc.), runs them through a PyTorch model and prints:

- verdict: `malicious` or `benign`
- confidence score
- MD5 / SHA1 / SHA256
- detected MIME type and model mode
- short reason (with p_mal)
- feature dump and tags for explainability

---

## Features

🧾 **Supported formats**: PDF, RTF, DOC/DOCX/DOCM, XLS/XLSX/XLSM/XLAM.
🔐 **Strict MIME validation**:
  - Signature-based detection (PDF/RTF/OLE/OOXML).
  - Rejects unsupported types.
🧮 **Static feature extraction**:
  - file size (log scale)
  - Shannon entropy
  - printable/ASCII ratio
  - number of URLs
  - JavaScript/OpenAction markers (PDF)
  - VBA and embedded objects
  - suspicious tokens (e.g. PowerShell, `xor`)
  - high-bytes ratio
🌈 **CLI UX**:
  - Colored output via `colorama` (can be disabled with `--no-color`).
  - Verbosity levels `-v`, `-vv`.
  - Execution time measurement.

---

## Installation

### 1. Clone the repo

