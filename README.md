# Kaggle_Sirius-SPbSU-2022
Kaggle qualifier with CNN for SVHN dataset


The task was to classify house numbers. In the process of solving it, the following was done:
1) there was salt and sugar noise in all pictures. I tried to solve this problem with the median filter with some modification. After applying the filter the loss fell, but insignificantly, because of the fact that in some pictures there was too much noise and they were too blurry. Experimented with different augmentations - gave a slight increase in quality.
2) On some of the pictures present more than 1 number, how to solve this problem, I have not thought of, because the principle of "take the center digit" does not always work.
3) I tried to increase the original size of the picture (32 * 32) a few layers of deconvolution, it did not bring good
4. I also tried different modifications of CNN, including trying to teach a few different networks and make them into an ensemble. It did not increase the quality.
5) Studied the original data, because they were unbalanced, tried balancing (first cut everything down to 4 thousand per class, then, on the contrary, increased). This did not increase the quality.
6) I tried to look at the classes in which the model is trained more often, but how to use this information effectively, I have not thought of.
7) From the book I borrowed the function to pick up lr - it was not much different from the default. The best quality - 93.5% on the closed dataset from the site.
