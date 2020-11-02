# Paradigm list

Most grammars of Western Armenian use 3 simple conjugation classes, but these don't cover the entire language. This is because of confounds like the following.
1) Derived verbs are conjugated differently than simple verbs. This includes causatives, passives, inchoatives.
2) Irregular verbs pattern differntly and show subregularities.
3) Defective verbs  don't have all the paradigm cells.
4) Suppletive verbs use different forms of the stem in different cells
5) Paradigms can slightly differ for vowel-initial vs. consonant-initial verbs. 

For more complete coverage, Boyacioglu 2010 uses 58 conjugation classes. We use his conjugation system. We slightly adapt his paradigms to incorporate passives and regularized irregular verbs. 

## Types of files
Paradigms are provided in four types of files:
1) `paradigms_arm.tsv`: Paradigms are presented in the Armenian script.
2) `paradigms_trans.tsv`: Paradigms are presented in their transliterated form, using the transliteration key described in `transliteration.md`.
3) `paradigms_arm_stem.tsv`: Paradigms are presented in the Armenian script. Paradigm cells are segmented into a stem and affixes. 
3) `paradigms_trans_stem.tsv`: Paradigms are presented in their transliterated form, using the transliteration key described in `transliteration.md`. Paradigm cells are segmented into a stem and affixes. 

## Structure of paradigm file
In this folder, we provide `xlxs` and `tsv` files which illustrates these classes. The structure of a file looks like the following. This is taken from the transliterated `paradigms_trans.tsv` file.

|Regularity	|Regular|	...| Suppletive|...|
|-|-|-|-|-|
|Class number|	Class 1|...|	Class 33|...
|Example lemma|	erkel|...|	əllal|...
|Example stem|	erk|...|	əll,eɣ|...
| ||||		
|evidential participle	|erker|	...| eɣer|...
|future participle|	erkelu|	...|əllalu|...|
|...|...|...|...|...| 

The different classes are organized on separate columns, starting from the second column. For example, the second column is for Class 1. 
The content of the paradigms are described on separate rows. The first four rows organize the classes in the following way:
1) **Regularity**: Type of class. Possible values are `Regular`, `Irregular`, `Defective`, or `Suppletive`.
2) **Class number**: Number of the class. Numbers are taken from Boyacioglu 2010 and range from Class 1 to Class 58
3) **Example lemma**: An example lemma that belongs to this classs, such as `erkel`.
4) **Example stem**: The stem of the example lemma. The stem is the part of the lemma without any suffixes, such as `erk`.

For most classes, the stem is a single item. But some classes use multiple stems in different contexts. For example, for the Class 33 lemma *əllal* uses two types of suppletive stems: *əll* and *eɣ*. These stems are listed in the **Example stem** row and separated with commas: `əll,eɣ`. Stems are useful for the stemmed files, described in *****.

The rest of the rows list the different paradigm cells, such as the evidential participle. For Class 1, the evidential participle of its example lemma *erkel* is `erker`. The full list of possible paradigm cells is described in ******


Depending on the class, the value of a paradigm cell can be:
1) **a single string**. For example, the evidential participle of Class 1 *erkel* is *erker*.
2) **multiple strings**. For some classes, a cell can have multiple possible values. For example for Class 3 *abril*, the imperative 2sg is either *abri՛r* or *abre՛*. These multiple forms are optional and separated by commas: `abri՛r, abre՛`.
3) **blank**. A blank cell means that the class is defective and doesn't have a realization for that cell. For example, Class 27 *grnam* doesn't have an an infinitival form. Its value for the `infinitival` cell is blank.
4) **the word 'periphrasis'**. Most classes use a periphrastic form for present negatives. For example for Class 1 *erkel*, the entry for `negative indicative present 1pl` is the word `periphrasis`. Periphrastic or complex tenses are described in the `complex_tenses.tsv` file.


## Stemming

The files `paradigms_arm.tsv` and `paradigms_trans.tsv` show the paradigm cells as a single string of letters. In the `paradigms_arm_stemmed.tsv` and  `paradigms_trans_stemmed.tsv`, the entries are divided into a stem and affixes. The stems are marked by angle brackets. Their value matche the values in the **Example stem** row.

For example, the table below is part of the `paradigms_trans_stemmed.tsv` file.


|Regularity	|Regular|	...| Suppletive|...|
|-|-|-|-|-|
|Class number|	Class 1|...|	Class 33|...
|Example lemma|	erkel|...|	əllal|...
|Example stem|	\<X\> = erk|...|	\<Xprs\> = əll, \<Xps\t> = eɣ|...
| ||||				
|evidential participle	|\<X\>er|	...| \<Xps\t>er|...
|future participle|	\<X\>elu|	...|\<Xprs\>alu|...|
|...|...|...|...|...|

For Class 1 *erkel*, it uses a stem *erk* which is represented as \<X\>. This is shown in the **Example stem** row: `<X> = erk`. The symbol \<X\> replaces *erk* in all of its paradigm cells, such as the evidential participle `<X>er` (= *erker*). 

Some classes like Class 33 *əllal* use multiple stems in different contexts. One of its stems *eɣ* is used in the evidential participle *eɣer* while another stem *əll* is used in future participle *əllalu*. These stems have unique names in the **Example stem** row: `<Xprs> = əll, <Xpst> = eɣ`. For Class 3, the symbols \<Xprs\> and \<Xpst\> replace the corresponding stems in the entire paradigm.

## Paradigm cells

The paradigm list keeps of track of at most 79 paradigm cells for each conjugation class. Some classes are defective and use less than the full 79 cells. In the paradigm files, the cells are distributed across 79 rows in alphabetical order. 
For illustration, I list these here based on their semantic grouping. For each table, I include a header but the header is not a paradigm cell.

1) Infinitivals

|Basic infinitival | Derived infinitval|
|-|-|
infinitival	|causative infinitival
negative infinitival|	passive infinitival

2) Participles

|Basic | Negative |
|-|-|
evidential participle	|	
future participle	|	negative future participle
past imperfect negative participle	|	
perfect participle	|	negative perfective participle
present negative participle	|	
prospective participle	|	negative prospective participle
subject participle	|	negative subject participle

3) Imperatives and prohibitives:

|Imperatives|Prohibitives|
|-|-|
imperative 2sg|	prohibitive 2sg
imperative 2pl|	prohibitive 2pl


4) Simple past

|Positive|Negative|
|-|-|
indicative past 1sg	|negative indicative past 1sg
indicative past 2sg	|negative indicative past 2sg
indicative past 3sg	|negative indicative past 3sg
indicative past 1pl|	negative indicative past 1pl
indicative past 2pl	|negative indicative past 2pl
indicative past 3pl	|negative indicative past 3pl

5) Present 

|Indicative|Subjunctive|Negative indicative|Negative subjunctive
|-|-|-|-|
indicative present 1sg	|	subjunctive present 1sg	|	negative indicative present 1sg	|	negative subjunctive present 1sg
indicative present 3sg	|	subjunctive present 3sg	|	negative indicative present 3sg	|	negative subjunctive present 3sg
indicative present 2sg	|	subjunctive present 2sg	|	negative indicative present 2sg	|	negative subjunctive present 2sg
indicative present 1pl	|	subjunctive present 1pl	|	negative indicative present 1pl	|	negative subjunctive present 1pl
indicative present 2pl	|	subjunctive present 2pl	|	negative indicative present 2pl	|	negative subjunctive present 2pl
indicative present 3pl	|	subjunctive present 3pl	|	negative indicative present 3pl	|	negative subjunctive present 3pl

6) Past imperfect

|Indicative|Subjunctive|Negative indicative|Negative subjunctive
|-|-|-|-|
indicative past imperfective 1sg	|	subjunctive past imperfective 1sg	|	negative indicative past imperfective 1sg	|	negative subjunctive past imperfective 1sg
indicative past imperfective 2sg	|	subjunctive past imperfective 3pl	|	negative indicative past imperfective 2sg	|	negative subjunctive past imperfective 2sg
indicative past imperfective 3sg	|	subjunctive past imperfective 3sg	|	negative indicative past imperfective 3sg	|	negative subjunctive past imperfective 3sg
indicative past imperfective 1pl	|	subjunctive past imperfective 1pl	|	negative indicative past imperfective 1pl	|	negative subjunctive past imperfective 1pl
indicative past imperfective 2pl	|	subjunctive past imperfective 2pl	|	negative indicative past imperfective 2pl	|	negative subjunctive past imperfective 2pl
indicative past imperfective 3pl	|	subjunctive past imperfective 3sg	|	negative indicative past imperfective 3pl	|	negative subjunctive past imperfective 3pl
