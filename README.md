# Multi label Sentiment Analysis Bert
In this repository, you can have access to the code file of a kaggle competition project with Multi-label SA. 
I still used the method i used in the in the project: [Sentiment analysis with bert](https://github.com/Shahbodshs/Sentiment-analysis-bert), but in only one change,
This project was multi label so here is the changes: 
```python
test_predictions_labels = (tf.nn.softmax(test_predictions.logits, axis=-1)[:, 1] > 0.9).numpy().astype(int)
```
Instead i used the following code: 
```python
test_predictions_labels = np.argmax(test_predictions.logits, axis=1)
```
__THe reason behind this:___
The second approach (np.argmax(...)) assigns the predicted label based on which class has the highest logit for each sample.
The first approach assigns a label of 1 or 0 based on whether the probability of the second class exceeds a confidence threshold (0.9).

## My kaggle: 
Dont forget to check my kaggle profile for the codes and outputs: [My kaggle](https://www.kaggle.com/shahbodsobhkhiz)
## Dataset: 
I might not be aloud to share the dataset but you can get it from here: [Dataset](https://www.kaggle.com/competitions/nlp-sentiment-analysis-xm).
## Code access: 
You can have access to  the code in the Code branch
