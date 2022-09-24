#Multiple Sequence Alignment

A program developed to find multiple sequence alignment of protein sequences read from input files.  
Global alignment was performed to find pairwise alignments.  
Gap values are taken as input from the user.  
Match and mismatch scores are taken from the BLOSUM62 matrix.  
After all pairwise alignments have been performed, a similarity score is created for each pairwise alignment. Using these scores, a similarity matrix of kxk size was created.  
&emsp;Similarity Score (si , sj ) = # of exact matches / aligned sequence length  
Using the similarity matrix, a guide tree was created with the neighbor joining algorithm, which is one of the distance based tree building methods.  
&emsp;Q(i,j) = (r−2)∗d(Ci, Cj) – u(Ci) – u(Cj)  
&emsp;r is the number of clusters.  
&emsp;Q(i,i) = 0 for all i.  
The most similar alignments were merged by backtracking in the order found in the guide tree.
