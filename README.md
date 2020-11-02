# Armenian verb paradigms
Armenian is an understudied and low-resource language. This repo contains the paradigms of all verbs in Western Armenian. A sample list of 3k verbs is provided, along with their conjugation class.

## About Armenian
Armenian is a low-resource Indo-European language. It has two standard dialects: Western Armenian and Eastern Armenian. Western Armenian is endangered and has fewer resources than Eastern Armenian. Western Armenian has a richer morphological system with:
- three basic conjugation classes based on theme vowels: *-e-,-i-,-a-*
- three additional conjugation classes for causatives, passives, and inchoatives
- obsolete or archaic classes with the theme vowel *-u-*
- phonologically-conditioned allomorphy
- irregular verbs, including suppletive and defective verbs

The most systematic collection of Western Armenian paradigms is found in Boyacioglu [2010](https://www.asiatheque.com/en/book/hay-pay-les-verbes-de-larmenien-occidental-western-armenian-verbs). He documents 58 paradigms 

## Resources
In the [paradigms](paradigms/) folder, 58 paradigms are provided in both `.xlxs` or `.tsv`. A [README](paradigms/README.md) file explains the organization of the files. The paradigms include:
- complex tenses
- particles and auxiliaries
- stemmed paradigms

The paradigms show the form of verb where only simple affixes are added. In addition, Armenian uses many periphrastic formations made up of a participle and an auxiliary. There are also constructions that use a verb and a clitic. These multi-unit constructions are described in the [complex_tenses](complex_tenses/) folder.

In the [verblist](verblist/)  folder, a lexicon of almost 3000 words is provided in both `.xlxs` or `.tsv`. The list is taken from Boyacioglu 2010. It includes the conjugation class of every verb.

Transliterated versions of the paradigms and verblist are also provided. They are transliterated based on the [transliteration key](transliteration.md).

The paradigms match the system used in the [Apertium](https://github.com/jhdeov/apertium-hyw) morphological analyzet for Western Armenian.

