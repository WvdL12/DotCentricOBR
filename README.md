# Braille data and OBR model results

## Datasets

Datasets available for use sourced from  
* [Ilya Ovodov, Angelina Set](https://github.com/IlyaOvodov/AngelinaDataset)  
* [DSBI Dataset](https://github.com/yeluo1994/DSBI)  

These datasets contain both Onesided and Twosided Braille documents and characters, with labels. The focus of the project is currently on onesided Braille document translation.  
The data labeling has been standardised from the different datasets. To account for generality, the label system used describes the dots present in a given Braille character, rather than directly translating the character.  

The `Braille Document Data` directory contains the raw Braille document datasets, with label files for character bounding boxes and labels, split into training, validation and testing sets.  
The `Structured Character Data` directory is intended for the extracted image data for the Braille characters included in the above datasets, with labels, structured as numpy array files. However, Github data quotas and storage limits prevents adding these files directly.  

## Model tuning

Hyperparameter tuning logs for model refinement and training were recorded in JSON format, stored under the `Hyperparameter tuning` directory.

## Performance results

The `Model Performance Results` directory includes performance results and model predictions used in masters research at Stellenbosch University, and included in an article submitted for publishing under the Journal of Universal Computer Science.
Models were trained under different data resampling scenarios, and with different classification approaches -- namely, multiclass and multilabel classification.
The predictions and performances on test sets include in-distribution test results on the Angelina dataset, which was used in training, as well as out-of-distribution (ood) test results on the DSBI dataset.

Experimental augmentations include Brightness, Noise and Rotation experiments to evaluate the robustness of each model to extreme data conditions.
