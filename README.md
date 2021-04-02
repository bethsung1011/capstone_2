# capstone_2

# Bengali AI Handwritten Grapheme Classification

### Classify the components of handwritten Bengali

[dataset](https://www.kaggle.com/c/bengaliai-cv19)


**Files**

* train.csv
    - grapheme_root: the first of the three target classes
    - vowel_diacritic: the second target class
    - consonant_diacritic: the third target class
    - grapheme: the complete character

* test.csv
    - Every image in the test set will require three rows of predictions, one for each component. 
    This csv specifies the exact order for you to provide your labels. 
    - row_id: foreign key to the sample submission 
    - image_id: foreign key to the parquet file 
    - component: the required target class for the row (grapheme_root, vowel_diacritic, or consonant_diacritic)

* sample_submission.csv 
    - row_id: foreign key to test.csv
    - target: the target column

* (train/test).parquet  
    - Each parquet file contains tens of thousands of 137x236 grayscale images.

* class_map.csv    
    - Maps the class labels to the actual Bengali grapheme components.

# What are Graphemes? 

![](https://github.com/bethsung1011/capstone_2/blob/main/img/2%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/3%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/4%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/5%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/6%20_.gif)


[click here to read mpre about it](https://www.kaggle.com/c/bengaliai-cv19/discussion/123002)



# Exploratory Data Analysis

## Top 5 Consonant Diacritic in training data
![](https://github.com/bethsung1011/capstone_2/blob/main/img/Top%205%20Consonant%20Diacritic%20in%20training%20data.gif)

## Top 5 Vowel Diacritic in taining data
![](https://github.com/bethsung1011/capstone_2/blob/main/img/Top%205%20Vowel%20Diacritic%20%20in%20training%20data.gif)

## Most used top 10 Grapheme Roots in training set
![](https://github.com/bethsung1011/capstone_2/blob/main/img/top%2010%20Grapheme%20Roots%20in%20training%20data.gif)

## Least used 10 Grapheme Roots in training set
![](https://github.com/bethsung1011/capstone_2/blob/main/img/Least%20used%2010%20Grapheme%20Roots%20in%20training%20data.gif)

## Distribution of Consonant Diacritic

![](https://github.com/bethsung1011/capstone_2/blob/main/img/dist_Consonant%20Diacritic.gif)

## Distribution of Vowel Diacritic

![](https://github.com/bethsung1011/capstone_2/blob/main/img/dist_%20Vowel%20Diacritic%20.gif)

## Distribution of Grapheme Roots

![](https://github.com/bethsung1011/capstone_2/blob/main/img/dist_Grapheme%20Roots%20_.gif)


# Model summary

![](https://github.com/bethsung1011/capstone_2/blob/main/img/model%20summary.gif)

# Plot Model

![](https://github.com/bethsung1011/capstone_2/blob/main/img/model1_.gif)


# Graph
![Consonant Diacritic loss and accuracy Graph](https://github.com/bethsung1011/capstone_2/blob/main/img/Consonant%20Diacritic%20graph.gif)
![Vowel Diacritic loss and accuracy Graph](https://github.com/bethsung1011/capstone_2/blob/main/img/Vowel%20Diacritic%20graph_1.gif)
![Grapheme Roots loss and accuracy Graph](https://github.com/bethsung1011/capstone_2/blob/main/img/Grapheme%20Roots%20graph_.gif)


# Confusion Matrix
![Consonant Diacritic Confusion Matrix](https://github.com/bethsung1011/capstone_2/blob/main/img/Consonant%20Diacritic%20confusion%20matrix.gif)
![Vowel Diacritic Confusion Matrix](https://github.com/bethsung1011/capstone_2/blob/main/img/vowel%20confusion%20matrix_1.gif)
![Grapheme Roots Confusion Matrix](https://github.com/bethsung1011/capstone_2/blob/main/img/Grapheme%20Roots%20confusion%20matrix_.gif)

# Test Result Summary 

## Initially the model result was ugly
 
    * consonant_diacritic : 
        * Test score: 2.7546441555023193
        * Test accuracy: 0.6499999761581421

    * vowel_diacritic : 
        * Test score: 1.8599588871002197
        * Test accuracy: 0.5040000081062317

    * grapheme_root : 
        * Test score: 4.7975382804870605
        * Test accuracy: 0.02500000037252903

## Tweak
    * Maybe it was too shallow?    
        * added layers
        * added 0.0001 learning rate 
        * added 3 normalization 
        * training epochs = 2 / steps = 300
        * testing steps = 30 


## The model result did tiny bit better 

    * consonant_diacritic :
        * Test score: 0.8095945119857788
        * Test accuracy: 0.7200000286102295

    * vowel_diacritic : 
        * Test score: 1.0902100801467896
        * Test accuracy: 0.6190000176429749

    * grapheme_root :         
        * Test score: 4.837403774261475
        * Test accuracy: 0.02500000037252903



## Tweak
    * Maybe it was too deep?

        * reduced layers
        * reduced normalization 
        * decreased learning rate from 0.0001 to 0.00001
        * training epochs = 30/ steps = 180
        * testing steps = 30 



## This time it did little better than random guess except graphem root 

    * consonant_diacritic :
        * Test score: 0.6155465841293335
        * Test accuracy: 0.8299999833106995

    * vowel_diacritic : 
        * Test score: 1.0217700004577637
        * Test accuracy: 0.6370000243186951


    * grapheme_root :         
        * Test score: 4.705227375030518
        * Test accuracy: 0.03500000014901161



# Future Extensions of this project 

    * Combining 3 target labels and run at the same time 
    * Make ongoing hand-written word and compare with trained model 
    * Boost up accuracy
    * adding more characters to balance the sample variation

# What tools are used
![](https://github.com/bethsung1011/capstone_2/blob/main/img/what%20used.gif)