# csci544-assignment-4-named-entity-recognition-solved
**TO GET THIS SOLUTION VISIT:** [CSCI544 Assignment 4-Named entity recognition Solved](https://www.ankitcodinghub.com/product/csci544-assignment-4-named-entity-recognition-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93669&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI544 Assignment 4-Named entity recognition Solved&nbsp;&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

Introduction

This assignment gives you hands-on experience on building deep learning models on named entity recognition (NER). We will use the CoNLL-2003 corpus to build a neural network for NER. The same as HW3, in the folder named data, there are three files: train, dev and test. In the files of train and dev, we provide you with the sentences with human-annotated NER tags. In the file of test, we provide only the raw sentences. The data format is that, each line contains three items separated by a white space symbol. The first item is the index of the word in the sentence. The second item is the word type and the third item is the corresponding NER tag. There will be a blank line at the end of one sentence. We also provide you with a file named glove.6B.100d.gz, which is the GloVe word embeddings [1].

We also provide the official evaluation script conll03eval to evaluate the results of the model. To use the script, you need to install perl and prepare your prediction file in the following format:

idx word gold pred (1)

where there is a white space between two columns. gold is the gold-standard NER tag and pred is the model-predicted tag. Then execute the command line:

perl conll03eval &lt; {predicted f ile}

where {predicted file} is the prediction file in the prepared format.

1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Task 1: Simple Bidirectional LSTM model

The first task is to build a simple bidirectional LSTM model (see slides page 43 in lecture 12 for the network architecture) for NER.

Task. Implementing the bidirectional LSTM network with PyTorch. The architecture of the network is:

Embedding → BLSTM → Linear → ELU → classifier

The hyper-parameters of the network are listed in the following table:

embedding dim 100

number of LSTM layers 1

LSTM hidden dim 256 LSTM Dropout 0.33

Linear output dim 128

Train this simple BLSTM model with the training data on NER with SGD as the optimizer. Please tune other parameters that are not specified in the above table, such as batch size, learning rate and learning rate scheduling.

What are the precision, recall and F1 score on the dev data? (hint: the reasonable F1 score on dev is 77%.

Task 2: Using GloVe word embeddings

The second task is to use the GloVe word embeddings to improve the BLSTM in Task 1. The way we use the GloVe word embeddings is straight forward: we initialize the embeddings in our neural network with the corresponding vectors in GloVe. Note that GloVe is case-insensitive, but our NER model should be case-sensitive because capitalization is an important information for NER. You are asked to find a way to deal with this conflict. What are the precision, recall and F1 score on the dev data? (hint: the reasonable F1 score on dev is 88%.

2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Bonus: LSTM-CNN model

The bonus task is to equip the BLSTM model in Task 2 with a CNN module to capture character-level information (see slides page 45 in lecture 12 for the network architecture). The character embedding dimension is set to 30. You need to tune other hyper-parameters of CNN module, such as the number of CNN layers, the kernel size and output dimension of each CNN layer. What are the precision, recall and F1 score on the dev data? Predicting the NER tags of the sentences in the test data and output the predictions in a file named pred, in the same format of training data. (hint: the bonus points are assigned based on the ranking of your model F1 score on the test data).

</div>
</div>
</div>
