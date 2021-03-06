# Mach-Learn-Mat-Sci
**Predict materials band gap with machine learning algorithm**

New materials band gaps are usually calculated using Density Functional Theory (DFT). However, DFT often underestimate the values of band gaps. Also, it can be computationally expensive to get good results. To overcome this problem, assuming a number of materials with the right band gaps are known, machine learning can be used to predict the band gaps of new materials, and expedite the discovery of new materials with useful applications.</br>

This code bandgap.py written in Python shows that ternary materials' band gap can be predicted using just atomic mass as the only feature.</br>
Training data = 10,000 materials band gaps</br>
Cross-validation (CV) = 3,000 materials band gaps</br>
Feature = atomic mass in each compounds</br>
Algorithm = random forest regression (untuned)</br>

**Results:**</br>
Training score = 0.92</br>
Prediction score on CV = 0.75</br>
Mean avarage error on CV = 0.43 eV</br>
Mean squared error on CV = 0.78 eV</br>

**Plot:**</br>
![](https://github.com/wfgoh/Mach-Learn-Mat-Sci/blob/master/bandgap_predict.jpg)</br>
It looks like machine learning is capable to predict band gaps given only the atomic mass of each elements in the compounds. Even though a handful of compounds are predicted to be semiconductors or insulators (non-zero band gap) while in reality they are metal/semimetals (zero band gap), keep in mind that only the atomic masses are used to guide the predictions. Therefore, feature engineering and fine tuning can be done to improve the result.
