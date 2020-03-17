# ITSP - Autonomous-TA

## Developers

[Aman Bansal](https://github.com/aman0456)

[Sahil Shah](https://github.com/sahil00199)

[Preey Shah](https://github.com/preeyshah)

[Shourya Pandey](https://github.com/pandeyshourya140998)

## Getting Started

Autonomous TA is a web application developed using the Django framework. Targeted towards students, Autonomous-TA serves an educational purpose in the following ways:

#### (i) Framing questions and answers out of a sentence, a paragraph or a long text for the student to solve.

#### (ii) Grading the response of a student to a question framed from text.

This implementation has been done using Python.


## Project Description

To start with, a sentence parser was used, which beautifully parses the phrases and words of a sentence into its individual parts of speech as a tree. This was done using [The Stanford Parser](https://nlp.stanford.edu/software/lex-parser.shtml) and the Natural Language Toolkit by Python (NLTK). An example tree is given below:

![tree](https://cloud.githubusercontent.com/assets/28354250/26765443/aa514f66-4999-11e7-8a62-4bdb800f9a72.png)

Next, we recognised patterns in different trees, and generated questions of a certain type if a sentence matched a pattern. Basic patterns of [simple sentences](http://eslau.ca/lesson/unit62.php) and complex/compound sentences were found. We also used [this](https://pdfs.semanticscholar.org/8b8b/c447119b4428da46b80eca9cda0e7b89c553.pdf) and coded a set of rules that disallow generation of too vague questions.

For grading, we already have the questions and "model answers" for a text. The user inputs a response to thequestion framed. We then compare the response with our own answer, and grade suitably (by assigning optimal weights to different words) . Care is taken that someword written by the user might be a synonym or the negation of an antonym of the corresponding word in the answer. For instance, if the model answer contains the word "freedom", then full credit should be given to an answer that uses the word "independence" instead. Such synonyms and antonyms have been parsed from an [online thesaurus](https://www.merriam-webster.com/thesaurus).

## Conclusion

Autonomous-TA has a socio-educational purpose for 

#### (i) Students who wish to be challenged by solving an exhaustive set of questions

#### (ii) Professors and Instructors who wish to frame questions for students to solve.


## References

Bird, Steven, Edward Loper and Ewan Klein (2009), Natural Language Processing with Python. O’Reilly Media Inc.

We used [this](https://github.com/dasmith/stanford-corenlp-python)  repository for parsing.

