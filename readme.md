<h1 align="center"> Rethinking UMM Visual Generation: Masked Modeling for Efficient Image-Only Pre-training </h1>

<p align="center">
  Peng&nbsp;Sun<sup>1,3,*</sup> &ensp; <b>&middot;</b> &ensp;
  Jun&nbsp;Xie<sup>1,2,3,*</sup> &ensp; <b>&middot;</b> &ensp;
  <a href="https://tlin-taolin.github.io/" target="_blank">Tao&nbsp;Lin</a><sup>3</sup> &ensp; &ensp;
</p>

<p align="center">
  <sup>1</sup>Zhejiang University &emsp; <sup>2</sup>Shanghai Innovation Institute&emsp; <sup>3</sup>Westlake University&emsp; <br>
</p>

<p align="center">
<a href="https://arxiv.org/abs/2603.16139">:page_facing_up: Paper</a> &ensp;
<a href="#label-bibliography">:label: BibTeX</a> &ensp;
  <br><br>
</p>

Official PyTorch implementation of IOMM: :trophy: A data-efficient training (both pre-training and fine-tuning) paradigm for Unified Multimodal Models.

<div align="center">
  <img src="assets/figures/final_title_figure.jpg" width="1000" />
  <p style="margin-top: 8px; font-size: 14px; color: #666; font-weight: bold;">
    Generation results of our IOMM-XL
  </p>
</div>

## :construction: TODOs

[✅] Release the [paper](https://arxiv.org/abs/2603.16139).

[ ] Release **IOMM-B**.

[ ] Release inference code.

[ ] Update the paper.

[ ] Release training code.

## :sparkles: Features

:rocket: **Image-only Pre-training**:

- :white_check_mark: **No need for high-quality text-image pair datasets**
- :white_check_mark: **Achieve GenEval=0.89 at 10 epoch under 11 million data**
- :white_check_mark: **Gain editing ability under zero-shot settings**


:zap: **Mixed Data Fine-tuning**:

- :white_check_mark: **GenEval = 0.89 and WISE = 0.63** for Qwen-Image-20B

- :bar_chart: **Extended results** for additional tuned models are available [here](#rocket-generalization-to-open-source-umms)

:book: Check more detailed features in our [paper](https://arxiv.org/abs/2603.16139)!



## :rocket: Generalization to open-source UMMs

Our mixed data fine-tuning paradigm also achieves notable performance enhancement in those open-source Unified Multimodal Models (UMMs), even for the powerful baseline Qwen-Image-20B.

| METHOD                                           | Res.        | NFE           | GenEval        | WISE        |
|--------------------------------------------------|-------------|---------------|----------------|-------------|
| OpenUni-L                                        | 512         | 20 $\times$ 2 | 0.85           | 0.52        |
| $\quad \boldsymbol{\oplus}$ Pair finetuning      | 512         | 20 $\times$ 2 | 0.88           | 0.62        |
| $\quad \boldsymbol{\oplus}$ Mix finetuning       | 512         | 20 $\times$ 2 | 0.88           | 0.59        |
| Qwen-Image-20B                                   | 512         | 50 $\times$ 2 | 0.85           | -           |
| $\quad \boldsymbol{\oplus}$ Pair finetuning      | 512         | 50 $\times$ 2 | 0.88           | 0.63        |
| $\quad \boldsymbol{\oplus}$ Mix finetuning       | 512         | 50 $\times$ 2 | 0.89           | 0.63        |
| Qwen-Image-20B                                   | 1024        | 50 $\times$ 2 | 0.87           | 0.62        |
| $\quad \boldsymbol{\oplus}$ Pair finetuning      | 1024        | 50 $\times$ 2 | 0.88           | 0.63        |
| $\quad \boldsymbol{\oplus}$ Mix finetuning       | 1024        | 50 $\times$ 2 | 0.89           | 0.63        |


## :label: Bibliography

If you find this repository helpful for your project, please consider citing our work:

```
@article{sun2026rethinking,
  title={Rethinking UMM Visual Generation: Masked Modeling for Efficient Image-Only Pre-training},
  author={Sun, Peng and Xie, Jun and Lin, Tao},
  journal={arXiv preprint arXiv:2603.16139},
  year={2026},
  url={https://arxiv.org/abs/2603.16139}
}
```

## :page_facing_up: License

Apache License 2.0 - See [LICENSE](LICENSE) for details.
