# Clutter Detection in Radar Applications

This repo holds my work during the time I spent at ABB AB as a thesis worker. 

## Abstract 

Radars have been used for detection purposes in safety applications (i.e., blind spot detection radar in cars) extensively. The existing detection methods, however, are not flawless. So far, the main focus of these methods is on detecting an object based on its reflectiveness. 

In this thesis, the limitation of conventional methods are addressed, and alternative approaches are proposed. The main objective is to model/identify the noise with statistical and machine learning approaches as an alternative to conventional methods that focus on the object. The second objective is to improve the time efficiency of these methods. 

The data for this thesis contains measurements collected from radars at ABB AB, Sweden. These measurements reflect the received signal strength. These radars are meant to be used in safety applications, such as in industrial environments. Thus, the trade-off between accuracy and complexity of the algorithms is crucial.

One way to ensure there is nothing but noise in the surveillance field of the radar is to model the noise only. A new input can then be compared to this model and be classified as noise or not noise (object). One-class classifiers can be employed to approach this problem as they only need noise for training; hence they have been one of the initial proposals in this thesis. Alternatively, binary classifiers are investigated to classify noise and object given a new input data. Moreover, a mathematical model for noise is computed using the Fourier series expansion. 
While the derived model holds useful information in itself, it can be used, e.g., for hypothesis testing purposes. Furthermore, to make the classification m ore time-efficient, dimension reduction methods are considered.  Feature extraction has been performed for this purpose with the help of the derived noise model.

In order to evaluate the performance of the considered methods, three different datasets have been formed. In the first dataset, the collected raw data has been preprocessed and used as the input to the considered algorithms. The second dataset consists of the features extracted from the preprocessed data. Finally, in the last dataset, the derived mathematical noise model is used to calculate the features. The methods are then carried out on these datasets for comparison over time efficiency and accuracy.


The One-class SVM seems to be the best candidate for this application considering the trade-off between accuracy and time efficiency. There has been a significant improvement in the time efficiency of all the methods after using dimension reduction techniques. However, that has been achieved with the cost of a small accuracy degradation. The question of if it is worth to use dimensionality reduction is best answered by the application needs considering the trade-off between accuracy and time efficiency.
