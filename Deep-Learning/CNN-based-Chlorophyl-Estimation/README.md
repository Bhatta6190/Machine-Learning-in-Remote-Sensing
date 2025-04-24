# CNN for Chlorophyll Estimation using Spectral Leaf Data

This directory implements a  1D convolutional neural network (CNN) to estimate chlorophyll content from hyperspectral leaf reflectance data. The spectral data is processed to simulate top-of-atmosphere (TOA) conditions with realistic system noise, mimicking the AVIRIS-NG sensor with 425 spectral bands spanning the 0.4 to 2.5 µm wavelength range.

---

## Dataset

The data consists of:

- **425-band hyperspectral signatures** per leaf sample.
- **Chlorophyll content** labels for each sample.
- Data has been forward-modeled to TOA and includes **added noise** for realism.

---

## Model Architecture

Implemented in PyTorch using `nn.Conv1d`. The architecture is as follows:

- 8 convolutional layers with kernel size 3, stride 2
- LeakyReLU activations with slope 0.01
- Final fully connected layer for regression

## Result

<p align="center">
  <img src="./output.png" alt="model_output" width="60%"/>
</p>
<p align="center"><strong>Figure: Chlorophyll content prediction outcome CNN model</strong></p>

The codes and *Results* for this task are available in the python notebook file- `CNN-based-Chlorophyl-Estimation/1DCNN_chlorophyl_est.ipynb`.