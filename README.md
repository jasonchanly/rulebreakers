# rulebreakers

Project page for "RULEBREAKERS: Challenging LLMs at the Crossroads between Formal Logic and Human-like Reasoning" (ICML 2025) by Jason Chan, Robert Gaizauskas and Zhixue Zhao, available at https://icml.cc/virtual/2025/poster/43712.

## Dataset

The full RULEBREAKERS dataset is found in ```./data/RULEBREAKERS_finegrained_format.csv```. Please refer to our paper for more details.

- ```id```: unique 7-digit ID assigned to the instance (each rulebreaker and non-rulebreaker pair share the same ID prefix, followed by _rb and _nonrb respectively e.g. "RULEBREAKERS_0000246_nonrb")
- ```rulebreaker_type```: the type of rulebreaker (or non-rulebreaker), classified by the logical rule applicable to the surface form of the premises ("mt" for modus tollens or "ds" for disjunctive syllogism)
- ```category```: the type of entities mentioned in the premises and conclusion (e.g. "cities", "fish", "brass instrument")
- ```premise1```: the first premise (either a conditional or disjunctive statement)
- ```premise2```: the second premise
- ```conclusion```: the conclusion that should be assessed in relation to the two premises
- ```label```: Boolean (true or false) - whether or not the conclusion follows from the premises (NB this is always true for non-rulebreakers and false for rulebreakers in the dataset)

Additional columns (these refer to the specific entities/names etc. that are used in creating the premises and conclusion)

- ```firstName```: the first name mentioned in the premises and conclusion
- ```pronoun```: the pronoun associated with the first name
- ```verb```: the verb mentioned (e.g. "is in", "is good at")
- ```entityA```: the first entity mentioned (i.e. a country or category of objects e.g "birds")
- ```entityB```: the second entity mentioned (i.e. a city or specific object e.g. "a robin")


## Contact

- Please contact Jason Chan (me) (JLYChan1@sheffield.ac.uk) or Zhixue Zhao (zhixue.zhao@sheffield.ac.uk) for any questions relating to the dataset or the project.

## Citation
```
@inproceedings{
chan2025rulebreakers,
title={{RULEBREAKERS}: Challenging {LLM}s at the Crossroads between Formal Logic and Human-like Reasoning},
author={Jason Chan and Robert J. Gaizauskas and Zhixue Zhao},
booktitle={Forty-second International Conference on Machine Learning},
year={2025},
url={https://openreview.net/forum?id=uqpML2nbIz}
}
```
