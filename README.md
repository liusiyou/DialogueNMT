# DialogueNMT

Translating conversational text, in particular task-oriented dialogues, is an important application task for machine translation technology. However, it has so far not been extensively explored due to its inherent characteristics including data limitation, discourse, informality and personality. 

We systematically investigate advanced models on the taskoriented dialogue translation task, including sentence-level, document-level and non-autoregressive NMT models. Besides, we explore existing techniques such as data selection, back/forward translation, larger batch learning, finetuning and domain adaptation. To alleviate low-resource problem, we transfer general knowledge from four different pre-training models to the downstream task. 


# Data

Please download the processed data from [Link](https://www.dropbox.com/sh/v7vztd736ffa2x0/AABZ9T00gaTB01AwUoEr058ea?dl=0).

1. 数据预处理

   * Step 1: remove non-printing characteristics (remove-non-printing-char.perl)
   * Step 2: normalize punctuations (normalize-punctuation.perl)
   * Step 3: tokenization (tokenizer.perl -a -l en)
   * Step 4: delete duplicate sentence pairs according to md5
   * Step 5: delete sentence pairs according to length and ratio (1~100/0.8~1.2)
   * Step 6: delete sentences according to language id (langdetect)
   * Step 7: joint bpe (32000)

2. 文件说明
   * chat_baseline: only chat domain data
		* train: training data
		* valid: validation data
		* test: testing data
		* databin: binary data for fariseq NMT
   * chat_adaptation_taskmaster+_mono_800k: chat domain and selected general domain data
		* train: training data
		* valid: validation data
		* test: testing data
		* databin: binary data for fariseq NMT

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