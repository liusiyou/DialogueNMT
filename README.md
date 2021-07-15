# DialogueNMT

Data Link: https://www.dropbox.com/sh/v7vztd736ffa2x0/AABZ9T00gaTB01AwUoEr058ea?dl=0

Translating conversational text, in particular task-oriented dialogues, is an important application task for machine translation
technology. However, it has so far not been extensively explored due to its inherent characteristics including data limitation,
discourse, informality and personality. In this paper, we systematically investigate advanced models on the taskoriented dialogue translation task, including sentence-level, document-level and non-autoregressive NMT models. Besides, we explore existing techniques such as data selection, back/forward translation, larger batch learning, finetuning and domain adaptation. To alleviate low-resource problem, we transfer general knowledge from four different pre-training models to the downstream task. Encouragingly, we find that
the best model with mBART pre-training pushes the SOTA performance on WMT20 English-German and IWSLT DIALOG Chinese-English datasets up to 62.67 and 23.21 BLEU points, respectively.1

# Citation

Please cite as:

```bibtex
@inproceedings{liu2021empirical,
  title={An Empirical Study on Task-Oriented Dialogue Translation},
  author={Liu, Siyou},
  booktitle={ICASSP 2021-2021 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
  pages={7558--7562},
  year={2021},
  organization={IEEE}
}
```