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


## Dataset 
PACS dataset

```
wget https://wjdcloud.blob.core.windows.net/dataset/PACS.zip
unzip PACS.zip
```
## How to run

We provide the commands for four tasks in PACS to reproduce the results.

```
python methods/main.py --dataset pacs --mode FedAtImg --test_envs 0 --iters 200 --wk_iters 1 --lr 5e-05
```
