# imgs2pdfs

A simple Python tool to convert images into PDF files and merge multiple PDFs.

------

## Features

- Convert multiple images into a single PDF
- Batch generate PDFs from folders
- Merge multiple PDFs into one
- Automatic file sorting (natural order)

------

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/imgs2pdfs.git
cd imgs2pdfs
```

Install dependencies:

```bash
pip install -r requirements.txt
```

------

## Project Structure

```
imgs2pdfs/
│
├── media/
│   ├── Picture/       # Input images
│   ├── PDF/           # Generated PDFs
│
├── imgs2pdfs.py       # Core logic
├── main.py            # Example usage
└── requirements.txt
```

------

##  Usage

### 1. Generate PDF from folders

Put your image folders inside:

```
media/Picture/
```

Each folder will be converted into a PDF.

```python
import imgs2pdfs

a = imgs2pdfs.PDFGener.list_read()
a.gene_from_file("output_name")
```

------

### 2. Generate PDF from images

Put images directly inside:

```
media/Picture/
a = imgs2pdfs.PDFGener(["1.jpg", "2.jpg"])
a.gene_from_pic("output_name")
```

------

### 3. Merge PDFs

Put PDFs inside:

```
media/PDF/
a = imgs2pdfs.PDFCombiner.list_read()
a.PDF_combiner("merged_name", 1, 3)
```

Parameters:

- `merged_name`: output file name
- `1`: starting index
- `3`: number of PDFs per merged file

------

##  Notes

- Only `.jpg` / `.jpeg` images are supported
- Output PDFs are saved in `media/PDF/`
- Merged PDFs are saved in `media/PDF/Combined PDF/`

------

## 📦 Requirements

- Python 3.8+
- Pillow
- PyPDF2

Install manually:

```bash
pip install Pillow PyPDF2
```

------

## 🛠️ Example

Run:

```bash
python main.py
```

------

