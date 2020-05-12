# Algorithmic Efficiency SOTA Submissions
We found that in 2019 it took [44x less compute](https://openai.com/blog/ai-and-efficiency/) to train a neural net to AlexNet-level performance than in 2012.
(Moore’s Law would have only yielded an 11x change in cost over this period).

Going forward, we're going to use this git repository to help publicly track state of the art (SOTA) algorithmic efficiency.
We're beginning by tracking training efficiency SOTA's in image recognition and translation at two levels.

#### AlexNet-level performance
*79.1% top 5 accuracy on ImageNet*

| Publication| Compute(tfs-s/days)| Reduction Factor| Analysis| Date |
| ----------------------- | ------------- | ------------ | ----------------------- | ------------ |
| [AlexNet](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)|3.1|1|AI and Efficiency| 6/1/2012|
| [GoogLeNet](https://arxiv.org/abs/1409.4842)|0.71|4.3|[AI and Efficiency](https://openai.com/blog/ai-and-efficiency/)| 9/17/2014|
| [MobileNet](https://arxiv.org/abs/1704.04861)|0.28|11|[AI and Efficiency](https://openai.com/blog/ai-and-efficiency/)| 4/17/2017|
| [ShuffeNet](https://arxiv.org/abs/1707.01083)|0.15|21|[AI and Efficiency](https://openai.com/blog/ai-and-efficiency/)| 7/3/2017|
| [ShuffleNet_v2](https://arxiv.org/abs/1807.11164)|0.12|25|[AI and Efficiency](https://openai.com/blog/ai-and-efficiency/)| 6/30/2018|
| [EfficientNet](https://arxiv.org/abs/1905.11946)|0.069|44|[EfficientNet](https://arxiv.org/abs/1905.11946)| 5/28/2019|

#### ResNet-50-level performance
*92.9% top 5 accuracy on ImageNet*

| Publication| Compute(tfs-s/days)| Reduction Factor| Analysis| Date |
| ----------------------- | ------------- | ------------ | ----------------------- | ------------ |
|[ResNet-50](https://arxiv.org/abs/1512.03385)|17|1|[AI and Efficiency](https://openai.com/blog/ai-and-efficiency/)| 1/10/2015|
|[EfficientNet](https://arxiv.org/abs/1905.11946)|0.75|10|[EfficientNet](https://arxiv.org/abs/1905.11946)| 5/28/2019|

#### Seq2Seq-level Performance
*34.8 BLEU on WMT-14 EN-FR*

| Publication| Compute(tfs-s/days)| Reduction Factor| Analysis| Date |
| ----------------------- | ------------- | ------------ | ----------------------- | ------------ |
[Seq2Seq (Ensemble)](https://arxiv.org/abs/1409.3215)|465|1|[AI and Compute](https://openai.com/blog/ai-and-compute/)| 1/10/2014
[Transformer(Base)](https://arxiv.org/abs/1706.03762)|8|61|[Attention is all you need](https://arxiv.org/abs/1807.11164)| 1/12/2017

#### GNMT-level performance
*39.92 BLEU on WMT-14 EN-FR*

| Publication| Compute(tfs-s/days)| Reduction Factor| Analysis| Date |
| ----------------------- | ------------- | ------------ | ----------------------- | ------------ |
[GNMT](https://arxiv.org/abs/1609.08144)|1620|1|[Attention is all you need](https://arxiv.org/abs/1807.11164)| 1/26/2016
[Transformer (Big)](https://arxiv.org/abs/1706.03762)|181|9|[Attention is all you need](https://arxiv.org/abs/1807.11164)| 1/12/2017

##In order to make an entry please submit a pull request in which you:
1. Make the appropriate update to efficiency_sota.csv
2. Make the appropriate update to the tables in this file, README.MD
3. Add the relevant calculations/supporting information to the analysis folder. To get examples of calculations please see
[AI and Compute](https://openai.com/blog/ai-and-compute/#appendixmethods) and Appendix A and B in [Measuring the Algorithmic Efficiency of Neural Networks](https://arxiv.org/abs/2005.04305).

FAQ
1. We're interested in tracking progress on additional benchmarks that have been of interest for many years and continue
to be of interest. Please send thoughts or analysis on such benchmarks to *danny@openai.com.*
2. ImageNet is the only training data source allowed for the vision benchmark. No human captioning, other images, or other data is allowed. Automated augmentation is ok.
3. We currently place no restrictions on training data used for translation, but may split results by appropriate categories in the future.
4. A tf-s/day equals a teraflop/s worth of compute run a day.

To cite this work please use the following bibtex entry.

@misc{hernandez2020efficiency
    title = {Measuring the Algorithmic Efficiency of Neural Networks},
    author = {Danny Hernandez, Tom B. Brown},
    year = {2020},
    eprint={2005.04305},
    archivePrefix={arXiv},
    primaryClass={cs.LG},
}
