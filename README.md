# Osteo-Fine-Mapp-SNP2SE2miRNA

This tool could help users to detect potential long-range effects of genome-wide SNPs on miRNA via super-enhancers in human osteoblast. Users could take a list of SNPs of interest as input, such as SNPs from GWAS summary results.


Use the follow command to download:

	$ git clone https://github.com/Zheng-Lab-Westlake/Osteo-Fine-Mapp-SNP2SE2miRNA.git 

Please run the follow command to to see the help message:

	$ python ./FineMapp_SNP2SE2miRNA.py -H
	
Arguments:
	
	-H/-h	show this help message and exit.

	-SNP	The INDEPENDENT SNPs file, which consists of at least three tab-separated
		columns: chromosome, position and P-value. Extra columns are allowed, but
		the first two columns must be chromosome (1-22, X, Y) and position (in hg19). 
	
	-PCol	Columns name of P-value in the SNP input file.
	
	-outPrefix	Prefix for output results.

An example is given, run it in the command line for details:

	$ sh example.sh
	
Output:

	-mapping.tsv, results of SNPs mapping to SEs.
	-mappedSE-Bonferroni_sig.tsv, mapped SEs with P < 0.05/1224.
	-Interaction_SE2miRNA.tsv, interactions between miRNA and SE.
	-SE-interacted_pri-miRNA.txt, SE-interacted pri-miRNAs.
	-SE-interacted_mature-miRNA.txt, mature miRNAs.



 Note that the step of long-range interaction identification between Super-Enhancer and miRNA may take a while. 


