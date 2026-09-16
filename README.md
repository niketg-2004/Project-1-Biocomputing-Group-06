# Project 1 - Biocomputing

## Group 06

## Project Workflow

1. Selected genes according to the categories assigned to the group members.
2. Searched the NCBI nucleotide database for the selected genes with and without the filter .
3. Identified the required sequence records and accession numbers.
4. Retrieved the required nucleotide record for the required gene.
5. Retrieved the GenBank record for the required gene.
6. Retrieved the protein Sequence record for the required gene.
7. Stored the retrieved FASTA and GenBank in the `data/` folder.
8. Stored the juypter notebook used for the analysis in the `scripts/` folder.
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
response = requests.get(base, params=params)
response.text
```

## Group Member Assignment

| Group Member | Category | Gene |
|---|---|---|
| Niket Gindodiya | A | MSRB1 |
| Ridhanya K B | B | MTND1 |
| Gargi Yadhav | C | ACTB |
