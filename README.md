This set of repositories contains projects that try to build computational linguistic approaches for creating or processing Question Under Discussion (QUD) structures based on text. The projects originated as part of a class called "Questions and Models of Discourse", co-taught by Tatjana Scheffler and Malte Zimmermann at the University of Potsdam in Summer 2018. 

## Background

*Questions under discussion* (Roberts, 1996) are a prominent discourse model in formal semantics and pragmatics. This model, which has been developed further in the meantime, postulates that implicit *questions* structure natural conversations. All conversations are seen to answer "the big question" (*What is the way things are?*), by successively addressing subquestions to this biggest question. This eventually yields a tree-like structure for the discourse.

In our projects, we addressed the issue of how to formalize the notions indicated in the linguistic literature and whether they are amenable to computational approaches. 

The individual projects contained in this repository are the following:

## 1. Analysing and Evaluating QUD structures
One issue with QUD trees is that they are often created ad-hoc by linguists to explain and motivate certain analyses. In order to evaluate the expressivity and validity of the model as a whole, though, one needs a data-driven approach to comparing and evaluating QUD structures. This project creates methods for comparing and evaluating QUD trees. In addition, a small corpus of QUD structures is created, which contains parallel QUD trees annotated on the same text by different human annotators. The methods of evaluation are applied to this novel corpus.

[Repository: QUD tree analysis](https://github.com/QUD-comp/analysis-of-QUD-structures)

## 2. Generating Potential Questions
A central problem for QUD analyses is which "next questions" are available at a given point in discourse. Onea (cit.) introduces the notion of *potential question* and presents a range of constraints/standard strategies for such potential questions based on linguistic phenomena. In this project, the given strategies from Onea are evaluated for their potential automation and are implemented in a system that automatically generates potential "follow-up" questions based on a given sentence.

[Repository: Generating potential questions](https://github.com/QUD-comp/potential-questions)

## 3. Ranking Potential Questions
Given a range of possible *potential questions* (see above), the QUD model makes some predictions as to their preferential order. This project implements a ranking system that evaluates the fit of a given question with regard to its preceding utterance. In order to do this, a new dataset is created for training a machine learning system for ranking questions.

[Repository: Ranking potential questions](https://github.com/QUD-comp/ranking-potential-questions)

## 4. Synthesizing QUD Trees from RST Annotations
QUD trees in effect impose a tree structure over a given discourse. There are other discourse models that also induce tree structures over discourse. In particular, Rhetorical Structure Theory (Mann/Thompson, 1988) is a formally and computationally well-studied coherence model for discourse that induces a global discourse tree. The question has been raised to what extent coherence models of discourse and QUD structures capture the same kinds of information. In this project, existing RST analyses of a microtext corpus are automatically transformed into QUD analyses. The method is evaluated on a small annotated corpus.

[Repository: Transform RST trees into QUD trees](https://github.com/QUD-comp/rst_to_qud)

## 5. Duplicate Question Classification
Finally, when comparing and evaluating QUD structures, individual *questions* need to be compared. Human-generated questions can be variable in form, even if their discourse role (or meaning) is the same. This project tackles the task of detecting when two questions ask for the same thing (are duplicates of each other). Next to other interesting uses, this kind of system is essential as a component when analysing and evaluating QUD trees (Project 1), as well as when evaluating other QUD processing systems (e.g., Project 4 which synthesizes QUD trees and then must compare them to the gold annotations). 

[Repository: Duplicate question classification](https://github.com/QUD-comp/duplicate-question-detection)

## Contact and Further Information

For further information, contact [Tatjana Scheffler](mailto:tatjana.scheffler@uni-potsdam.de)

## Some References

- Riester, A. (2018). Constructing QUD trees. In: Questions in Discourse, vol. 2.
- Roberts, C. (1998). Focus, the flow of information, and universal grammar. In P. Culicover, & L. McNally (Eds.), The Limits of Syntax (pp. 109–160). San Diego: Academic Press.
