# RNN Simulations of Grammaticality Judgments on Long-distance Dependencies

The study explores the ability of LSTM networks trained on a language modeling task to detect linguistic structures which are ungrammatical due to extraction violations (extra arguments and subject-relative clause island violations), and considers its implications for the debate on language innatism.

The results show that the current RNN model can correctly classify (un)grammatical sentences, in certain conditions, but it is sensitive to linguistic processing factors and probably ultimately unable to induce a more abstract notion of grammaticality, at least in the domain we tested.


## Study Includes:
### Task A: Subject vs. Object Relative Clauses
File: Test Dataset - TaskA-SubVsObjRC.csv
Fields inside:
<Sentence\>, <Cases\>
where <Sentence\> are the instances
and <Cases\> indicated whether the instance is either subject extraction (given by *SubjectRC*) or an object extraction (by *ObjectRC*)

For example:
The below sentence is an example of subject extraction
```
"the student that had seen her gave a brief speech .", SubjectRC
```
where as
```
"the student that she had seen gave a brief speech .",ObjectRC
```
is an object extraction example.

Note this task is to test the sensitivity of the network towards the position of the gap and to the type of intervening subject: a pronoun, a proper name or a full noun phrase. These instances are completely acceptable to adults.

### Task B: Wh extractions
Includes cases of Wh-extraction where the gap position could be empty (a) or filled by an overt element (b) (a personal pronoun, an indefinite pronoun, a demonstrative NP). The test set also includes a corresponding affirmative sentences.

```
(a) Which candidate/issue should the students discuss [Gap]?
(b) *Which candidate/issue should the students discuss {him / it / something else / this candidate / this issue}
```
File: Test Dataset - TaskB-Wh-extraction.csv
Fields inside:
<Sentences\>, <Type\>, <Has_Gap\>, <Level_embedding\>, <Gram\>
where <Sentence\> are the instances,
<Type\> = {WH or AFF}; WH represents Wh-Pattern and AFF indicates affirmative form of sentences.
<Has_Gap\> = {y or n}; y indicates the presence of gap [Gap] in the sentence and n represents that the gap has been filled.  
<Level_embedding\> = {0, 1 or 2}, represents level of embedding between the wh-element and the gap position
<Gram\> = {G or UG}.
G - Grammatical cases.
UG - Ungrammatical cases

### Task C: Subject and Relative Island Violations
File: Test Dataset - TaskC-Wh-islands.csv
Fields inside:
<Sentence\>, <Groups\>, <PatternType\>
where <Sentence\> are the instances,
<Groups\> = {NO, NS, NSp, RO, RS}
where:
  * Object, OBJ, NP extraction (NO)
  * Subject, SUBJ, NP extraction (NS)
  * SUBJ NP extraction from passives (NSp)
  * OBJ relative clause, RC, extraction (RO)
  * SUBJ RC extraction (RS)

<PatternType\> indicates the type of sentence,
includes values:
Wh-interrogatives, Y/N-interrogatives, and Affirmatives

Note that the islands are present in Wh-interrogatives patterns only. The other two pattern has been supplied as a point of reference.


* Paper -- to be uploaded later.
* To cite the paper:
```
@inproceedings{Zamparelli2018,
	Author = {Roberto Zamparelli and Shammur Absar Chowdhury},
	Booktitle = {Proc. of COLING: International Conference on Computational Linguistics},
	Title = {RNN Simulations of Grammaticality Judgments on Long-distance Dependencies},
	Year = {2018}}
```
