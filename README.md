

Official PyTorch implementation of the paper *"Self-Supervised Relational Reasoning for Representation Learning"* [[arxiv]](https://arxiv.org/abs/2006.05849)

*Abstract*: In self-supervised learning, a system is tasked with achieving a surrogate objective by defining alternative targets on a set of unlabeled data. The aim is to build useful representations that can be used in downstream tasks, without costly manual annotation. In this work, we propose a novel self-supervised formulation of relational reasoning that allows a learner to bootstrap a signal from information implicit in unlabeled data. Training a relation head to discriminate how entities relate to themselves (intra-reasoning) and other entities (inter-reasoning), results in rich and descriptive representations in the underlying neural network backbone, which can be used in downstream tasks such as classification and image retrieval. We evaluate the proposed method following a rigorous experimental procedure, using standard datasets, protocols, and backbones. Self-supervised relational reasoning outperforms the best competitor in all conditions by an average 14% in accuracy, and the most recent state-of-the-art model by 3%. We link the effectiveness of the method to the maximization of a Bernoulli log-likelihood, which can be considered as a proxy for maximizing the mutual information, resulting in a more efficient objective with respect to the commonly used contrastive losses. 


<p align="center">
  <img width="600" alt="self-supervised relational reasoning" src="./etc/model_with_caption.png">
</p>


Citation
---------

```
@article{patacchiola2020self,
  title={Self-Supervised Relational Reasoning for Representation Learning},
  author={Patacchiola, Massimiliano and Storkey, Amos},
  journal={arXiv preprint arXiv:2006.05849},
  year={2020}
}
```

Essential code
--------------


Here, you can find the essential code of the method with full training pipeline: 

- [stand-alone python script](./essential_script.py) the stand-alone training script, it only requires PyTorch and Torchvision.
- [jupyter notebook](./essential_notebook.ipynb) step-by-step explanation of the code with both train and linear-evaluation phases.

The essential code above, trains a self-supervised relation module on CIFAR-10 with a Conv4 backbone.
The backbone is stored at the end of the training and can be used for other downstream tasks (e.g. classification, image retrieval). The GPU is not required for those examples. This has been tested on `Ubuntu 18.04 LTS` with `Python 3.6` and `Pytorch 1.4`.

Running instruction (Added by Sudipan)
--------------------------------

There was no env file in the original repo. So I added one. After creating the env file by command:

conda env create -f environment. yml

It needs to be activated:

source activate selfSupRelationalLearning 

(or, conda activate selfSupRelationalLearning)

Then, run 

python python essential_script.py


Code to reproduce the experiments
--------------------------------

Coming soon...


License
-------

MIT License

Copyright (c) 2020 Massimiliano Patacchiola

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
