# capstone_2

# Bengali AI Handwritten Grapheme Classification

### Classify the components of handwritten Bengali

[dataset](https://www.kaggle.com/c/bengaliai-cv19)


**Files**

* train.csv

    - image_id: the foreign key for the parquet files
    - grapheme_root: the first of the three target classes
    - vowel_diacritic: the second target class
    - consonant_diacritic: the third target class
    - grapheme: the complete character. Provided for informational purposes only, you should not need to use this.

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

    - Each parquet file contains tens of thousands of 137x236 grayscale images. The images have been provided in the parquet format for I/O and space efficiency. Each row in the parquet files contains an image_id column, and the flattened image.

* class_map.csv

    - Maps the class labels to the actual Bengali grapheme components.*


<!-- ![Grapheme](img/2.png)
![Why Grapheme?](img/3.png)
![Why Common Graphemes in Contest?](img/4.png)
![Bengali Orthography](img/5.png)
![Labels example](img/6.png) -->

![](https://github.com/bethsung1011/capstone_2/blob/main/img/2%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/3%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/4%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/5%20_.gif)

![](https://github.com/bethsung1011/capstone_2/blob/main/img/6%20_.gif)




# Most used top 10 Grapheme Roots in training set
![](https://github.com/bethsung1011/capstone_2/blob/main/img/top%2010%20Grapheme%20Roots%20in%20training%20data.gif)

# Least used 10 Grapheme Roots in training set
![](https://github.com/bethsung1011/capstone_2/blob/main/img/Least%20used%2010%20Grapheme%20Roots%20in%20training%20data.gif)

# Top 5 Vowel Diacritic in taining data
![](https://github.com/bethsung1011/capstone_2/blob/main/img/Top%205%20Vowel%20Diacritic%20%20in%20training%20data.gif)

# Top 5 Consonant Diacritic in training data
![](https://github.com/bethsung1011/capstone_2/blob/main/img/Top%205%20Consonant%20Diacritic%20in%20training%20data.gif)

# Distribution of Grapheme Roots

![](https://github.com/bethsung1011/capstone_2/blob/main/img/dist_Grapheme%20Roots%20_.gif)

# Distribution of Vowel Diacritic

![](https://github.com/bethsung1011/capstone_2/blob/main/img/dist_%20Vowel%20Diacritic%20.gif)

# Distribution of Consonant Diacritic

![](https://github.com/bethsung1011/capstone_2/blob/main/img/dist_Consonant%20Diacritic.gif)


# Model 

![](https://github.com/bethsung1011/capstone_2/blob/main/img/model1_.gif)


# Graph



