## PPTOD: Multi-Task Pre-Training for Plug-and-Play Task-Oriented Dialogue System
**Authors**: Yixuan Su, Lei Shu, Elman Mansimov, Arshit Gupta, Deng Cai, Yi-An Lai, and Yi Zhang

Code our PPTOD paper: [PPTOD: Multi-Task Pre-Training for Plug-and-Play Task-Oriented Dialogue System]()

### Introduction:
Pre-trained language models have been recently shown to benefit task-oriented dialogue (TOD) systems. Despite their success, existing methods often formulate this task as a cascaded generation problem which can lead to error accumulation across different sub-tasks and greater data annotation overhead. In this study, we present PPTOD, a unified model that seamlessly supports both task-oriented dialogue understanding and response generation in a plug-and-play fashion. In addition, we introduce a new dialogue multi-task pre-training strategy that allows the model to learn the primary TOD task completion skills from heterogeneous dialog corpora. We extensively test our model on three benchmark TOD tasks, including end-to-end dialogue modelling, dialogue state tracking, and intent classification. Results show that PPTOD creates new state-of-the-art on all evaluated tasks in both full training and low-resource scenarios. Furthermore, comparisons against previous SOTA methods show that the responses generated by PPTOD are more factually correct and semantically coherent as judged by human annotators.

![Alt text](https://github.com/awslabs/pptod/blob/main/overview.png)

### 1. Citation
If you find our paper and resources useful, please kindly cite our paper:

    @article{su2021pptod,
      author = {Yixuan Su and
                Lei Shu and
                Elman Mansimov and
                Arshit Gupta and
                Deng Cai and
                Yi-An Lai and
                Yi Zhang},
      title  = {PPTOD: Multi-Task Pre-Training for Plug-and-Play Task-Oriented Dialogue System},
      journal = {CoRR},
      year = {2021},
      eprinttype = {arXiv}
    }
    
### 2. Environment Setup:
```yaml
pip3 install -r requirements.txt
pip3 install gdown
python -m spacy download en_core_web_sm
```

### 3. PPTOD Checkpoints:
You can download checkpoints of PPTOD with different configurations here.

| PPTOD-small       | PPTOD-base          | PPTOD-large  |
| :-------------: |:-------------:| :-----:|
| [here](https://pptod.s3.amazonaws.com/Pretrain/small.zip)      | [here](https://pptod.s3.amazonaws.com/Pretrain/base.zip) | [here](https://drive.google.com/file/d/1rz7LMxxZA7OO96Iy0U3oVzqLbdZERoB5/view?usp=sharing) |

To use PPTOD, you should download the checkpoint you want and unzip it in the ./checkpoints directory.

Alternatively, you can run the following commands to download the PPTOD checkpoints.

#### (1) Downloading Pre-trained PPTOD-small Checkpoint:
```yaml
cd checkpoints
chmod +x ./download_pptod_small.sh
./download_pptod_small.sh
```

#### (2) Downloading Pre-trained PPTOD-base Checkpoint:
```yaml
cd checkpoints
chmod +x ./download_pptod_base.sh
./download_pptod_base.sh
```

#### (3) Downloading Pre-trained PPTOD-large Checkpoint:
```yaml
cd checkpoints
chmod +x ./download_pptod_large.sh
./download_pptod_large.sh
```

### 4. Data Preparation:
The detailed instruction for preparing the pre-training corpora and the data of downstream TOD tasks are provided in the ./data folder.

### 5. Dialogue Multi-Task Pre-training:
To pre-train a PPTOD model from scratch, please refer to details provided in ./Pretraining directory.

### 6. Downstream TOD Tasks:
#### (1) End-to-End Dialogue Modelling:
To perform End-to-End Dialogue Modelling using PPTOD, please refer to details provided in ./E2E_TOD directory. 

#### (2) Dialogue State Tracking:
To perform Dialogue State Tracking using PPTOD, please refer to details provided in ./DST directory. 

#### (3) Intent Classification:
To perform Intent Classification using PPTOD, please refer to details provided in ./IC directory. 


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This project is licensed under the Apache-2.0 License.

