# EVA7 - Session 14 - DETR - End to End Object Detection with Transformers

## Submission by :
Pranabesh Dash
Satya Nekkanti

Goals:
1. Fine-tune DETR on a custom dataset for object detection
2. Understand architectural concepts and how  to fine tune

## DETR

![DETR_Arch](https://github.com/pranabeshdash/EVA7/S14_finetune_DETR/DETR_Arch.png)

### DETR Architecture

DETR consists of 3 main components:
1. CNN Backbone for embedding image patches
2. Encoder-Decoder transformer
3. Feed forward network as head a prediction head

![DETR_backbone](https://github.com/pranabeshdash/EVA7/S14_finetune_DETR/DETR_transformer.png)

### Bipartite Matching Loss

![bipartite](https://github.com/pranabeshdash/EVA7/S14_finetune_DETR/bipartite_matching_loss.png)

DETR makes a fixed set of predictions which need to be narrowed down to the specific number of objects present in the image. This is done through bipartite matching i.e, one to one comparisons of the object predictions helping to eliminate low quality predictions and helping to achieve output reductions like NMS.

## Fine Tuning DETR on Custom Dataset

The notebook for the fine tuning exercise can be found [here](https://github.com/a-pujahari/EVA7/blob/main/Session14/EVA7_Session14_FineTuningDETR.ipynb).

### Metrics

Illustrated below are the loss and mean average precision value progression captured during training. 

![metrics](https://github.com/a-pujahari/EVA7/blob/main/Session14/train_metrics.png)

### Results 

![train_image](https://github.com/a-pujahari/EVA7/blob/main/Session14/val_image_result.png)

![validation_image](https://github.com/a-pujahari/EVA7/blob/main/Session14/train_image_result.png)


