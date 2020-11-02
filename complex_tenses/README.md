# Complex tenses

Most meanings are marked by adding a suffix to the verb. But some paradigm cells utilize periphrasis or clitics. The list of complex constructions is taken from Boyacioglu 2010. 

## Types of complex-tense files

In this folder, we provide `xlsx` and `tsv` files which illustrates these complex-tense lists. There are types of files:
1) [complex_tenses](complex_tenses_tsv/complex_tenses.tsv): List of complex tense constructions.
2) [particles](complex_tenses_tsv/particles.tsv): List of particles or clitics used in complex tenses. 
2) [synthetic_negative](complex_tenses_tsv/synthetic_negative.tsv): Conjugation of the synthetic-negative auxiilary which is used in negative indicatives.
2) [other_auxiliaries](complex_tenses_tsv/other_auxiliaries.tsv): Brief description of other auxilaries. 

Armenian script is transliterated based on the [transliteration key](../transliteration.md).

## Structure of the complex-tenses list

The structure of the [complex_tenses](complex_tenses_tsv/complex_tenses.tsv) file looks like the following. 

|Construction|	Verb shape|	Auxiliary type	|Auxiliary tense|	Template|
|-|-|-|-|-|
|negative indicative present|	present negative participle|	Synthetic negative 	|synthetic-negative present|	Aux Ptcp
|...|...|...|...|...|
simple future|	subjunctive present	|	||	Fut V|
|...|...|...|...|...|

The constructions are listed starting from the second row. Information about every construction is provided in the different culumns. The first row describes the information provided in every column:

1) **Construction**: The name of the construction. The name encodes its meaning.
1) **Verb shape**: All constructions specify a certain shape for the verb, such as a type of participle. The right shapes are shown in the [paradigms](../paradigms/).
1) **Auxiliariy type**: Some constructions use an auxiliary verb. Possible auxiliary verbs are the synthetic-negative, short auxiliary, and long auxiliary.
1) **Auxiliary tense**: If an auxiliary is used, then the auxiliary is usually inflected for tense and agreement. 
1) **Template**: Order in which the verb and the other morphemes appear in the construction.

The construction can also utilize either auxilaries or simple morphemes like clitics. For example, the simple future uses the `Fut` clitic before the verb. A list of these clitics is described in the [particles](particles.tsv) file.

Boyacioglu 2010 doesn't discuss progressive constructions. We added those.

## Inflection for person
For simple verbs, Armenian has three persons (1,2,3) and distingushes singulars from plurals. Most of the complex tense constructions also mark person and nubmer. For example, for the `simple future`, the verb is described with the `subjunctive present` shape. But, its actual form ranges from `subjunctive present 1sg` to `subjunctive present 3pl`. 

If a construction uses an auxiliary, then the auxiliary carries all person, tense, and number marking for the construction. 
- For the synthetic-negative auxiliary, its inflection is described in the [synthetic_negative](complex_tenses_tsv/synthetic_negative.tsv) file. 
- The other two auxiliaries are  mentioned in the [other_auxiliaries](complex_tenses_tsv/other_auxiliaries.tsv) file, alongside their class number. Their full paradigm is in [paradigms](../paradigms/).



