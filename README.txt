Submitted by: 
Avishek De
Pranjali Jain

name of this directory : PranjaliJain/IDCM

Dataset : 
- dataset name : TREC 45 
- present in : PranjaliJain/IDCM/data/
- dataset files : trec45-processed.xml (if not present in IDCM/data folder, copy from /cs/sandbox/faculty/tyang/290N/trec45-processed.xml)
                : queries.txt
                : qrels.trec6-8.nocr
                : trec45_indri_kstem_top1000_bm25.out 
                (- all these files can be obtained from the HW1 zip file present here : https://sites.cs.ucsb.edu/~tyang_class/293s21f/hw/hw1-2021/hw1-starter.tar.gz)
- to create csv file of documents from the xml file : use the convert_data_to_csv.ipynb file
    - output of this file : trec45-documents.csv
- data/trec45-documents.csv has these columns:
    DOCNO:string, HEADLINE:string, TEXT:string 
    

Code: 
- present in : PranjaliJain/IDCM/code/
- files : convert_data_to_csv.ipynb
        : idcm_eval.ipynb
- convert_data_to_csv.ipynb : converts the data in trec45-processed.xml to csv format with document text
- idcm_eval.ipynb : 
    - tests the idcm model on trec45 dataset 
        - 150 queries
        - IDCM ranking performed on top-100 documents ranked by BM25 obtained from data/trec45_indri_kstem_top1000_bm25.out
    - compares the idcm model's efficiency in terms of time required with ColBERT, BERTCAT and BERTDOT


To Run: 
- Run the .ipynb files with jupyter notebook 