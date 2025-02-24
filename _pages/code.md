---
permalink: /code/
title: "Code/Data"
excerpt: "Code/Date"
author_profile: true
redirect_from: 
- /data/
---

This page is mostly for self-use. Codes are available upon request. If you see some of your code, please feel free to contact me to credit you appropriately.

## Code for research projects

- Python snippet to load WRDS data into pandas DataFrame 

- Python snippet to load data from the FRED API to pandas DataFrame

- Python snippet to load data from the BEA API to pandas DataFrame

- Decently fast financial beta computation in native Python

- The Zero-Beta Rate (2023): replication code in Python for portfolio construction and GMM estimation, available upon approval from the authors

- Code for the computation of maximin priors and minimax rules (Kempthorne (1987) and Chamberlain (2000))

## Useful datasource

- Macro/Finance: WRDS, FRED, BEA

## Useful bits of code

- Unix shell

```
f='file.djvu'
pg=$(djvused -e 'n' $f)
for i in $(seq 1 $pg)
do
    djvu2hocr -p $i $f | sed 's/ocrx/ocr/g' > `printf "pg%04d.html" $i`
    ddjvu -format=tiff -page=$i $f `printf "pg%04d.tiff" $i`
done
pdfbeads -o ${f/djvu/pdf}
```
```
for i in *.jpg; do
  convert $i -quality 30 $i.pdf
done;

pdfunite $(ls -v *.pdf) output.pdf;
```
```
pdftk {1..20}.pdf cat output out.pdf
```
```
wget -r -A "*.pdf" "https://example.html"
```