# Verb list

The verb list is taken from Boyacioglu 2010. He provides a list of 3258 verbs and notes their conjugation class. This folder contains a modified version of his verb list.

## Types of verb list files

In this folder, there are two types of files:
1) [verblist_arm](verblist_tsv/verblist_arm.tsv): Verb list is presented in the Armenian script.
2) [verblist_trans](verblist_tsv/verblist_trans.tsv): Verb list is presented in its transliterated form.

The files have both `xlsx` and `tsv` versions.  The transliterated forms are generated based on  the [transliteration key](../transliteration.md).
## Structure of a verb list

The structure of a paradigm file looks like the following. This is taken from the transliterated [verblist_trans](verblist_tsv/verblist_trans.tsv) file.

|Index|	Verb|	Class number|	Subclass|	Example lemma|	Stem|	Regularity	|Initial segment	|Regular category|	Affix|
|-	|-|	- |	- |	-|	-|	 -|	- |	- |	  -|
1|	akut͡sel|	1|	 |  erkel|akut͡s|	Regular|	V|		E-Class|	-el|
|...	|...|... |... |...|	...| ...|...  |... |	  ...|	 
207|	paʒnvil	|4|	Passive|zzvil|	paʒn|	Regular	|C|	Passive|	-vil
|...	|...|... |... |...|	...| ...|...  |... |	  ...|	 

Verbs are listed starting from the second row. The first row describes the information provided in every column:

1) **Index**: Unique index of a verb, ranging from 1 to 3258
1) **Verb**: Citation form of the verb, usually the infinitival, such as `akut͡sel`.
1) **Class number**: Class number of the verb.
1) **Subclass**: Subclass of the verb's class. If a verb's class doesn't have any subclasses, the value in this column is blank.
1) **Example lemma**: Every class or subclass has an example lemma which is used in the [paradigm](../paradigms) files. For Class 1 verbs, the example lemma is `erkel`.
1) **Stem**: Stem of the citation form. This is usually the verb minus its infinitival suffix, such as `erk`.
1) **Regularity**: Verbs belong to classes which have different degrees of regularity. Possible values are `Regular`, `Archaic`, `Irregular`, `Suppletive`, and `Defective`.
1) **Initial segment**: The initial segment of all the lemmas of a class can either be a vowel `V` or a consonant `C`.
1) **Regular category**: If a verb belongs to a regular class, this field provides its basic category. Possible values are `E-Class`, `I-Class`, `A-Class`, `Causative`,`Passive`,  `Inchoative`, or blank.
1) **Affix**: The sequence of segments which follows the stem.

## Modifications
We slightly modified Boyacioglu's verb list to correct for typos and errors. The differences are listed in [modifications](modifications.md) file.

