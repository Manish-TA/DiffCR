<p align="center">
<h1 align="center">DiffCR: A Fast Conditional Diffusion Framework for Cloud Removal from Optical Satellite Images</h1>
<p align="center">This repository is the official PyTorch implementation of the paper DiffCR.
</p>
</p>
<p align="center">
    <a href="https://blog.csdn.net/qq_42951560">Xuechao Zou<sup>1*</sup></a>,
    <a href="https://cslikai.cn/">Kai Li<sup>2*</sup></a>, Student Member, IEEE,
    <a href="https://www.cs.tsinghua.edu.cn/info/1116/5088.htm">Junliang Xing<sup>2</sup></a>, Senior Member, IEEE,
    <br>
    <a href="https://jiangchulang.blog.csdn.net/">Yu Zhang<sup>1</sup></a>,
    <a href="https://cs.qhu.edu.cn/jxgz/jxysz/szgk/50127.htm">Shiying Wang<sup>1</sup></a>,
    <a href="https://teacher.bupt.edu.cn/jinlei1/zh_CN/index/260463/list/">Lei Jin<sup>3</sup></a>,
    <a href="https://www.cs.tsinghua.edu.cn/info/1117/3542.htm">Pin Tao<sup>1,2,†</sup></a>, Member, IEEE
</p>

<p align="center">
    <a href="https://www.qhu.edu.cn/">Qinghai University</a><sup>1</sup>
    ,
    <a href="https://www.tsinghua.edu.cn/">Tsinghua University</a><sup>2</sup>,
    <br><a href="http://www.bupt.edu.cn/">Beijing University of Posts and Telecommunications</a><sup>3</sup>
</p>
<!-- <p align="center">
    <a href="https://arxiv.org/abs/2303.16565">Paper Preprint </a>
    |
    <a href="https://xavierjiezou.github.io/PMAA">Project Page</a>
</p> -->

<p align="center">
<!-- Optional: include a graphic explaining your approach/main result, bibtex entry, link to demos, blog posts and tutorials -->

![DiffCR](image/README/diffcr.png)

<!-- ![transformer+lim](image/README/transformer+lim.png) -->
</p>

<!-- ## News

- [2023/07/30] Code release.
- [2023/07/16] PMAA got accepted by ECAI 2023.
- [2023/03/29] PMAA is on arXiv now. -->

## Requirements

To install dependencies:

```setup
pip install -r requirements.txt
```

<!-- >📋  Describe how to set up the environment, e.g. pip/conda/docker commands, download datasets, etc... -->

To download datasets:

- Sen2_MTC_Old: [multipleImage.tar.gz](https://doi.org/10.7910/DVN/BSETKZ)

- Sen2_MTC_New: [CTGAN.zip](https://drive.google.com/file/d/1-hDX9ezWZI2OtiaGbE8RrKJkN1X-ZO1P/view?usp=share_link)

## Training

To train the models in the paper, run these commands:

```train
python run.py -p train -c config/ours_sigmoid.json
```

<!-- >📋  Describe how to train the models, with example commands on how to train the models in your paper, including the full training procedure and appropriate hyperparameters. -->

## Test

To test the pre-trained models in the paper, run these commands:

```test
python run.py -p test -c config/ours_sigmoid.json
```

## Evaluation

To evaluate my models on two datasets, run:

```eval
python evaluation/eval.py -s [ground-truth image path] -d [predicted-sample image path]
```

<!-- >📋  Describe how to evaluate the trained models on benchmarks reported in the paper, give commands that produce the results (section below). -->

## Pre-trained Models

You can download pretrained models here:

- Our awesome model trained on Sen2_MTC_Old: [diffcr_old.pth](/pretrained/diffcr_old.pth)
- Our awesome model trained on Sen2_MTC_New: [diffcr_new.pth](/pretrained/diffcr_new.pth)

<!-- >📋  Give a link to where/how the pretrained models can be downloaded and how they were trained (if applicable).  Alternatively you can have an additional column in your results table with a link to the models. -->

## Results

### Quantitative Results

- Abalation Study

![abalation](image/README/abalation.png)

- Main Results

![exp](image/README/exp.png)

### Qualitative Results

- Visualization results on the Sen2_MTC_Old dataset.

![old_1](image/README/old/11WNR_50003000.png)

---

![old_2](image/README/old/14RPS_20001000.png)

---

![old_3](image/README/old/14SQB_20006000.png)

---

![old_4](image/README/old/15RTN_70002000.png)

---

![old_5](image/README/old/31TEM_30009000.png)

- Visualization results on the Sen2_MTC_New dataset.

![new_1](image/README/new/T12TUR_R027_55.png)

---

![new_2](image/README/new/T15UVU_R012_12.png)

---

![new_3](image/README/new/T15UVU_R012_13.png)

---

![new_4](image/README/new/T15UVU_R012_17.png)

---

![new_5](image/README/new/T41VMJ_R006_64.png)

