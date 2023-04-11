# Sentiment-Analysis-using-Hugging-Face-library
This GitHub repository provides a Python script that demonstrates how to perform sentiment analysis on a dataset of text data using the Hugging Face library.

This code demonstrates how to perform sentiment analysis on a column of text data in an Excel file using the Hugging Face library.
First, the code imports the required libraries pandas and transformers. The torch library is also imported, but is not directly used in the code.
Next, the code reads an Excel file named "data.xlsx" located in the same directory as the Python script into a Pandas DataFrame named df.

Then, the code loads a pre-trained sentiment analysis model from Hugging Face using the pipeline method. The model is configured to run on the CPU (device 0) by default, but can be changed to run on the GPU if available by passing device=-1.

After that, the code defines a function named get_sentiment that takes a text input and uses the Hugging Face model to perform sentiment analysis on the text. The function returns the sentiment ("positive" or "negative") and the sentiment score (a floating-point number between 0 and 1).

The code then uses the apply method of the DataFrame to apply the get_sentiment function to the "text" column of the DataFrame. The lambda function extracts the sentiment and score values returned by the get_sentiment function and creates new columns named "sentiment" and "score" to store these values.

Finally, the code prints the head of the DataFrame to verify that the data was processed correctly.

Note that you will need to install the transformers library using pip install transformers before running this code.
