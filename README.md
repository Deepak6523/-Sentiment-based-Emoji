# -Sentiment-based-Emoji


This code performs text analysis to detect emotions in a given text file (deep.txt) using predefined emotional mappings in another file (emotions.txt). Here's a breakdown of its functionality:

Importing Libraries:
The necessary libraries are imported:
string is used for punctuation removal.
collections.Counter helps in counting occurrences.
matplotlib.pyplot is used for plotting a bar chart.

Reading the Text File:
The content of deep.txt is read into the text variable.
Text Preprocessing:
Lowercasing: The text is converted to lowercase using text.lower() to ensure uniformity.
Removing Punctuation: The translate() function with str.maketrans() is used to remove punctuation marks from the text.
Tokenization: The cleaned text is split into individual words using the split() function.
Removing Stop Words:
A list of common English stop words (stop_words) is defined. The script iterates over tokenized_words and appends words not present in stop_words to final_words. This helps in filtering out less meaningful words.

Emotion Detection:
The script reads an emotions.txt file, where each line contains a word and its corresponding emotion, separated by a colon (:). If a word in final_words matches a word in emotions.txt, the corresponding emotion is added to the emotion_list.

Counting Emotions:
The Counter class is used to count the frequency of each emotion in emotion_list. This count is stored in the w variable.
Visualizing Emotions:
A bar chart is created using matplotlib to visualize the frequency of emotions. The bar heights correspond to the emotion counts from w. The x-axis labels are formatted using fig.autofmt_xdate(), and the plot is saved as graph.png and displayed using plt.show().

Summary
The code reads a text file, preprocesses the text by removing punctuation and stop words, identifies the emotions associated with certain words, counts these emotions, and then visualizes the results in a bar chart.
