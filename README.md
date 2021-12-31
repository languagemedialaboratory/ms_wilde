# MIss RoBERTa WiLDe
Metaphor Identification using Masked Language Model with Wiktionary Lexical Definitions

The main part of the code available in this repository was created by the authors of MelBERT[1] and originally comes from https://github.com/jin530/MelBERT . 

The introduced modifications allow for using definitions of the target words instead of the target words themselves. They also change the way the sentence vector representation is produced - it now comes from the mean value of the component token vectors instead of [CLS] special token.  

We perform 5 trials for every experiment; each score published in the paper is the average of the scores yielded in these 5 trials. We always use the same set of random seeds: 1, 2, 3, 4 and 5. The results published in the paper were achieved using Tesla P100-PCIE-16GB GPU.

In order to reproduce the results published in the paper one has to use the same GPU as well as the same set of random seeds. 

The datasets used in the experiments originally come from https://github.com/jin530/MelBERT/blob/main . Each dataset available in the _data_ directory is enriched with the target words definitions coming from Wiktionary. 

To perform the experiment, one should run the main.py file from one of the three subdirectories available in this repository (base, cosine-similarity, s-bert).







[1] Choi, M., Lee, S., Choi, E., Park, H., Lee, J., Lee, D., & Lee, J. (2021). MelBERT: metaphor detection via contextualized late interaction using metaphorical identification theories. arXiv preprint arXiv:2104.13615.


