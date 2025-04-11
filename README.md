Steps to run program:

Clone repository and unzip CodeT5.zip.

DataSubsets.zip contains the split datasets which I created, but is not necessary to downlaod.

Setup Instructions

1. Open the Notebook in Colab
Go to Google Colab and upload CodeT5_IfPrediction.ipynb (File > Upload Notebook).
Or, if the repository is in Google Drive, open it directly.
2. Enable GPU
In Colab, go to "Runtime > Change runtime type" and select "GPU".
3. Upload Dataset Files
In Colab’s left sidebar, upload python_methods.csv and repos.csv from the dataset/ folder.
The other .csv files are not necessary as they will be overwritten during runtime anyways.


Running the Code
Method 1 (Recommended):
1. Open CodeT5_IfPrediction.ipynb in Colab.
2. Ensure that python_methods.csv is uploaded to the dataset.
3. Run cell 1 to install necessary libraries.
4. Skip cell 2, the program will use the already created csv file and cell 2 is lengthy.
5. Run the remaining cells in order.

Method 2 (Slower):
1. Open CodeT5_IfPrediction.ipynb in Colab.
2. Ensure that repos.csv is uploaded to the dataset.
3. Run all cells in order.

First cell installs required libraries (e.g., torch, transformers, datasets).
Second cell drills github through the metadata provided in repos.csv, quite time consuming.
Other cells load the dataset, model (Salesforce/codet5-small), tokenize data, train the model, and evaluate it.
The notebook will fine-tune the model on the training set and evaluate it on the test set.

2. View Results
Evaluation metrics (exact match, BLEU, CodeBLEU) will be printed in the notebook.
Predictions are saved in testset-results.csv with columns: input function, prediction correctness, expected if condition, predicted if condition, CodeBLEU score, and BLEU-4 score.
