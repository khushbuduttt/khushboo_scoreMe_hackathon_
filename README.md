# Hackathon-Assignment-Detecting-and-Extracting-Tables-from-PDFs
PDF Table Extractor
PDF Table Extractor is a Python-based tool that extracts tables from PDF files and converts them into structured Excel sheets. This tool does not rely on Tabula or Camelot and supports various table structures, including regular, irregular, and borderless tables.
1. Extracts tables from PDFs using pdfplumber and PyPDF2
2. Handles irregular tables using custom extraction techniques
3. Detects and corrects rotated pages before extraction
4. Cleans and structures extracted tables
5. Exports tables to Excel (.xlsx)
6. Provides a Streamlit UI for easy interaction

Installation
Before running the tool, install the required dependencies:
pip install pdfplumber PyPDF2 pandas openpyxl streamlit base64
Usage
1Running in Jupyter Notebook
If you want to run the script in Jupyter Notebook without the Streamlit interface, use the following:
from pdf_extractor import extract_tables_from_pdf ## pdf_extractor is file with the name: assignment_PEC_scoreme_21103106.
pdf_path = "sample.pdf"  # Change this to your PDF file
output_path = "output.xlsx"
dfs, success = extract_tables_from_pdf(pdf_path, output_path)
if success:
    print("Tables extracted and saved to", output_path)
else:
    print("No tables found.")
2Running as a Streamlit Web App
To launch the Streamlit-based UI, run:
streamlit run pdf_extractor.py
Open the link in your browser.
Upload a PDF file.
Extract and download the tables in Excel format.
Folder Structure
PDF-Table-Extractor
pdf_extractor.py : Main script
README.md:           Project documentation
requirements.txt:    List of dependencies
  pdfs :           Folder to store input PDFs
  output:          Folder to store extracted Excel files



After processing, extracted tables are saved as Excel files in the output/ folder, each sheet containing a table from the PDF.

