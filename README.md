# Generating Less Certain Adversarial Examples Improves Robust Generalization

Code for our paper _Generating Less Certain Adversarial Examples Improves Robust Generalization_ by [Minxing Zhang](https://scholar.google.com/citations?user=wsSLja0AAAAJ&hl=en&oi=ao), [Michael Backes](https://scholar.google.com/citations?user=ZVS3KOEAAAAJ&hl=en&oi=ao), and [Xiao Zhang](https://scholar.google.com/citations?user=L-lz7CUAAAAJ&hl=en&oi=ao).

***

## News

Oct. 6, 2023 - We created this repo and our code will be released soon.

Oct. 7, 2023 - We uploaded the codes of the EDAC-based adversarial training on CIFAR-10 and the evaluation by AutoAttack.

***

## Our Code (To Be Released Soon)

To improve robust generalization, we propose a novel **E**xtragradient-type method to explicitly **D**ecrease **A**dversarial **C**ertainty, i.e., **EDAC**.

Our implementation of EDAC-based adversarial training (AT-EDAC) on CIFAR-10 is ``./at_edac_cifar10.py``.

### Usage

To train PreActResNet-18 on CIFAR-10: ``python at_edac_cifar10.py --model PreActResNet18``

To train WideResNet-34-10 on CIFAR-10: ``python at_edac_cfar10.py --model WideResNet``

To evaluate PreActResNet-18 on CIFAR-10: ``python eval_autoattack.py --arch PreActResNet18 --data CIFAR10``

To evaluate WideResNet-34-10 on CIFAR-10: ``python eval_autoattack.py --arch WideResNet --data CIFAR10``

### Trained Model

The PreActResNet-18 trained by AT-EDAC on CIFAR-10: [https://drive.google.com/file/d/1xC3kAMY5tHWSF3F2NNHRyPt4FerHYX1l/view?usp=sharing](https://drive.google.com/file/d/1xC3kAMY5tHWSF3F2NNHRyPt4FerHYX1l/view?usp=sharing).

The WideResNet-34-10 trained by AT-EDAC on CIFAR-10: [https://drive.google.com/file/d/1yMm_WGLz53ka6rn0x0SgqNTD9fYJxL-Q/view?usp=sharing](https://drive.google.com/file/d/1yMm_WGLz53ka6rn0x0SgqNTD9fYJxL-Q/view?usp=sharing).

***

## Reference Code
1. Robust Overfitting: [https://github.com/locuslab/robust_overfitting](https://github.com/locuslab/robust_overfitting)
2. AutoAttack: [https://github.com/fra31/auto-attack](https://github.com/fra31/auto-attack)
