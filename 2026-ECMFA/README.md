# ECMFA 2026 – EMF-Kaizen Experimental Artifacts

This folder contains all experimental artifacts used in the ECMFA 2026
submission describing EMF-Kaizen.

## Evaluation
The evaluation answers three RQs:
- RQ1 How effective is EMF-Kaizen in providing (meta-)modelling assistance?
- RQ1.1 What is the effect of different LLMs?
- RQ2 What is the effect of the different parts of the prompt?

## Experiments
We designed two experiments, one two answer RQ1 and RQ1.1, and the other for RQ2.

### Experiment for RQ1 and RQ1.1
Design:
- We selected 5 meta-models in different domains that jointly cover structural and behavioural aspects, and work at the meta-model and model levels.
– We created 3 models per meta-model, each on a degree of completeness, from almost empty models to detailed ones. These represent different stages at which the assistant may be used.
– We defined 4 completion request categories (command-like, model-based, recommendation, domain descriptive), and designed 2 NL requests per model. This
amounts to 120 requests.
– We selected 4 LLMs for the experiment: gemini-2.5-flash-lite (from Google), gpt-4o-mini, gpt-4.1-mini and gpt-5-mini (from OpenAI). 

Folder [RQ1](./RQ1) contains:
- Meta-models used in the evaluation
- Models at different stages of completeness
- Natural-language assistance requests
- Raw and aggregated evaluation results

### Experiment for RQ2
Design:
- We selected 2 meta-models: the standard UML2 and another for specifying adapters for model migration transformations in adaptive languages. You can check the paper [here](https://www.miso.es/pubs/tosem_adaptive.pdf).
- We created 3 models per meta-model, each on a degree of completeness, from almost empty models to detailed ones. These represent different stages at which the assistant may.
- We defined 8 prompts per model.
- We conducted an ablation study, executing the experiment with: (i) the full prompt, (ii) the prompt without the NL explanation of the meta-model, (iii) the prompt without examples, and (iv) no pruning in the meta-model
- We used gpt-4o-mini.

Folder [RQ2](./RQ2) contains:
- Meta-models used in the evaluation
- Models at different stages of completeness
- Natural-language assistance requests
- Raw and aggregated evaluation results
