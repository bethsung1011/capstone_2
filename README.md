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
