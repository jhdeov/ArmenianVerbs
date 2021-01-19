# Verb list

The verb list is taken from Boyacioglu 2010. He provides a list of 3258 verbs and notes their conjugation class. This folder contains a modified version of his verb list. The modifications are explained in the [modifications](../paradigms/modifications.md) file.

## Types of verb list files

In this folder, there are two types of files:

1. [verblist_arm](verblist_tsv/verblist_arm.tsv): Verb list is presented in the Armenian script.
2. [verblist_trans](verblist_tsv/verblist_trans.tsv): Verb list is presented in its transliterated form.

The files have both `xlsx` and `tsv` versions.  The transliterated forms are generated based on  the [transliteration key](../transliteration.md). 
## Structure of a verb list

The structure of a paradigm file looks like the following. This is taken from the transliterated [verblist_trans](verblist_tsv/verblist_trans.tsv) file.

|Index|	Verb|	Class number|	Subclass|	Example lemma|	Stem|	Regularity	|Initial segment	|Regular category|	Affix| Translation | Transitivity |
|-	|-|	- |	- |	-|	-|	 -|	- |	- |	  -| -| -|  
|1|	akut͡sel|	1|	 |  erkel|akut͡s|	Regular|	V|		E-Class|	-e| | Transitive|
|...	|...|... |... |...|	...| ...|...  |... |	  ...|	... |...|
|207|	paʒnvil	|4|	Passive|zzvil|	paʒn|	Regular	|C|	Passive|	-vil| To divide... | Intransitive|
|...	|...|... |... |...|	...| ...|...  |... |	  ...|	... |... |

Verbs are listed starting from the second row. The first row describes the information provided in every column:

1. **Index**: Unique index of a verb, ranging from 1 to 3258
2. **Verb**: Citation form of the verb, usually the infinitival, such as `akut͡sel`.
3. **Class number**: Class number of the verb.
4. **Subclass**: Subclass of the verb's class. If a verb's class doesn't have any subclasses, the value in this column is blank.
4. **Example lemma**: Every class or subclass has an example lemma which is used in the [paradigm](../paradigms) files. For Class 1 verbs, the example lemma is `erkel`.
5. **Stem**: Stem of the citation form. This is usually the verb minus its infinitival suffix, such as `erk`.
6. **Regularity**: Verbs belong to classes which have different degrees of regularity. Possible values are `Regular`, `Archaic`, `Irregular`, `Suppletive`, and `Defective`.
7. **Initial segment**: The initial segment of all the lemmas of a class can either be a vowel `V` or a consonant `C`.
8. **Regular category**: If a verb belongs to a regular class, this field provides its basic category. Possible values are `E-Class`, `I-Class`, `A-Class`, `Causative`,`Passive`,  `Inchoative`, or blank.
9. **Affix**: The sequence of segments which follows the stem.
10. **Translation**: A translation of the verb taken from Kouyoumdjian 1970 "A Comprehensive Dictionary Armenian-English", available on [Nayiri](http://www.nayiri.com/search?l=en&dt=HY_EN&r=0&query=). If the translation was a redirection to another Armenian word, then we translated that verb too. If a verb is not listed in Kouyoumdjian, then we omit a translation. Of the 3258 verbs from Boyacioglu 2010, 2749 did not appear in Kouyoumdjian and were not translated.  
11. **Transitivity**: The transitivity of the verb. Possible values are `Intranstive`, `Transitive`,  `Both`, or `Neither`. The transitivity values are mostly taken from Kouyoumdjian 1970 with some additions and modifications, discussed in the [modifications](../paradigms/modifications.md) file.




