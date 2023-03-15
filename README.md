# Problem_Set_9

This week we learned how to build and test Hidden Markov Models (HMM)
HMMs are very useful in biological, genomic, and proteomic investigations. 

## Problem 1 - Construct the Transmission and Emission matrices. 

![lab_model](https://user-images.githubusercontent.com/47755288/225417771-6d96f8af-61c4-4321-b07f-243674a64eab.png)

One use of HMMs is to model genomic content to identify genes within genomes. The above is a simplifed version of this idea. 
The top part of the diagram is a Markov Chain that represents various parts of genes. Any transition (arrow) not shown is zero (0). 
These states are _hidden_ .

The bottom part of the diagram is the emissions from each hidden state. These are represented by codons. We can sample the codons along a genomic sequence. We have three different codon possibilites: Start Codon, Other Codon, Stop Codon. 

In this case the codon depends _only_ on the hidden state. Below each hidden state is the emission probability for each of our three possible observations 

**Build the transmission and emission matrices from this diagram**


## Problem 2 - Probability of our observation (2 points)

Let's imagine we sample a DNA sequence which would have the RNA sequence below (aka you don't need to transcribe it) 

**ACU  AAA  AUG  AUG  GCG  UGA  UUU**

_Reminder: AUG is start. Stop is UAA, UAG, or UGA_

In this case we are going to assume that **we start at an intergenic hidden state**
Use the approrpiate command in the HMM package to find the probability of our observation given our HMM 



## Problem 2 - Hidden States (3 points)

Remember we have two methods for assessing the hidden states associated with our sequence above. We can calculate the probability of being at any given hidden state at time T. We can also find the most likely sequence of hidden states given our observations. 

Conduct both of these analysis types and report the most likely hidden states. 


## Problem 3 - Tuning a parameter (4 points)

In our transmission matrix we assigned probabilities to transitions associatd with the Intergenic and Exon states. 

Let's imagine we want to tune one of these two parameters - the Intergenic parameters. 

Test 100 different probabilities (spanning from 0 to 1) using a loop like was shown in the lecture. Use the new transition probabilities to compute the probability of observing the sequence above. 

Plot the transition probabilities agains the probability of our observation

What Intergenic transition probabilities maximize the probability of our observed sequence? 



## Final Step (1 point)

Knit and upload your document to canvas







