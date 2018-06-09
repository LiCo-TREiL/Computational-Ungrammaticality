# RNN Simulations of Grammaticality Judgments on Long-distance Dependencies

#About
The study explores the ability of LSTM networks trained on a language modeling task to detect linguistic structures which are ungrammatical due to extraction violations (extra arguments and subject-relative clause island violations), and considers its implications for the debate on language innatism.

The results show that the current RNN model can correctly classify (un)grammatical sentences, in certain conditions, but it is sensitive to linguistic processing factors and probably ultimately unable to induce a more abstract notion of grammaticality, at least in the domain we tested.


## Task for the study includes:
### Task A: Subject vs. Object Relative Clauses
File: Test Dataset - TaskA-SubVsObjRC.csv
Fields inside:
<Test sentence>,<Cases>
where <Test sentence> are the instances for example:
and <Cases> indicated whether the instance is either subject extraction (given by *SubjectRC*) or an object extraction (by *ObjectRC*)

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
File: Test Dataset - 
