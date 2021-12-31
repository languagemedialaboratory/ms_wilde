# MIss RoBERTa WiLDe
Metaphor Identification using Masked Language Model with Wiktionary Lexical Definitions

The main part of the code available in this repository was created by the authors of MelBERT[1] and originally comes from https://github.com/jin530/MelBERT/blob/main . 

The introduced modifications allow for using the definitions of the target words instead of the target words themselves. They also change the way of producing the sentence vector representation which now comes from the mean value of the component token vectors instead of [CLS] special token.  

The results published in the paper were achieved using Tesla P100-PCIE-16GB GPU.





[1] Choi, M., Lee, S., Choi, E., Park, H., Lee, J., Lee, D., & Lee, J. (2021). MelBERT: metaphor detection via contextualized late interaction using metaphorical identification theories. arXiv preprint arXiv:2104.13615.


