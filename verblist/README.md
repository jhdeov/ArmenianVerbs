# Verb list

The verb list is taken from Boyacioglu 2010. He provides a list of 3258 verbs and provides their conjugation class. This folder contains a modified version of his verb list.

## Types of verb list files

In this folder, we provide `xlsx` and `tsv` files which illustrates these verb lists.  Verb lists in two types of files:
1) [verblist_arm](verblist_tsv/verblist_arm.tsv): Verb list is presented in the Armenian script.
2) [verblist_trans](verblist_tsv/verblist_trans.tsv): Verb list is presented in its transliterated form.

The transliterated forms are generated based on  the [transliteration key](../transliteration.md).
## Structure of the verb list

The structure of a paradigm file looks like the following. This is taken from the transliterated [verblist_trans](verblist_tsv/verblist_trans.tsv) file.

|Index	|Verb|	Class number|	Class example|	Stem|	Regularity|	Regular category|	Phonological marker|	Morphological marker| 
|-	|-|	- |	- |	-|	-|	 -|	- |	- |	  
1|	akut͡sel|	1|	erkel|	akut͡s|	Regular| 	E-Class| 	V-initial| -el	|	
2|	azadakrel|	1|	erkel|	azadakr	|Regular|	E-Class	|V-initial| -el	|
|...	|...|... |... |...|	...| ...|...  |... |	 

Verbs are listed started in the second row. Information about every verb is provided in the different culumnsThe first row describes the information provided in every column:

1) **Index**: Unique index of a verb, ranging from 1 to 3258
1) **Verb**: Citation form of the verb, usually the infinitival, such as `akut͡sel`.
1) **Class number**: Class number of the verb.
1) **Class example**: Every class has an example lemma which is used in the [paradigm](../paradigms) files. For Class 1 verbs, the example lemma is `erkel`.
1) **Stem**: Stem of the citation form. This is usually the verb minus its infinitival suffix, such as `erk`.
1) **Regularity**: Verbs belong to  classes which have different degrees of regularity. Possible values are `Regular`, `Archaic`, `Irregular`, `Suppletive`, and `Defective`.
Passive verbs aren't separated in Boyacioglu's system. They have the value `Regular (identical to 4)` or `Regular (identical to 3)`
1) **Regular category**: If a verb belongs to a regular class, this field provides its basic category. Possible values are `E-Class`, `I-Class`, `A-Class`, `Causative`,`Passive`,  `Inchoative`, or blank.
1) **Phonological marker**: Some classes are determined based on the first segment. Possible values are `V-initial`, `C-initial`, or blank.
1) **Morphological marker**: The main marker or suffix that marks this class. If this verb's class isn't distinguished by some suffix, then this column uses the value `Lexeme`.

## Notes

Minor notes on the verb list:
- Boyacioglu uses the marker -ուլ (*-ul*) for Classes 21 and 22, but we use -նուլ (*-nul*).
- Some archaic verbs have unclear conjugations because the stem is vowel-final. But because they are archaic or obsolete, it is difficult to verify how they were conjugated.
- Some irregular verbs are optionally regularized in colloquial Western Armenian. This isn't noted in Boyacioglu 2010 or in our verb list.
