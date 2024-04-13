# TriplePlay

# Abstract
The surge in the evolution and complexity of pretrained
models, particularly exemplified by CLIP, presents both op-
portunities and challenges for Federated Learning (FL),
a cornerstone of privacy-preserving artificial intelligence.
This research delves into the intricacies of integrating large
foundation models like CLIP within FL frameworks to en-
hance privacy, efficiency, and adaptability across heteroge-
neous data landscapes. It specifically addresses the chal-
lenges posed by non-IID data distributions, the computa-
tional and communication overheads of leveraging such
complex models, and the skewed representation of classes
within datasets. Through a novel approach that incorpo-
rates CLIP as an adapter, this study aims to improve FL’s
adaptability and performance across diverse data distribu-
tions, tackle the long-tail distribution problem with GAN-
generated synthetic data, and mitigate resource demands
using quantization and low rank adaptation techniques. The
goal is to transcend the limitations of current FL practices
through a multi-faceted approach, offering solutions to en-
hance model performance while maintaining data privacy
and reducing computational demands. Our simulation re-
sults demonstrate that TriplePlay effectively decreases GPU
usage costs and speeds up the learning process, achieving
convergence with reduced communication overhead


## Prerequisites

Before you begin, make sure you have the following installed:
- Python 3.8 or higher


## Installation



## Training

```shell
python -m train.adversarial_training_clip --clip_model_name ViT-L-14 --pretrained openai --dataset imagenet --imagenet_root /path/to/imagenet --template std --output_normalize True --steps 20000 --warmup 1400 --batch_size 128 --loss ce --opt adamw --lr 1e-5 --wd 1e-4 --attack pgd --inner_loss ce --norm linf --eps 4 --iterations_adv 10 --stepsize_adv 1 --wandb False --output_dir /path/to/out/dir --experiment_name TECOA4 --log_freq 10 --eval_freq 10```
```
