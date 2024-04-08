This repository contains code and experiments for the paper:

# Toward Fairness Across Skin Tones in Dermatological Image Processing

## Abstract:
Skin cancer is a prevalent and concerning form of cancer, with an annual incidence rate estimated to be more than 3 million cases in the US. In recent years, the field of medical image processing has made remarkable progress in the domain of skin cancer detection, surpassing the diagnostic capabilities of dermatologists in certain settings. However, it has been reported that the performance of these deep-learning detection models varies significantly across different skin tones (e.g., light versus dark), motivating the need for fair and unbiased classification results. Here, we evaluate DeepDerm, a state-of-the-art skin cancer detection model, specifically focusing on its performance across skin types classified by the Fitzpatrick Skin Tones (FST). By analyzing the model’s accuracy and fairness, we observe no-table discrepancies in its performance across different FST categories. We propose a novel architecture that leverages finetuning, an ensemble architecture, and fairness-based resampling to support high accuracy and fairness in skin cancer detection. The proposed framework demonstrates promising outcomes, marking a significant stride toward achieving fairness and accuracy in dermatological image processing.


To cite:

> @inproceedings{almuzainit2023toward,
    title={Toward Fairness Across Skin Tones in Dermatological Image Processing},
    author={Almuzainit, Abdulaziz A and Dendukuri, Srujan K and Singh, Vivek K},
    booktitle={2023 IEEE 6th International Conference on Multimedia Information Processing and Retrieval (MIPR)},
    pages={1--7},
    year={2023},
    organization={IEEE}
  }

# Requirements

1. Get the SAFE model weights from this [link](https://drive.google.com/file/d/1t7Ujcj8-YTQ10LQL2e37m8eeB8TRJYRA/view?usp=share_link).
2. Get the datasets:
   - DDI dataset [link] (https://ddi-dataset.github.io/).
   - Fitzpatrick17k [link] (https://github.com/mattgroh/fitzpatrick17k).
4. If using GoogleColab -> add datasets to the "dataset" folder and model weights to the "new_models" folder.
   - arrange the dataset folder to separate folders for darker skin images (i.e., 56) and lighter skin images (i.e., 12) and split them in train/val sub-folders:
     - dataset
        - 12
          - train
          - val
        - 56
          - train
          - val
6. Run SAFE-Evaluation.ipynb.
    - SAFE-Framework.ipynb -> contains the experiment code for the framework proposed in the paper. 
    - SAFE-FineTuning.ipynb -> is the base code for fine-tuning the DeepDerm model.
