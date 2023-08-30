# Two Word Test
## Combinatorial Semantics Benchmark for Large Language Models (LLMs)
### Nicholas Riccardi and Rutvik Desai - University of South Carolina Department of Psychology

LLMs sometimes struggle with word-order effects and compositional (or combinatorial) language processes, especially when surrounding context is absent. Here, we provide the Two Word Test, a series of functions that compares LLM meaningfulness judgments of simple two word phrases to meaningfulness judgments made by humans (Graves et al., 2013; https://doi.org/10.3758/s13428-012-0256-3).

We provide a variety of statistical methods to quantify LLM performance and compare it to human performance. We test OpenAI's GPT-4 and GPT-3.5-turbo, and Google's Bard. Briefly, we find that GPT-3.5 and Bard fail dramatically at judging the meaningfulness of simple two word phrases without context. GPT-4 performs substantially better, but still fails in certain circumstances, especially when asked to make continuous instead of binary judgments.

## Using the Two Word Test

To gather LLM meaningfulness ratings, we used the prompts detailed in our manuscript (closely mirroring the prompt used by Graves et al., 2013 to gather human ratings, but providing more examples for the LLMs). We collected binary and continuous ratings for all models. two-word-test.ipynb can be run as-is, taking LLM_ratings.csv and graves_2013.csv as input. LLM_ratings.csv can be updated by adding the ratings from other LLMs, which must then be specified in the models list within two-word-test.ipynb. A description of each function's purpose and brief explanations of the statistical tests can be found within.

Comments and questions can be posted in the discussion, or emailed to riccardn@email.sc.edu

## Scripts

### graves-gpt-api.ipynb

Sample query to GPT. Prompts and word lists can be edited to suit an experimenter's needs.

### LLM_ratings.csv

Once ratings are collected from an LLM, they should be formatted identically to this document. This .csv is fed into two-word-test.ipynb

### graves_2013.csv

Human ratings collected by Graves. Also includes similarity metrics for each phrase from some popular word embedding models. This .csv is also fed into two-word-test.ipynb

### two-word-test.ipynb

The statistical tests used to compare LLM responses to humans. If changes are made to LLM_ratings.csv or graves_2013.csv, this script will have to be edited accordingly.
