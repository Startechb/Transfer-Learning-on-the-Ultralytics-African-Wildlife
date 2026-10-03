# Transfer-Learning-on-the-Ultralytics-African-Wildlife
# Author: Sylvia Njane (@startechb)

 Image classification of five flagship African species  buffalo, elephant, rhino, lion, leopard — using a pre-trained ResNet50 (TensorFlow/Keras), comparing feature extraction (frozen backbone) with fine-tuning (upper blocks unfrozen).

 Base data: Ultralytics African Wildlife (downloaded from the Ultralytics GitHub release) (zebra dropped)
 Lion/leopard added from the Kaggle 10 Big Cats of the Wild dataset
 Runs on Google Colab (T4 GPU)
#Progress done
  Step 1  Setup, data download, 5-class dataset construction done
  Step 2  Stratified 70/15/15 split, tf.data pipeline, augmentation done
  Step 3  Model construction (ResNet50 + custom head) done
 Step 4  Experiment A (feature extraction) and B (fine-tuning) done
 Step 5  Evaluation (plots, classification report, confusion matrix, results table)  done
Step 6  PDF engineering report (report/African_Wildlife_Engineering_Report.pdf)
Notebook: notebooks/African_Wildlife_Transfer_Learning.ipynb

 Results (test set, 240 images)
 Metric	A: feature extraction	B: fine-tuning
 Best validation accuracy	99.16 %	99.58 %
 Test macro F1	0.9858	0.9821
 Average epoch time	15.0 s	18.1 s
Fine-tuning gave no measurable gain (4 vs 5 test errors; exact McNemar p = 1.0). See the PDF report for error analysis.
