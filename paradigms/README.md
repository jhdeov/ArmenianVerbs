# Paradigm list

Most grammars of Western Armenian use 3 simple conjugation classes, but these don't cover the entire language. This is because of confounds like the following:
1) Derived verbs are conjugated differently than simple verbs. This includes causatives, passives, inchoatives.
2) Irregular verbs pattern differently and show subregularities.
3) Defective verbs  don't have all the paradigm cells.
4) Suppletive verbs use different stems in different cells
5) Paradigms can slightly differ for vowel-initial vs. consonant-initial verbs. 

For more complete coverage, Boyacioglu 2010 uses 58 conjugation classes. We use his conjugation system. We refine his paradigms to incorporate passives and regularized verbs. We did some other minor changes, described in the [differences](#Differences-from-Boyacioglu-2010) section.

## Types of files

In this folder, paradigms are provided in four types of files:
1) [paradigms_arm](paradigms_tsv/paradigms_arm.tsv): paradigms  in the Armenian script.
2) [paradigms_trans](paradigms_tsv/paradigms_trans.tsv): paradigms in their transliterated form.
3) [paradigms_arm_stemmed](paradigms_tsv/paradigms_arm_stemmed.tsv): stemmed paradigms  in the Armenian script. 
4) [paradigms_trans_stemmed](paradigms_tsv/paradigms_trans_stemmed.tsv): stemmed paradigms in their transliterated form. 

For stemmed paradigms, the paradigm cells are segmented into a stem and affixes. The transliterated forms are generated based on  the [transliteration key](../transliteration.md). The files have both `xlsx` and `tsv` versions. 
## Structure of a paradigm file

The structure of a paradigm file looks like the following. This is taken from the transliterated [paradigms_trans](paradigms_tsv/paradigms_trans.tsv) file.

|Class number|	Class 1|...|	Class 57|...
|-|-|-|-|-|
|Subclass|	|...|	|...
|Regularity	|Regular|	...| Suppletive|...|
|Initial segment	|V|	...| V|...|
|Example lemma|	erkel|...|	udel|...
|Example stem|	erk|...|	ud, ger|...
|Affix 	|-el|	...| -el|...|
|evidential participle	|erker|	...| gerer|...
|future participle|	erkelu|	...|udelu|...|
|...|...|...|...|...| 

The different classes are organized on separate columns, starting from the second column. For example, the second column is for Class 1.  The content of the paradigms is described on separate rows. The first 7 rows organize the classes in the following way:
1) **Class number**: Number of the class. Numbers are taken from Boyacioglu 2010 and range from Class 1 to Class 58.
2) **Subclass**: We refine Boyacioglu's classes and provide subclasses for some classesNumber of the class.
1) **Regularity**: Type of class. Possible values are `Regular`, `Archaic`, `Irregular`, `Defective`, or `Suppletive`.
1) **Initial segment**: The initial segment of all the lemmas of a class can either be a vowel `V` or a consonant `C`.
3) **Example lemma**: An example lemma that belongs to this classs, such as `erkel`.
4) **Example stem**: The stem of the example lemma. The stem is the part of the lemma without any suffixes, such as `erk`.
1) **Affix**: The sequence of segments which follows the stem.

For most classes, the stem is a single item. But some classes use multiple stems in different contexts. For example, the Class 57 lemma *udel* uses two types of suppletive stems: *ud* and *ger*. These stems are listed in the **Example stem** row and separated with commas: `ud, ger`. Stems are useful for the stemmed files, described in the [Stemming](#Stemming) section.

The rest of the rows list the different paradigm cells, such as the `evidential participle`. For Class 1, the evidential participle of its example lemma *erkel* is `erker`. The full list of possible paradigm cells is described in the [Paradigm cells](#Paradigm-cells) section.


Depending on the class, the value of a paradigm cell can be:
1) **a single string**: For example, the evidential participle of Class 1 *erkel* is *erker*.
2) **multiple strings**: For some classes, a cell can have multiple possible values. For example for Class 3 *abril*, the imperative 2sg is either *abri՛r* or *abre՛*. These multiple forms are optional and separated by commas: `abri՛r, abre՛`.
3) **blank**: A blank cell means that the class is defective and doesn't have a realization for that cell. For example, Class 27 *grnam* doesn't have an an infinitival form. Its value for the `infinitival` cell is blank.
4) **the word 'periphrasis'**: Most classes use a periphrastic form for present negatives. For example for Class 1 *erkel*, the entry for `negative indicative present 1pl` is the word `periphrasis`. Periphrastic or complex tenses are described in the [complex_tenses](../complex_tenses/) file.


## Stemming

The files `paradigms_arm.tsv` and `paradigms_trans.tsv` show the paradigm cells as a single string of letters. In the `paradigms_arm_stemmed.tsv` and  `paradigms_trans_stemmed.tsv` files, the entries are divided into a stem and affixes. The stems are marked by angle brackets. Their value matche the values in the **Example stem** row.

For example, the table below is part of the [paradigms_trans_stemmed](paradigms_tsv/paradigms_trans_stemmed.tsv) file.


|Class number|	Class 1|...|	Class 57|...
|-|-|-|-|-|
|Subclass|	|...|	|...
|Regularity	|Regular|	...| Suppletive|...|
|Initial segment	|V|	...| V|...|
|Example lemma|	erkel|...|	udel|...
|Example stem|	\<X\> = erk|...|	\<Xprs\> = ud, \<Xpst\> = ger|...
|Affix 	|-el|	...| -el|...|
|evidential participle	|\<X\>er|	...| \<Xpst\>er|...
|future participle|	\<X\>elu|	...|\<Xprs\>elu|...|
|...|...|...|...|...|

For Class 1 *erkel*, it uses a stem *erk* which is represented as \<X\>. This is shown in the **Example stem** row: `<X> = erk`. The symbol \<X\> replaces *erk* in all of its paradigm cells, such as the evidential participle `<X>er` (= *erker*). 

Some classes like Class 57 *udel* use multiple stems in different contexts. One of its stems *ger* is used in the evidential participle *gerer* while another stem *ud* is used in future participle *udelu*. These stems have unique names in the **Example stem** row: `<Xprs> = ud, <Xpst> = ger`. For Class 57, the symbols \<Xprs\> and \<Xpst\> replace the corresponding stems in the entire paradigm.

For some classes, the imperative 2sg is just the stem with the exlamation mark, such as *ge՛r* 'eat!' for Class 57 *udel*. The exclamation mark is placed inside the verb. For convenience, its stem form is `<Xpst>՛` with the exclamation mark placed after the stem.

## Paradigm cells

The paradigm list keeps of track of at most 79 paradigm cells for each conjugation class. Some classes are defective and use less than the full 79 cells. Besides these 79 paradigm cells, there are also over 20 complex tense [constructions](../complex_tenses/). The paradigm list and complex-tense list partially overlap for negatives indicatives and prohibitives.

In the paradigm files, the cells are distributed across 79 rows in alphabetical order. For illustration, I list these cells here based on their semantic grouping. For each table, I include a header but the header is not a paradigm cell.

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

## Differences from Boyacioglu 2010
Boyacioglu provides the most complete coverage of Western Armenian verbs. Although our paradigm files and verb list files largely are adapted from Boyacioglu, we reorganized some minor details.
1) **Stems**: Boyacioglu 2010 doesn't explicitly state the stem of words. The stems are our own analysis. 
2) **Affixes**: Boyacioglu uses the morphological marker -ուլ (*-ul*) as the affix for Classes 21 and 22, but we use -նուլ (*-nul*).
3) **Subclass**: While still using Boyacioglu's class numbering, we set up subclasses for conjugations which slightly differ. For example, Classes 3 and 4 include both simple verbs and passive verbs. We set these two types of verbs apart.
4) **Obsolete verbs**: Boyacioglu listed paradigms for some archaic or obsolete verbs when end in the sequence -ուլ *-ul*. These are classes 7, 8, 21, 22. These verbs are no longer used in modern spoken Armenian.  We provide Boyacioglu's original paradigms in our verb list and paradigm list.
5) **Archaic verbs**: Boyacioglu set up classes 11, 12 for archaic verbs which end in the sequence -ուցանել *-ut͡sanel*. These verbs are treated as regular Class 1, 2 verbs in modern spoken Armenian. We provide Boyacioglu's original paradigms in our verb list and paradigm list.
5) **Causatives**: some causatives use an orthographic variant of the causative suffix. We set apart these verbs using a separate subclass based on orthography.
6) ***-anil* verbs**: Boyacioglu used separated classes (17, 18) for verbs that end in *-anil*. But these are conjugated the same as regular verbs in Class 3, 4 that end in *-il*. We reassign these verbs to Class 3, 4 and don't have a separate class for them.
7) **Class 26**: Classes 26 includes verbs with the suffix *-t͡ʃil* or the suffix *-il*. We reassign the verbs with *-il* into Class 44.


