# In Development

# Prompt-Tuned Conspiracy Theory Classification on Twitter using Large Language Models
This repository provides the data and code needed to replicate "Semantic proximity underlies progression in the endorsement of multiple conspiracy theories by individuals." Paul Vicinanza, Echo Zhou, Hayagreeva Rao, and Henrich Greve. 2024. 

The core methodological task of the paper is to classify tweets as endorsing, or not endorsing, a given conspiracy theory. We identify 16 conspiracies in the data through a combination of unsupervised topic modelling and manual annotation. Using a keyword match for the top-n terms of a conpsiracy theory, we construct a set of possible conspiracy endorsements for each conspiracy. We prompt-tune a frozen BLOOMZ-1.7B parameter model separately for each conspiracy theory using a hand-labelled dataset of 500 tweets.

### Results

**Prompt Tuning Benchmark**
| | BLOOMZ-1.7B Prompt Tuned | GPT3 175B Davinci-003 | 
| :------------- | :-------------: | :-------------: | 
| Accuracy | 0.85 | 0.63 |
| F1 | 0.904 | 0.697 |
| Precision | 0.887 | 0.52 |
| Recall | 0.903 | 0.929 |

### Replication code

Code needed to replicate the results of the study is provided as a jupyter notebook designed to run in Google Colab: peft_prompt_tuning_conspiracies.ipynb

### 
