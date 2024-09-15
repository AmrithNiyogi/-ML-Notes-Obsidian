

- Table that describes the performance of a classification model by grouping prediction into 4 categories - True Positives, True Negatives, False Negatives, False Positives.
- For example:
	- *True Positives(TP):* We correctly predicted they do have diabetes
	- *True Negatives(TN):* We correctly predicted they don't have diabetes
	- *False Negatives(FN):* We incorrectly predicted they do have diabetes (Type I error)
	- *False Positives(FP):* We incorrectly predicted they don't have diabetes (Type II error)
- **Accuracy** = (TP + TN) / N
- **Precision** = TP / (TP + FP)
	- Minimizes the number of FP
	- Precision shows how often an ML model is correct when predicting target class
- **Recall** = TP / (TP + FN)
	- Maximizing the number of TP
	- Recall tells how often an ML model identifies positive instances from all actual positive samples in a dataset.
- **F1-score**: Allows to trade off precision against recall.
	- Harmonic mean between precision and recall
	- $$1/F = 1/2(1/P + 1/R)$$

	[[Pasted image 20240802103319.png]]
	