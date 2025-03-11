# Fetch_Research_papers

# README: PubMed Research Paper Extractor

## 1. Overview
This Python script retrieves research papers from PubMed, extracts key metadata, filters for non-academic authors affiliated with biotech or pharmaceutical companies, and exports the results as a CSV file. It is designed to work in both local environments and Google Colab.

## 2. Code Organization
- **`fetch_pubmed_papers(query, max_results=50)`**: Fetches research papers from PubMed.
- **`extract_paper_info(papers)`**: Extracts and filters relevant metadata.
- **`save_to_csv(data, filename)`**: Saves the extracted data to a CSV file.
- **`main()`**: Handles command-line argument parsing and program execution.
- **Google Colab Detection**: The script detects if it is running in Google Colab and modifies execution accordingly.

## 3. Installation
To run this script, you need Python installed along with the required dependencies.

### **3.1 Install Python Dependencies**
Use `pip` or `Poetry` to install the required libraries:
```sh
pip install biopython pandas
```
OR, if using Poetry:
```sh
poetry add biopython pandas
```

## 4. Running the Script
You can execute the script from the command line using:
```sh
python script.py --query "biotech OR pharma" --file output.csv
```
### **4.1 Available Command-Line Options**
- `-h` or `--help`: Display usage instructions.
- `--query <query>`: PubMed query string (required).
- `-d` or `--debug`: Enable debug mode to print execution details.
- `-f` or `--file <filename>`: Specify output CSV file. If omitted, results print to the console.

## 5. Tools & Libraries Used
- **BioPython**: For PubMed API interaction ([link](https://biopython.org/)).
- **Pandas**: For handling and exporting tabular data ([link](https://pandas.pydata.org/)).
- **Regular Expressions (Regex)**: For filtering author affiliations.
- **LLMs**: Assisted in refining API queries, optimizing regex filtering, and improving CLI usability.

## 6. Execution in Google Colab
If running inside Google Colab, simply execute:
```python
!python script.py
```
The script defaults to fetching biotech and pharma-related papers and saves results in `pubmed_results.csv`.
