# chatbotLLM

## LLM_Chatbot_Flask deploys a basic chatbot in flask. Hugging face model, microsoft/Phi-3-mini-4k-instruct is used to accomplish this

## flan-t5-xl chatbot - 

TFAutoModelForSeq2SeqLM: This is the TensorFlow version of a sequence-to-sequence language model, which is often used for tasks like translation or summarization. We are fine tuning the model on OpenOrca dataset by taking only 10000 entries as it's a huge dataset and would take 10 minutes to process the whole dataset even with GPU. We are training it only for 2 epochs and using adam optimizer of tensorflow. Rouche metrics is used to check scores.


##Sentiment Analysis Pipeline 
has been implemented too, to adjust the chatbot’s responses based on user sentiment. The Chatbot gives an empathetic response if the input is termed to have a "NEGATIVE" sentiment.

Methods used -
- Quantization
- Pruning - Using this to make the model better

## Model Distillation

Smaller model is trained to mimic the performance of a larger model. Smaller model is called student and larger model is called teacher



## Model Quantization

Model is smaller and performance is also better compared to normal model


Pruning: Implement model pruning using TensorFlow’s model optimization toolkit.
Quantization: Apply TensorFlow Lite for quantizing the model.
Integration: Update your Flask chatbot to load and use the optimized model.


## More about pruning_quant_fineTuned.ipynb

Purpose: This function prepares the dataset for a translation task from English to German.

Example input:

**{
    "translation": [
        {"en": "Hello", "de": "Hallo"},
        {"en": "How are you?", "de": "Wie geht's?"},
        {"en": "I love programming.", "de": "Ich liebe Programmieren."}
    ]
}**




