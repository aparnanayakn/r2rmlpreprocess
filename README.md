# r2rmlpreprocess

This repository contains 3 directories. 

#####  1. Extracting LT : 
This directory contains 2 pythons files.  

a. extractLG : This code helps to scrape the language tags from w3schools website. 

b. convertToTag : Sample testing code that converts language to tags if any.

#####  2. DT prediction:
This directory contains preprocessing steps required to generate typed literals. 

a. Annotations : Contains all the testcases considered in the experiment. The testcases include RML testcases and scenarios given by KGC workshop that is colocated in ESWC 2021. RML testcases are modified to add language tag and datatype. 

b. Challenge patterns : Contains the testcases given by KGC workshop. 

c. Individual : Contains all the RML test cases that has single JSON object. 

d. Repeated patterns: Contains all the RML test cases that has multiple JSON objects. 

e. Testanno: Contains CSV output that is generated from JSON files after preprocessing.

f. Dtlgprediction : Code that is responsible to preprocess the data i.e. to convert language tags and datatype in appropriate format or to infer datatype. 

 
#####  3. r2rml
This directory contains java code that is responsible to map CSV/RDB to RDF. It reads the preprocessed files that is preprocessed in DT prediction. 

Java code can be compiled with following commands. 

*mvn clean*

*mvn package*

*mvn dependency:copy-dependencies*

Once the code is compiled, following command can be used to generate RDF by considering the input and correspondng mapping file. 

*java -jar ./target/r2rml.jar configurationfile*

Configuration file includes input file that is to be processed, mapping file, output file that is to be generated and the format that will be used to generate output. 





References 

i. https://rml.io/test-cases/  

ii. https://github.com/chrdebru/r2rml

iii. https://github.com/kg-construct/mapping-challenges/tree/main/challenges/
