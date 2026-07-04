# 🎬 Movie Review Sentiment Analysis with DistilBERT

## 📌 Project Overview
In this project, I fine-tuned a pre-trained **DistilBERT** model using the Hugging Face `transformers` library to classify movie reviews as either Positive or Negative. The model was trained on a subset of the IMDB dataset.

## 🛠️ Tools & Libraries Used
* Python
* Google Colab (T4 GPU)
* Hugging Face (`transformers`, `datasets`, `evaluate`)
* PyTorch

 📊 Training Details & Results
 Dataset: StanfordNLP IMDB Movie Reviews (1,000 training, 500 testing)
 Epochs: 3
 Final Accuracy: 87.6%  

 🧪 Error Analysis & "Tricky" Testing
To test the model's true understanding, I fed it custom "tricky" reviews containing sarcasm and mixed emotions. 

Example of a success:
Review: "The trailer looked amazing... but the actual movie was a complete disaster."
 Model Prediction:* Negative (Correct!)

Example of a failure (Edge Case):
Review: "The first half was incredibly boring and I almost walked out. But the twist at the end made it the best movie I've seen all year!"
  Model Prediction:* Negative (Incorrect)
  Why it failed:* The AI heavily weighed words like "boring" and "walked out" without understanding the twist at the end. This shows the limitation of small training datasets in capturing deep human context.

 💡 Conclusion
This project successfully demonstrated how to take an existing Large Language Model and fine-tune it for a specific downstream task. In the future, training on the full 25,000-review dataset would likely improve the model's ability to detect sarcasm.
