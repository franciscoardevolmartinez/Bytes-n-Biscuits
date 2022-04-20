# Transmission spectra of exoplanets


The dataset is divided into a training and test set (Training: training.npy; Test: testing.npy).

training.npy is a (79999, 18) array and testing.npy is a (20001, 18) array. Each row represents an individual synthetic spectrum and their corresponding parameters. The transit depths (in percentages) are given in the first 13 columns, and the parameters in the 5 remaining ones.

The parameters are: temperature, log(H2O), log(HCN), log(NH3) and a grey cloud opacity.

There is also an actual observation of WASP-12b, which you can use to test your trained machine learning algorithm.

The training and testing datasets don't contain the wavelength values, but these can be taken from the WASP-12b observation.
