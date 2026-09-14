# Project 1 - Biocomputing

## Group 06

## Project Workflow

1. Selected genes according to the categories assigned to the group members.
2. Searched the NCBI nucleotide database for the selected genes.
3. Identified the required sequence records and accession numbers.
4. Retrieved the required nucleotide and protein sequences.
5. Retrieved the GenBank record for the required gene.
6. Stored the retrieved FASTA and GenBank in the `data/` folder.
7. Performed the required analysis using Python.
8. Stored the Python notebook used for the analysis in the `scripts/` folder.
9. Stored the output files and Q4 summary table in the `results/` folder.

## NCBI Search and Retrieval

The NCBI E-utilities were used to search and retrieve sequence information.

### NCBI Search

```python
import requests

base = "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi"

params = {
    "db": "nuccore",
    "term": "MSRB1",
    "retmode": "text"
}
## Group Member Assignment

| Group Member | Category | Gene |
|---|---|---|
| Niket | A | MSRB1 |
| RB | B | MTND1 |
| Gargi | C | ACTB |

response = requests.get(base, params=params)
response.text
