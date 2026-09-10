# Experiment 2 – Identification of Distantly Related Homologous Sequences Using PSI-BLAST

## Aim

To utilize Position-Specific Iterative BLAST (PSI-BLAST) to identify distantly related homologous sequences of a given query protein sequence.

---

## Objectives

* To understand the principles of PSI-BLAST for detecting remote sequence similarities.
* To perform a PSI-BLAST search using the NCBI protein database.
* To analyze the results and identify potential homologs of the query protein.
* To evaluate the reliability of identified homologs based on E-value and sequence conservation.

---

## Introduction

Protein BLAST (blastp) is commonly used to identify homologous proteins based on sequence similarity. However, standard BLAST may not effectively detect distantly related proteins having low sequence identity.

PSI-BLAST (Position-Specific Iterated BLAST) improves the sensitivity of sequence searching by constructing a Position-Specific Scoring Matrix (PSSM) from the results of the initial search.

In each iteration, the PSSM is refined using aligned sequences. This allows PSI-BLAST to detect remote homologs that may have low sequence identity but can still share structural or functional relationships.

PSI-BLAST is useful in comparative genomics, protein family analysis, and protein function prediction.

---

## Query Protein

**Protein:** Cytochrome P450 4B1

**Organism:** Homo sapiens (Human)

**Gene:** CYP4B1

**UniProt Accession:** P13584

**Sequence Format:** FASTA

---

## Tools and Databases Used

* **UniProt** – Retrieval of the query protein sequence in FASTA format
* **NCBI PSI-BLAST** – Identification of homologous protein sequences
* **NCBI nr Database** – Non-redundant protein sequence database (specifically ClusteredNR)
* **NCBI Conserved Domains / Graphic Summary** – Identification of conserved domains

---

## Parameters Used

| Parameter | Value |
| --- | --- |
| Search Tool | PSI-BLAST |
| Database | ClusteredNR (clustered_nr) |
| E-value Threshold | 0.005 |
| Number of Iterations | 4 (completed 3 rounds of results) |
| Query Type | Protein |
| Query Format | FASTA |

---

## Procedure

### 1. Query Protein Preparation

1. Open UniProt.
2. Search for the selected Cytochrome P450 protein.
3. Open the appropriate protein record.
4. Download or copy the protein sequence in FASTA format.

### 2. Running PSI-BLAST

1. Open the NCBI Protein BLAST webpage.
2. Enter the query protein sequence in the query box.
3. Select **PSI-BLAST** as the search algorithm.
4. Select the **ClusteredNR (clustered_nr)** database.
5. Set the E-value threshold to **0.005**.
6. Set the number of iterations to **3**.
7. Start the BLAST search.
8. Record the important results from Iteration 1.

### 3. PSI-BLAST Iterations

1. Examine the significant hits obtained from the first iteration.
2. Select appropriate sequences for inclusion in the next iteration.
3. Run **PSI-BLAST Iteration 2**.
4. Continue the analysis up to **Iteration 3** (or further depending on convergence).
5. Compare the number and diversity of hits obtained between the iterations.

### 4. Conserved Domain Analysis

1. Examine the **Graphic Summary** section.
2. Examine the **Conserved Domains** information.
3. Record the conserved domains identified in the query protein.
4. Save screenshots of the relevant results.

### 5. Result Comparison

Compare the PSI-BLAST results with standard blastp results using the same query sequence.

The comparison should consider:

* Number of significant hits
* E-values
* Percentage identity
* Query coverage
* Detection of distant homologs
* Conserved domains

---

## Screenshots

The following screenshots document the major steps of the analysis:

**1. Query Protein**


**2. FASTA Sequence**


**3. PSI-BLAST Input Parameters**


**4. Iteration 1 Results**


**5. Iteration 2 Results**


**6. Iteration 3 Results**


---

## Results

PSI-BLAST was used to search the NCBI clustered_nr protein database for homologous sequences of the selected Cytochrome P450 4B1 protein.

The results obtained from each iteration were recorded based on:

* Number of hits
* E-value
* Percentage identity
* Query coverage
* Newly detected homologs
* Conserved domains

### Observation Table

| Iteration | Number of Hits | Representative E-value | % Identity Range | Query Coverage Range | New Homologs |
| --- | --- | --- | --- | --- | --- |
| Iteration 1 | 500 | 0.0 | ~85.13% - 100.00% | 98% - 100% | Base Homologs Established |
| Iteration 2 | 500 | 0.0 | ~83.56% - 100.00% | 98% - 100% | Sequences added to build PSSM |
| Iteration 3 | 500 | 0.0 | ~59.45% - 100.00% | 98% - 100% | Distant homologs identified (e.g., 59.45% identity hit KAN4279789.1) |

### Conserved Domains

**Domain identified:** Cytochrome P450 family domain

**Domain information:** This domain is conserved across the sequences and is responsible for the core catalytic function of the P450 enzymes. *(Note: Complete domain visualization requires checking the Graphic Summary/Conserved Domains tab in the NCBI output).*

---

## Interpretation

PSI-BLAST provides increased sensitivity compared with standard blastp for identifying distantly related homologous sequences.

As the iterations proceed, the position-specific profile is refined and may identify additional sequences with lower sequence identity. This was successfully demonstrated by Iteration 3, where distant hits with percent identities dropping into the 50-60% range (e.g., 59.45% for uncharacterized protein FRY00_015135) were identified with high confidence (E-value 0.0).

The E-values and sequence conservation should be monitored carefully during each iteration to avoid the inclusion of false-positive sequences and profile drift.

Convergence of the PSI-BLAST profile indicates that no significant new homologous sequences are being detected.

---

## Conclusion

PSI-BLAST was successfully performed for Cytochrome P450 4B1 (Homo sapiens) using the NCBI ClusteredNR database.

The iterative search helped identify homologous protein sequences and analyze their sequence similarity, expanding detection from close relatives (85%+ identity) in the first iteration to much more distant homologs (~59% identity) by the third iteration.

The experiment demonstrated the usefulness of PSI-BLAST for detecting distantly related homologous proteins that may not be identified effectively using standard blastp alone.

---

## References

* UniProt: [https://www.uniprot.org/](https://www.uniprot.org/)
* NCBI BLAST: [https://blast.ncbi.nlm.nih.gov/](https://blast.ncbi.nlm.nih.gov/)
* NCBI Conserved Domains Database: [https://www.ncbi.nlm.nih.gov/Structure/cdd/](https://www.ncbi.nlm.nih.gov/Structure/cdd/)
