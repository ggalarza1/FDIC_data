# FDIC_data
This repository explores the data from the Federal Deposit Insurance Corporation (FDIC) using the API and the FDICDataPy.

# Installation
```
pip install fdicdata

```

# Data Exploration

This code comes from this repository: https://github.com/Visbanking/fdicdataPy/tree/main?tab=readme-ov-file.
I've modified it to explore the data a bit more. As well create my own findings.

```
import fdicdata as fdic

### Data Taxonomy:
fdic.dataTaxonomy("institution")

### Get Failures:
fdic.getFailures(['CERT'], date_range=('2010','2015'), name=("DORAL BANK"))

### Get Financials:
fdic.getFinancials(IDRSSD_or_CERT=37, metrics=["ASSET", "DEP"], limit=10, date_range=["2015-01-01", "*"])

### Get History:
fdic.getHistory(CERT_or_NAME=3850, fields=["INSTNAME", "CERT", "PCITY", "PSTALP", "PZIP5"], CERT=True, limit=10)

### Get Institutions:
fdic.getInstitution(IDRSSD_or_CERT='480228', fields=["NAME", "CITY", "STATE"], limit=10)

### Get Institutions All:
fdic.getInstitutionsAll()

### Get Location:
fdic.getLocation(3850)
fdic.getLocation(3850, fields=['NAME', 'CITY', 'ZIP'])

### Get Summary:
fdic.getSummary(states = ["California", "New York"], date_range= ["2020", "2021"], fields =  ["DEP", "ASSET"])
```
