# imSituVQA
imSituVQA is a corpus for Visual Question Answering Annotated with Semantic Frame Information. 

We took advantage of the imSitu dataset (http://imsitu.org/), developed for situation recognition. The imSitu dataset consists of about 125k images. Each image is annotated with one of  $504$ candidate verbs and its frame elements according to FrameNet. 

The imSituVQA creation process was composed of two primary steps: (1) Question answer template generation: Question answer templates are generated from imSitu abstract verb definitions. (2) Question answer pair realization:  The templates are filled with noun values from the imSitu annotated images.

The created imSituVQA dataset is stored in /data/imSituVQA.json 

## Load data
dataset us stored as a dictioanary (hash map) in imSituVQA.json.
```
import json
dataset = json.load(open('/data/imSituVQA.json','r')) 
```

## Images
imSitu images can be downloaded from http://imsitu.org/download/

## Splits
The dataset is split for three phased: train, dev and test 

## Format

Every dataset[PHASE_NAME] is a dictioanary with the following key items: 

question, answer, image_file, verb, question_frame_elements, response_frame_element

dataset[PHASE_NAME][ITEM] returns a list of all items for that phase. 
