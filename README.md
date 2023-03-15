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


## Problem 2 - Probability of our observation

Let's imagine we sample a DNA sequence which would have the RNA sequence below (aka you don't need to transcribe it) 

**ACU  AAA  AUG  AUG  GCG  UGA  UUU**

_Reminder: AUG is start. Stop is UAA, UAG, or UGA_

In this case we are going to assume that **we start at an intergenic hidden state**
Use the approrpiate command in the HMM package to find the probability of our observation given our HMM 



## Problem 2 - Hidden States

Remember we have two methods for assessing the hidden states associated with our sequence above. We can calculate the probability of being at any given hidden state at time T. We can also find the most likely sequence of hidden states given our observations. 

Conduct both of these analysis types and report the most likely hidden states. 


## Problem 3 - Tuning a parameter

In the model above you'll notice that there is a small probability of the hidden state "start" emitting the state "other" aka sometimes our genes do not start with a start codon! There are alternative start codons that organisms can utilize to start a gene sequence. 

You have a sequence from an unusual new species that you _think_ might be using alternative start codons at a higher rate than you based your model on 

Here is the sequence

**CUA  GCG  UCG  GAG  CAU  UAA  UCU  CCG  UCG  GUG  UGA  AUG**







