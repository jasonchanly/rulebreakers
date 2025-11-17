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

Detail columns (these refer to the specific entities/names etc. that are used in creating the premises and conclusion)

- ```firstName```: the first name mentioned in the premises and conclusion
- ```pronoun```: the pronoun associated with the first name
- ```verb```: the verb mentioned (e.g. "is in", "is good at")
- ```entityA```: the first entity mentioned (i.e. a country or category of objects e.g "birds")
- ```entityB```: the second entity mentioned (i.e. a city or specific object e.g. "a robin")

Additional columns (these columns are included for ease of use/evaluation)

- ```kc_gen_formatted_prompt```: a ready-to-use prompt that presents the premises to the model and asks it to generate a conclusion that follows from the premises
- ```target_correct_conclusion```: the correct response expected from the model given the prompt (rulebreakers: "Nothing follows"; non-rulebreakers: the conclusion that can be derived by applying a logical rule to the premises)
- ```target_incorrect_conclusion```: the incorrect response expected from the model (rulebreakers: the conclusion that can be derived by applying a logical rule to the premises; non-rulebreakers: "Nothing follows")

Paired correctness: a rulebreaker and non-rulebreaker scenario pair is considered to be correctly answered if the model generates the corresponding "target_correct_conclusion" in the rulebreaker ("_rb") as well as the non-rulebreaker ("_nonrb") scenario. A pair is considered "unparsed" if, in at least one of the two scenarios, the model generates a response that matches neither the "target_correct_conclusion" nor the "target_incorrect_conclusion". In all other cases, the pair is considered "incorrect". See paper for further details.


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
