# N50_ANALYSER

**Genome Filtering Based on N50**  

This Python script, **n50_Analyse.py**, calculates the N50 value of FASTA files containing genomic sequences and filters these files, moving them to a separate directory if the N50 value is greater than or equal to a specified threshold. In this specific code, it filters genomes with **N50 ≥ 20 kb (20000).**  

### **Description**  

The script performs the following tasks:  

- **Calculate N50**: The N50 is a metric used to assess the quality and continuity of genomic sequences. It represents the contig (sequence fragment) size at which, when summing up larger contigs, 50% of the total sequenced bases are reached or exceeded.  
- **Filter Genomes**: The script checks the N50 value of each FASTA file in a specified directory and moves the files with an N50 value greater than or equal to a predefined threshold to a destination directory.  
- **Generate a Log**: A log file is created, recording the name of each file and its respective N50 value.  

### **Prerequisites**  

This script is designed to run on a **Linux** environment with **Python 3** installed.  

### **How to Use**  

#### **1. Make the Script Executable**  

Open a terminal, navigate to the directory where the `N50_Analyse.py` file is located, and make it executable with the following command:  

```bash
chmod +x n50_Analyse.py
```

#### **2. Run the Script**  

Before running, verify if **20 kb** is the desired threshold. If not, change the value in the following line:  

python
n50 = 20000


Replace it with the desired value.  

To execute the script, provide the path to the directory containing the FASTA files as an argument. The script will also create a directory named **N50** within the original directory, where the filtered files will be copied.  
```
bash

python n50_Analyse.py /path/to/fasta/files
```
Or, if using Python 3:  
```
bash
python3 N50_Analyse.py /path/to/fasta/files
```

#### **3. Execution**  

As the program runs, you will see the genome being processed and whether it meets the criteria for copying.  

**Example Output:**


File genome1.fna copied (N50 = 25000)
File genome2.fna copied (N50 = 30000)


At the end, a folder named **N50** will be created in the same location as the original FASTA files, containing the filtered files based on the specified criteria.
