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


---

## Installation

### 1. Clone the repo

