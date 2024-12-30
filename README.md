# Problem_Set_09

This week we learned how to build and test Hidden Markov Models (HMM)
HMMs are very useful in biological, genomic, and proteomic investigations. 

## Problem A - Construct the Transmission and Emission matrices. 

![lab_model](https://user-images.githubusercontent.com/47755288/225417771-6d96f8af-61c4-4321-b07f-243674a64eab.png)

One use of HMMs is to model genomic content to identify genes within genomes. The above is a simplified version of this idea. 
The top part of the diagram is a Markov Chain that represents various parts of genes. Any transition (arrow) not shown is zero (0). 
These states are _hidden_ .

The bottom part of the diagram is the emissions from each hidden state. These are represented by codons. We can sample the codons along a genomic sequence. We have three different codon possibilites: Start Codon, Other Codon, Stop Codon. 

In this case the codon depends _only_ on the hidden state. Below each hidden state is the emission probability for each of our three possible observations 

**Build the transmission and emission matrices from this diagram**

## Question A1
Report your transmission matrix

## Question A2 
Report your emission matrix

&nbsp;
&nbsp;


## Problem B - Probability of our observation

Let's imagine we sample a DNA sequence that would have the RNA sequence below (aka you don't need to transcribe it) 

**ACU  AAA  AUG  AUG  GCG  UGA  UUU**

_Reminder: AUG is start. Stop is UAA, UAG, or UGA_

In this case, we are going to assume that **we start at an intergenic hidden state**
Use the appropriate command in the HMM package to find the probability of our observation given our HMM 

_Hint: you will need to figure out which state each of the codons belongs to_

## Question B1
Report the probability of the 7 states listed above when starting at an intergenic state

&nbsp;
&nbsp;

## Problem C - Hidden States

Remember we have two methods for assessing the hidden states associated with our sequence above. We can calculate the probability of being at any given hidden state at time T. We can also find the most likely sequence of hidden states given our observations. We are specifically getting at the difference between steady-state probabilities and assessing the probabilities based on our observations

## Question C1
What state has the maximum probability in the steady states?

## Question C2
What is the probability associated with the steady-state selected in Question C1?

## Question C3
What is the most likely series of hidden states associated with the above DNA/RNA sequence (the 7 observed states from Question B)
&nbsp;
&nbsp;

## Problem D - Tuning a parameter (4 points)

In our transmission matrix, we assigned probabilities to transitions associated with the Intergenic and Exon states. 

Let's imagine we want to tune one of these two parameters - the Intergenic parameters. 

Test 100 different probabilities (spanning from 0 to 1) using a loop like was shown in the lecture. Use the new transition probabilities to compute the probability of observing the sequence above. 

## Question D1
Plot the transition probabilities against the probability of our observation. The observation is the 7 states listed in question B.

## Question D1
Include the plot

## Question D2
What Intergenic transition probabilities maximize the probability of our observed sequence? 



## Final Step

Knit and upload your document to canvas







