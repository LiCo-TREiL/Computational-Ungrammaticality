# An LSTM adaptation study of (un)grammaticality

We propose a novel approach to the study of how artificial neural
network perceive the distinction between grammatical and ungrammatical
sentences, a crucial task in the growing field of synthetic
linguistics. The method is based on performance measures of language
models trained on corpora and fine-tuned with either grammatical or
ungrammatical sentences, then applied to (different types of)
grammatical or ungrammatical sentences. 

The results show that both in
the difficult and highly symmetrical task of detecting subject
islands and in the more open CoLA dataset, grammatical sentences give
rise to better scores than ungrammatical ones, possibly because they
can be better integrated within the body of linguistic structural
knowledge that the language model has accumulated.

## Study Includes:
### Affirmative
####  With complex object (AffObj) and with gerund in subject position (AffSubj)
File: Dataset - Affirmative_sub_obj.csv

Fields inside:<Sentence\>, <Cases\>

where <Sentence\> are the instances
and <Cases\> indicated whether the instance has either gerund in subject subject position (given by *AffSubj*) or has a complex object (by *AffObj*)

For example:
The below sentence is an example of affirmative sentence with complex object
```
"governments thought about fighting against these laws .", AffObj
```
where as
```
"fighting against these laws disgusted governments .",AffSubj
```
is an affirmative example with gerund in subject position.

Note this is a control scenario, both *AffSubj* and *AffObj* are grammatically correct and 
affirmative cases already contain most of the lexicon found in the RC/Wh sentences thus showing effect of lexical overlap.

### Corresponding root Wh-clauses 
Includes cases of Wh subject vs object sub-extraction.


```
(a) What did governments think about fighting against ? - WhObj
(b) *What did fighting against disgust governments ?    - WhSubj 
```
File: Dataset - Wh_sub_obj.csv

Fields inside:<Sentence\>, <Cases\>

where <Sentence\> are the instances
and <Cases\> indicated whether the instance has either gerund in subject subject position (given by *WhSubj*) or has a complex object (by *WhObj*)


### Relative Clause
Includes RC fragments of the sentences


```
(a) the laws that governments thought about fighting against - RelObj
(b) *the laws that fighting against disgusted governments    - RelSubj 
```


File: Dataset - Relative_clasue_sub_obj_extraction.csv

Fields inside:<Sentence\>, <Cases\>

where <Sentence\> are the instances
and <Cases\> indicated whether the instance has either gerund in subject subject position (given by *WhSubj*) or has a complex object (by *WhObj*)


* Paper -- to be uploaded later.
* To cite the paper:
```
@inproceedings{Zamparelli2019,
  	Author = {Shammur Absar Chowdhury and Roberto Zamparelli},
	Booktitle = {In Proc. of the 2019 ACL BlackboxNLP: Analyzing and Interpreting Neural Networks for NLP},
	Title = {An LSTM adaptation study of (un)grammaticality},
	Year = {2019}}
```
