---
layout: base
title: UD for Punjabi
udver: 2
---


# UD for Punjabi <span class="flagspan"><img class="flag" src="../../flags/svg/PK.svg" /></span> <span class="flagspan" style="padding-left:1em"><img class="flag" src="../../flags/svg/IN.svg" /></span>

## Tokenization and Word Segmentation

* Tokenize with whitespace and punctuation basically.
* Compounds with hyphens should be split.
* Some clitics have apostrophes at the beginning and could be written merged with the previous word (e.g. 'چ "in"). These should be tokenized separately.

**Additional tokenization details For Rang punjabi:**

* Keep punctuation as separate tokens This includes ، : ؟ ۔ and also quote like symbols that appear in the data.
* Treat postpositions and case markers as separate tokens tagged ADP, attached to the noun or pronoun with relation case for example نوں وچ توں دا دی دیاں.
* Parentheses and brackets are tokenized as punctuation and attached with punct to the nearest relevant head, often the predicate of the main clause.


## Morphology

* Use the full range of UPOS tags.
* Aspectual light verbs should be tagged [VERB]() since they take full inflectional paradigms.
* Pay special attention to ਜਾਣا "to go",  which is usually [VERB]() (including as a light verb) but [AUX]() if it is passivising a verb.

**Additional tagging patterns For Rang punjabi:**

* Copular ہونا is tagged AUX and used as cop with nominal or adjectival predicates, where the predicate is the root for example “میں چھ سال دا ساں” where سال is the root and ساں is cop.
* The same lemma ہونا is also tagged AUX  when the main predicate is verbal and the auxiliary carries tense or agreement.
* Negation like “نہیں” is tagged PART and often attaches as advmod to the predicate, including nominal predicates.
  
  
### Features

**Features For Rang punjabi:**

 • Aspect: Imp, Perf  
 • Case: Abl, Acc, Nom  
 • Degree: Pos  
 • Gender: Fem, Masc  
 • Mood: Imp, Ind  
 • NumType: Card  
 • Number: Plur, Sing  
 • Person: 1, 2, 3  
 • Poss: Yes  
 • PronType: Dem, Ind, Prs, Rel  
 • Reflex: Yes  
 • Tense: Fut, Past, Pres  
 • VerbForm: Fin, Inf, Part 


## Syntax

* Special relations:
  * [acl:relcl]() for relative adnominal clauses. These have to have a relative pronoun in them (otherwise just [acl]()).
  * [aux:pass]() for passive auxiliary ਜਾਣا.
  * [compound:lvc]() for noun/adjective + verb constructions.
  * [compound:redup]() for reduplication.
  * [compound:svc]() for aspectual light verbs.
  * [nsubj:pass]() for passivized subjects.

**Additional special relations For Rang punjabi:**

  * [obl:arg]() — used for arguments marked by postpositions
  * [obl:tmod]() — used for temporal oblique modifiers that express time or duration.
  * [obl:agent]() — used to mark an explicit agent phrase.
  * [det:poss]()— used when a possessive determiner modifies a noun directly.
  * [nmod:poss]() — used for possessive nominal dependents where possession is marked by a genitive postposition


## Treebanks

There are [2](../treebanks/pa-comparison.html) Punjabi UD treebanks:

  * [Punjabi-PunTB](../treebanks/pa_puntb/index.html)
  *  Punjabi Rang

