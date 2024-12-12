# [NeurIPS 2024] Learning Frequency-Adapted Vision Foundation Model for Domain Generalized Semantic Segmentation

This is the official implementation of our work entitled as ```Learning Frequency-Adapted Vision Foundation Model for Domain Generalized Semantic Segmentation```, which has been accepted by ```NeurIPS 2024```.

## Environment Configuration

Please refer to the ```requirements.txt``` file in this project.

## Training on the Source Domain

An command example to train the model when using ```CityScapes``` as the source domain is:

```python tools/train.py configs/my/citys_rein_dinov2_mask2former_512x512_bs1x4.py --work-dir exps/exp0322```

Please remember to change the file folder to your own.

## Inference on the Unseen Target Domains

An command example to infer the model when using ```CityScapes``` as the source domain is:

```python tools/test.py configs/my/citys_rein_dinov2_mask2former_512x512_bs1x4.py exps/exp0429/iter_40000.pth --backbone checkpoints/dinov2_converted.pth```

Please remember to change the file folder to your own, and also to specify the file folder of the target domain in the script.

## Citation

If you find this work is useful for your task please cite our work as follows:

```BibTeX
@inproceedings{bi2024fada,
  title={Learning Frequency-Adapted Vision Foundation Model for Domain Generalized Semantic Segmentation},
  author={Bi, Qi and Yi, Jingjun and Zheng, Hao and Zhan, Haolan and Huang, Yawen and Ji, Wei and Li, Yuexiang and Zheng, Yefeng},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  volume={37},
  year={2024}
}
```

## Acknowledgement

Our implementation is primarily based on the following repositories, with significant influence from Rein. Thanks for their authors.
* [MMSegmentation](https://github.com/open-mmlab/mmsegmentation)
* [Rein](https://github.com/w1oves/Rein)

