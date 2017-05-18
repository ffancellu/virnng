# Generative Constituency Parser with (linear-time) Discriminative Recognition Algorithm

The code implements a neural sequence-to-tree model in the context of constituency parsing, provides a unifination of discriminative and generative RNNG, and is capable of doing constituency parsing and language modeling. 

## Dependencies
* Dynet (2.0)
* Numpy

## Instructions
* Training (supervised\_enc, supervised\_dec, unsupervised)
* Testing (lm, parsing)
* For parsing, there arw two choices: 1) find the argmax tree from the approximated posterior q(a|x); 2) find the sampled tree from q(a|x) which maximizes the joint p(a,x) 
* For language modeling, there are three choices: 1) lower bound approximation; 2) importance sampling using variational distribution as proposal; and 3) directly sampling from prior
* Focused training depending on the final objective: if parsing is the goal, focus on maximizing q(a|x) and p(a|x); if language modeling is the goal, focus on maximizing p(x)

## Citation
```
@InProceedings{cheng2017virnng, 
  author = {Cheng, Jianpeng and Lopez, Adam and Lapata, Mirella}, 
  title = {A Generative Parser with a Discriminative Recognition Algorithm}, 
  booktitle = {Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Short Papers)}, 
  year = {2017}, 
  address = {Vancouver, Canada}, 
  publisher = {Association for Computational Linguistics} 
 }
```
## Contact
jianpeng.cheng@ed.ac.uk
