The CheXpert 8x200 image-image and text-image retrieval evaluation sets
===============

## Preparation

The images used in this evaluation are drawn from the [CheXpert dataset](https://stanfordmlgroup.github.io/competitions/chexpert/). Please make sure to download the CheXpert dataset with all images before proceeding.

## Data Files

1. `image-retrieval`: This directory hosts files for the image-image retrieval evaluation.

- `candidate.csv`: This file contains the paths of 8x200 candidate images, along with original labels in the CheXpert dataset. The paths are relative to the original CheXpert download directory.

- `query.csv`: This file contains expert-selected query images. For each one of the 8 disease categories, 10 query images are provided.


2. `text-retrieval`: This directory hosts files for the text-image retrieval evaluation.

- `candidate.csv`: This file contains the paths of the same 8x200 candidate images drawn from the CheXpert dataset.

- `query.csv`: This file contains expert-written text queries. For each one of the 8 disease categories, 10 textual queries are provided.


## Evaluation

A retrieved image from all the candidates is considered correct only if its label matches the label of the query image or text. For example, for a query image from the `Atelectasis` category, a retrieved image is only considered a positive retrieval if its label for `Atelectasis` is `1`. The retrieval metrics such as `Precision@10` are then calculated based on this criterion.

## Reference

For details on how the data is collected and used, please refer to [this paper](https://arxiv.org/abs/2010.00747).
