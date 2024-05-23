# Generating Less Certain Adversarial Examples Improves Robust Generalization

Code for our paper _Generating Less Certain Adversarial Examples Improves Robust Generalization_ by [Minxing Zhang](https://scholar.google.com/citations?user=wsSLja0AAAAJ&hl=en&oi=ao), [Michael Backes](https://scholar.google.com/citations?user=ZVS3KOEAAAAJ&hl=en&oi=ao), and [Xiao Zhang](https://scholar.google.com/citations?user=L-lz7CUAAAAJ&hl=en&oi=ao). In this work, to improve robust generalization, we propose a general method to explicitly **D**ecrease **A**dversarial **C**ertainty, i.e., **DAC**.

***

### Abstract

This paper revisits the robust overfitting phenomenon of adversarial training. Observing that models with better robust generalization performance are less certain in predicting adversarially generated training inputs, we argue that overconfidence in predicting adversarial examples is a potential cause. Therefore, we hypothesize that generating less certain adversarial examples improves robust generalization, and propose a formal definition of adversarial certainty that captures the variance of the model's predicted logits on adversarial examples. Our theoretical analysis of synthetic distributions characterizes the connection between adversarial certainty and robust generalization. Accordingly, built upon the notion of adversarial certainty, we develop a general method to search for models that can generate training-time adversarial inputs with reduced certainty, while maintaining the model's capability in distinguishing adversarial examples. Extensive experiments on image benchmarks demonstrate that our method effectively learns models with consistently improved robustness and mitigates robust overfitting, confirming the importance of generating less certain adversarial examples for robust generalization.

***

### News

Oct. 6, 2023 - We created this repo and our code will be released soon.

Oct. 7, 2023 - We uploaded the codes of the DAC-AT on CIFAR-10 and the evaluation by AutoAttack.

Oct. 26, 2023 - We uploaded the codes of the DAC-TRADES and DAC-MART.

***

### Usage

To train DAC-AT on CIFAR-10:
```text
python dac_at_cifar10.py --model {OnWhichModelArchitecture}
```

To train DAC-TRADES on CIFAR-10:
```text
python dac_trades_cifar10.py --model {OnWhichModelArchitecture}
```

To train DAC-MART on CIFAR-10:
```text
python dac_mart_cifar10.py --model {OnWhichModelArchitecture}
```

To evaluate on CIFAR-10:
```text
python eval_autoattack.py --arch {OnWhichModelArchitecture} --data CIFAR10
```

### Trained Model

The PreActResNet-18 trained by DAC-AT on CIFAR-10: [https://drive.google.com/file/d/1xC3kAMY5tHWSF3F2NNHRyPt4FerHYX1l/view?usp=sharing](https://drive.google.com/file/d/1xC3kAMY5tHWSF3F2NNHRyPt4FerHYX1l/view?usp=sharing).

The WideResNet-34-10 trained by DAC-AT on CIFAR-10: [https://drive.google.com/file/d/1yMm_WGLz53ka6rn0x0SgqNTD9fYJxL-Q/view?usp=sharing](https://drive.google.com/file/d/1yMm_WGLz53ka6rn0x0SgqNTD9fYJxL-Q/view?usp=sharing).

***

### Reference Code
1. Robust Overfitting: [https://github.com/locuslab/robust_overfitting](https://github.com/locuslab/robust_overfitting)
2. TRADES: [https://github.com/yaodongyu/TRADES](https://github.com/yaodongyu/TRADES)
3. MART: [https://github.com/YisenWang/MART/tree/master](https://github.com/YisenWang/MART/)
4. AutoAttack: [https://github.com/fra31/auto-attack](https://github.com/fra31/auto-attack)
