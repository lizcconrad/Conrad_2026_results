# Conrad 2026 Results

This repository stores the results of running the POGG data-to-text algorithm at various points of the development pipeline. 

## `refactor_trace`

I refactored the structure of the lexicon/output significantly after finishing developing semantic functions for the `perplexity` dataset.

This directory holds runs on the `perplexity` dataset through different checkpoints of this refactoring.

While full detailed diffs of the results of these runs are not available, there is a top-level `dataset_report.txt` for each run. Each run throughout the refactor has identical results in the "EVALUATION METRICS" table at the top.[^1] 

[^1]: The one exception to this is `post_perplexity__original` which had a few missed nodes/edges due to a bug in the lexicon. After fixing this bug I re-ran the algorithm on the dataset without refactoring any of the code so the first "official" run for the refactoring is `post_perplexity__pre_lex_refactor`

| Run name                          | Description                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------| 
| post_perplexity__original         | original run on perplexity dataset after finishing semantic development for this dataset |
| post_perplexity__pre_lex_refactor | fixed some incorrect entries in the lexicon and reran on perplexity dataset              |
| post_perplexity__lex_refactor     | run after lexicon refactoring                                                            | 
| post_perplexity__eval_refactor    | run after evaluation refactoring                                                         | 
| post_perplexity__divide_repos     | run after moving Semantic Composition to a separate repository                           | 