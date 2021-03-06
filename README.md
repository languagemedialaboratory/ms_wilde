# MIss RoBERTa WiLDe
**Metaphor Identification using Masked Language Model with Wiktionary Lexical Definitions**
ㅤㅤ

ㅤ
ㅤ


This repository comprises the code and the datasets used in the experiments performed for the article "MIss RoBERTa WiLDe: Metaphor Identification using Masked Language Model with Wiktionary Lexical Definitions".

The main part of the code available in the repository was created by the authors of MelBERT[1] and originally comes from https://github.com/jin530/MelBERT . 

The introduced modifications allow for using definitions of the target words instead of the target words themselves. They also change the way the sentence vector representation is produced - it now comes from the mean value of the component token vectors instead of [CLS] special token.  

The datasets used in the experiments originally come from https://drive.google.com/file/d/1738aqFObjfcOg2O7knrELmUHulNhoqRz/view?usp=sharing and are enriched with the Wiktionary definitions for the target words. All of the datasets used in the experiments are available in the data directory. 

Before performing the experiment, one should set the path to the dataset (e.g. data_dir = ./../data/vua-18) as well as specify the random seed (e.g. seed = 4) in main_config.cfg file. The experiment can be initialized from the command line with the "python main.py" command.

The results for GENRES and POS datasets published in the paper were achieved using the models first trained on VUA-18. To reproduce these results one has to first run the training on VUA-18 and then use the saved model for testing on GENRES or POS. In order to do so, in the main_config.cfg file, the saved model needs to be specified (e.g. bert_model = ./saves/roberta-base/0_20211111-1720), do_train option has to be set to False (do_train = False) and the path to the dataset has to be changed accordingly (e.g. data_dir = ./../data/pos).

The results for MOH and TroFi datasets published in the paper were achieved using the models first trained on VUA-20. To reproduce these results one has to first run the training on VUA-20 and then use the saved model for testing on MOH or TroFi. In order to do so, in the main_config.cfg file, task_name parameter needs to be set as "trofi" (for both MOH and TroFi), the saved model needs to be specified (e.g. bert_model = ./saves/roberta-base/3_20211112-1720), do_train option has to be set to False (do_train = False) and the path to the dataset has to be changed accordingly (e.g. data_dir = ./../data/moh).

We perform 5 trials for every experiment; each score published in the paper is the average value of the scores yielded in these 5 trials. We always use the same set of random seeds: 1, 2, 3, 4 and 5. The results published in the paper were achieved using Tesla P100-PCIE-16GB GPU.

In order to reproduce the results published in the paper one has to use the same GPU as well as the same set of random seeds. 

ㅤㅤ

ㅤㅤ

ㅤㅤ


[1] Choi, M., Lee, S., Choi, E., Park, H., Lee, J., Lee, D., & Lee, J. (2021). MelBERT: metaphor detection via contextualized late interaction using metaphorical identification theories. arXiv preprint arXiv:2104.13615.


