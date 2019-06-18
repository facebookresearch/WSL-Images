## WSL-Images

This project provides models pre-trained in weakly-supervised fashion on **940 million** public images with 1.5K hashtags matching with 1000 ImageNet1K synsets, followed by fine-tuning on ImageNet1K dataset.  Please refer to "Exploring the Limits of Weakly Supervised Pretraining" (https://arxiv.org/abs/1805.00932) presented at ECCV 2018 for the details of model training.

We are providing 4 models with different capacities.

| Model              | #Parameters | FLOPS | Top-1 Acc. | Top-5 Acc. |
| ------------------ | :---------: | :---: | :--------: | :--------: |
| ResNeXt-101 32x8d  | 88M         | 16B   |    82.2    |  96.4      |
| ResNeXt-101 32x16d | 193M        | 36B   |    84.2    |  97.2      |
| ResNeXt-101 32x32d | 466M        | 87B   |    85.1    |  97.5      |
| ResNeXt-101 32x48d | 829M        | 153B  |    85.4    |  97.6      |

Our models significantly improve the training accuracy on ImageNet compared to training from scratch. **We achieve state-of-the-art accuracy of 85.4% on ImageNet with our ResNext-101 32x48d model.**

## Loading models with torch.hub
The models are available with [torch.hub](https://pytorch.org/docs/stable/hub.html).
As an example, to load the ResNext-101 32x16d model, simply run:

```
model = torch.hub.load('facebookresearch/WSL-Images', 'resnext101_32x16d_wsl')
```
Please refer to [torch.hub](https://pytorch.org/docs/stable/hub.html) to see a full example of using the model to classify an image.

## Citing WSL-Images

If you use the WSL-Images models, please cite the following publication.
```
@inproceedings{wslimageseccv2018,
  title={Exploring the Limits of Weakly Supervised Pretraining},
  author={Dhruv Kumar Mahajan and Ross B. Girshick and Vignesh Ramanathan and Kaiming He and Manohar Paluri and Yixuan Li and Ashwin Bharambe and Laurens van der Maaten},
  booktitle={ECCV},
  year={2018}
}
```

## License
WSL-Images models are released under the CC-BY-NC 4.0 license. See [LICENSE](LICENSE) for additional details.
