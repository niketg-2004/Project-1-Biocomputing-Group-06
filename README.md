# Project 1 - Biocomputing

## Group 06

## Project Workflow

1. Selected genes according to the categories assigned to the group members.
2. Searched the NCBI nucleotide database for the selected genes with and without the filter .
3. Retrieved the required nucleotide record for the required gene.
5. Retrieved the GenBank record for the required gene.
6. Retrieved the protein Sequence record for the required gene.
7. Extract the header from each of the all file.
8. Using the CDS coordinate extract the mRNA.
9. Used the one word for the each genetic code
10. compare the deposited and protein and identify the difference.  
11. Stored the retrieved FASTA and GenBank in the `data/` folder.
12. Stored the juypter notebook used for the analysis in the `scripts/` folder.
13. Stored the output files and Q4 summary table in the `results/` folder.

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
response = requests.get(base, params=params)
response.text
```

## Group Member Assignment

| Group Member | Category | Gene |
|---|---|---|
| Niket Gindodiya | A | MSRB1 |
| Ridhanya K B | B | MTND1 |
| Gargi Yadhav | C | ACTB |
