# Armenian verb paradigms
Armenian is an understudied and low-resource language. This repo contains the paradigms of all verbs in Western Armenian. A sample list of 3k verbs is provided, along with their conjugation class.

## About Armenian
Armenian is a low-resource Indo-European language. It has two standard dialects: Western Armenian and Eastern Armenian. Western Armenian is endangered and has fewer resources than Eastern Armenian. Western Armenian has a richer morphological system with:
- three basic conjugation classes based on three theme vowels: *-e-, -i-, -a-*
- three additional conjugation classes for causatives, passives, and inchoatives
- obsolete or archaic classes with the theme vowel *-u-*
- phonologically-conditioned allomorphy
- irregular verbs, including suppletive and defective verbs

The most systematic collection of Western Armenian paradigms is found in Boyacioglu [2010](https://www.asiatheque.com/en/book/hay-pay-les-verbes-de-larmenien-occidental-western-armenian-verbs). He documents 58 paradigms. 

## Resources
The [paradigms](paradigms/) folder describes 64 paradigms, based on Boyacioglu's 58 paradigms. A [README](paradigms/README.md) file explains the organization of the paradigm files. The paradigms are provided in:
1) the Armenian script,
2) a transliterated script, similar to IPA, and
3) a stemmed form.

The paradigms show the form of verb where only simple affixes are added. In addition, Armenian uses many periphrastic formations made up of a participle and an auxiliary. There are also constructions that use a verb and a clitic. These multi-unit constructions are described in the [complex_tenses](complex_tenses/) folder.

The [verblist](verblist/)  folder contains a lexicon of almost 3000 words. The list is taken from Boyacioglu 2010. It includes the conjugation class of every verb.

For all three folders, the files are  provided in both `.xlxs` or `.tsv`. Transliterated versions of the data are also provided. They are transliterated based on the [transliteration key](transliteration.md).

The paradigms match the system used in the [Apertium](https://github.com/jhdeov/apertium-hyw) morphological analyzer for Western Armenian.

## Using and citations

All material in this repo is open-source. If you use it, please cite the repo with the following citation. You can export a citation from our [Zenodo](https://zenodo.org/record/4397423) link.

> Nisan Boyacioglu, & Hossep Dolatian. (2020, December 29). Armenian Verbs: Paradigms and verb lists of Western Armenian conjugation classes (Version v.1.0.0). Zenodo. http://doi.org/10.5281/zenodo.4397423


