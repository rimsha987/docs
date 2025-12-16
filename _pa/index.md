---
layout: base
title:  'Punjabi UD'
udver: '2'
---

# UD for Punjabi <span class="flagspan"><img class="flag" src="../../flags/svg/PK.svg" /></span> <span class="flagspan" style="padding-left:1em"><img class="flag" src="../../flags/svg/IN.svg" /></span>

##  Punjabi-Rang (Shahmukhi)
This repository contains an extension of the **Punjabi Universal Dependencies (UD) treebank** with manually annotated data in **Shahmukhi Punjabi**.The treebank follows **Universal Dependencies v2** guidelines .

## Language and Script Punjabi-Rang

- Language: Punjabi (Western / Pakistan)
- Script: Shahmukhi
- UD version: v2

 ## Data Description Punjabi-Rang

The dataset includes written Punjabi texts from multiple genres:

- Narrative prose
- Cultural commentary
- Argumentative and persuasive discourse
- Conditional and evaluative constructions

The data covers a wide range of syntactic phenomena common in contemporary Punjabi, including:
- Copular and non-verbal predicates
- Light verb constructions
- Relative clauses with explicit relativizers
- Conditional clauses and discourse sequencing
- Passive and impersonal constructions


## Tokenization and Word Segmentation

* Tokenize with whitespace and punctuation basically.
* Compounds with hyphens should be split.
* Some clitics have apostrophes at the beginning and could be written merged with the previous word (e.g. 'ਚ "in"). These should be tokenized separately.

In addition, the following conventions are applied for Punjabi-Rang
* Shahmukhi-specific punctuation variants are normalized and tokenized as separate PUNCT tokens
* In argumentative and discourse-heavy texts, discourse particles (e.g. پر, تاں, وی) are always tokenized as independent.
* Quotation marks and emphasis punctuation used in persuasive discourse are tokenized separately.

  ## Annotation Principles

- Annotation follows Universal Dependencies v2 guidelines.
- Full UPOS tagset is used.
- Light verbs are annotated using appropriate `compound` subtypes where applicable.
- Relative clauses introduced by explicit relativizers are annotated as `acl:relcl`.


### Tags

* Use the full range of UPOS tags.
* Aspectual light verbs should be tagged [VERB]() since they take full inflectional paradigms.
  * Pay special attention to ਜਾਣਾ "to go",  which is usually [VERB]() (including as a light verb) but [AUX]() if it is passivising a verb.
 ### Morphology Punjabi-Rang
 The treebank Punjabi-Rang also uses the full UPOS tagset defined by Universal Dependencies.
 Verbs and auxiliaries are distinguished based on syntactic function. ہونا is annotated as AUX
 when used as a copula or auxiliary and as VERB otherwise.

### Features Punjabi-Rang
 Morphological features are annotated where they are overtly marked and reliably recoverable. Common features include Number,  Gender, Person, Tense, Mood, VerbForm, and Aspect. Features that are ambiguous or not morphologically explicit in Shahmukhi   Punjabi are left unspecified.

## Syntax

* Special relations:
  * [acl:relcl]() for relative adnominal clauses. These have to have a relative pronoun in them (otherwise just [acl]()).
  * [aux:pass]() for passive auxiliary ਜਾਣਾ.
  * [compound:lvc]() for noun/adjective + verb constructions.
  * [compound:redup]() for reduplication.
  * [compound:svc]() for aspectual light verbs.
  * [nsubj:pass]() for passivized subjects.

* Special relations (Punjabi-Rang):
  * [nmod:poss]() for genitive possessive constructions marked by **دا / دی / دے**  
    (e.g. *پنجاب دی ثقافت*, *محبت دا اظہار*, *محنت دا پھل*).
  * [obl:tmod]() for temporal oblique modifiers  
    (e.g. *ویلے*, *بعد*, *وار*).

## Treebanks

There are [1](../treebanks/pa-comparison.html) Punjabi UD treebanks:

  * [Punjabi-PunTB](../treebanks/pa_puntb/index.html)
