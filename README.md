# rulebreakers

Project page for "RULEBREAKERS: Challenging LLMs at the Crossroads between Formal Logic and Human-like Reasoning" (ICML 2025, forthcoming) by Jason Chan, Robert Gaizauskas and Zhixue Zhao, preprint available at https://arxiv.org/abs/2410.16502.

## Dataset

The full RULEBREAKERS dataset is found in ```./data/rulebreakers_dataset.json```. Please refer to our paper for more details.

- ```id```: unique 7-digit ID assigned to the instance (each rulebreaker and non-rulebreaker pair share the same ID prefix, followed by _rb and _nonrb respectively e.g. "RULEBREAKERS_0000246_nonrb")
- ```rulebreaker_type```: the type of rulebreaker (or non-rulebreaker), classified by the logical rule applicable to the surface form of the premises ("mt" for modus tollens or "ds" for disjunctive syllogism)
- ```category```: the type of entities mentioned in the premises and conclusion (e.g. "cities", "fish", "brass instrument")
- ```premises```: the information provided as context 
- ```conclusion```: the conclusion that should be assessed in relation to the premises
- ```label```: Boolean (true or false) - whether or not the conclusion follows from the premises (NB this is always true for non-rulebreakers and false for rulebreakers in the dataset)


## Contact

- Please contact Jason Chan (me) (JLYChan1@sheffield.ac.uk) or Zhixue Zhao (zhixue.zhao@sheffield.ac.uk) for any questions relating to the dataset or the project.

