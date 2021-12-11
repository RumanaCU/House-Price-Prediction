# House-Price-Prediction
**Author**: Rumana Sultana, Mahsa Rahamian

House Price prediction using Data Mining

**Database to use:** -Zillow Home Value Index (ZHVI) & (ZHVF) <br /> 
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp; **Description:** Zillow Home Value Index dataset that is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type.<br />
&emsp;  &emsp; &emsp;  &emsp; &emsp;&emsp;  &emsp;<br />


**Technology to use:**  Linear Regression Model, <br />
                        &emsp; &emsp; &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;Gradient Boosting Regression<br />

**Platforms:** Jupyter notebook, Python3, Matplotlib, NumPy, SciPy, sklearn, etc. 

**Description of Project:**  goal of Data Mining Solution is to be able to predict with some accuracy (currently 45% for linear model) the future home prices for potential investors. 
   &emsp;  &emsp;  &emsp;&emsp; &emsp;  &emsp;  &emsp;&emsp;   <img src="work process1.png">
<br />
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**Figure 1: Basic Idea of the Project** <br />
<br />
**Work Done Under the Project:**  (1) Cirrently, I have trained the base model with sleep-edfx data set. The base model contains ten 1-dimentional convolution layers and five maxpolling layers alongwith fully connected layers. The fully connected layer is connected to the 5 classes of sleep stages. The layers of base model is shown in figure below.<br />
<br />
&emsp;    &emsp;  &emsp;  &emsp;  <img src="New model.png">
<br />
     &emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp; &emsp;  &emsp; &emsp;  &emsp;  &emsp; &emsp; &emsp; **Figure 2: Layers of Base Model**
<br /><br />
**Result Analysis of Base Model:** The base model is trained for 30 epochs with pre-processed sleep data set. In Table 1, the number of examples are given used in the training. In one training no filtering is applied and the other is trained with filtered data by **Butterworth filtering** function (20 epochs done). For the both training I got above 85% accuracy with F1 score 78. My analysis is the second training accuracy would be higher than the first one if 100 epochs could be finished. The loss was used **categorical_crossentropy** and the optimizer is **adam** in both training session. The loss and validation loss with epochs is shown in Figure 3 (training 1) and the accuracy and validation accuracy with epochs is shown in Figure 4 (training 2). The performance of training is shown in Figure 5 and the visualization is shown in Figure 6. The labels clarification for visualization is 0->1, 1->2, 2->3, 3->4, 4->5. [Note: The LibreOffice Calc change the numbers even I gave it in correct sequence].
<br /><br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;  &emsp;&emsp;  **Table 1: Number of examples used in training**<br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;&emsp;<img src="Dataset.png">
<br /><br />
&emsp; <img src="loss vs val_loss.png"> &emsp; <img src="accuracy1.png"><br />
&emsp;&emsp;&emsp;&emsp;**Figure 3: Loss Visulization with Epochs** &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**Figure 4: Accuracy Visulization with Epochs**<br />
<br /><br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;&emsp;  &emsp;  <img src="accuracy.png"><br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;&emsp;  &emsp;  &emsp; &emsp;  &emsp;&emsp;&emsp;&emsp;**Figure 5: Performance of Training**<br /><br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;<img src="Graph1.png"><br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;&emsp;  &emsp;&emsp;&emsp;&emsp;**Figure 6: Visualization of Performance Factors**<br /><br />
**(2) Fine tune Model:** For fine tuning the base model, I could preprocessed the data set in Matlab only. I couldn't finish embedding the base model into finetuning model. However, after finetuning the visualization should be as Figure 7 (the visualization is taken from base paper). I expect to increase the performance about 3% for all the factors as my base model (accuracy for single chennel EEG is about 86%+) gave me better performance from base models(DeepSleepNet+: accuracy for single chennel EEG is 84.3% and SeqSleepNet+: accuracy for single chennel EEG is 84.5%) used in the original paper.
<br /><br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;&emsp;  &emsp;<img src="transfer.png"><br />
&emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;&emsp;&emsp;  &emsp;&emsp;**Figure 7: Visualization of Performance Factors after Finetune**<br /><br />
