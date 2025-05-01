---
library_name: transformers
license: apache-2.0
base_model: google/flan-t5-base
tags:
- generated_from_trainer
metrics:
- rouge
model-index:
- name: data-processing
  results: []
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# data-processing

This model is a fine-tuned version of [google/flan-t5-base](https://huggingface.co/google/flan-t5-base) on the None dataset.
It achieves the following results on the evaluation set:
- Loss: 0.4043
- Rouge1: 47.7838
- Rouge2: 24.6572
- Rougel: 40.6741
- Rougelsum: 44.3864
- Gen Len: 17.7945

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 5e-05
- train_batch_size: 16
- eval_batch_size: 16
- seed: 42
- optimizer: Use OptimizerNames.ADAMW_TORCH with betas=(0.9,0.999) and epsilon=1e-08 and optimizer_args=No additional optimizer arguments
- lr_scheduler_type: linear
- num_epochs: 10

### Training results

| Training Loss | Epoch | Step | Validation Loss | Rouge1  | Rouge2  | Rougel  | Rougelsum | Gen Len |
|:-------------:|:-----:|:----:|:---------------:|:-------:|:-------:|:-------:|:---------:|:-------:|
| 1.8935        | 1.0   | 778  | 0.4131          | 47.4859 | 24.4416 | 40.308  | 44.1216   | 17.6058 |
| 0.459         | 2.0   | 1556 | 0.4081          | 47.7341 | 24.6997 | 40.537  | 44.2984   | 17.8064 |
| 0.4387        | 3.0   | 2334 | 0.4049          | 47.7041 | 24.6537 | 40.6339 | 44.2808   | 17.6251 |
| 0.4198        | 4.0   | 3112 | 0.4043          | 47.7838 | 24.6572 | 40.6741 | 44.3864   | 17.7945 |
| 0.4097        | 5.0   | 3890 | 0.4054          | 47.9612 | 24.8432 | 40.7765 | 44.4737   | 17.8023 |
| 0.3953        | 6.0   | 4668 | 0.4049          | 47.7135 | 24.7773 | 40.663  | 44.2913   | 17.9447 |
| 0.3875        | 7.0   | 5446 | 0.4058          | 48.0405 | 24.8429 | 40.8252 | 44.506    | 17.7627 |
| 0.377         | 8.0   | 6224 | 0.4058          | 48.1113 | 24.875  | 40.8236 | 44.5432   | 17.9556 |
| 0.3734        | 9.0   | 7002 | 0.4065          | 47.9645 | 24.8396 | 40.7411 | 44.4284   | 17.8531 |
| 0.3739        | 10.0  | 7780 | 0.4068          | 47.945  | 24.8247 | 40.7296 | 44.3957   | 17.8415 |


### Framework versions

- Transformers 4.51.3
- Pytorch 2.7.0+cu126
- Datasets 3.5.1
- Tokenizers 0.21.1
