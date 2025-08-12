# D.2 Necessary and Sufficient - Examples

The appendix contains an extended version of [Necessary Conditions and Sufficient Definitions](<../../2 snomed-ct-logical-model/2.3 concept-definitions/2.3.2-necessary-conditions-and-sufficient-definitions.md>) supported by more detailed examples.

## Assertions

The stated view of concept definition consists of one or more assertions made by SNOMED CT authors.

## Necessary Conditions

Each time an assertion is made about a concept, an author must decide if that assertion is a necessary condition. If the assertion is always true for that concept and its subtypes, it is a necessary condition.

* This implies that for all instances of that concept or its subtypes, the assertion must be true, even if it has not been explicitly stated.
* A necessary condition is defined as a characteristic that is always true of a concept.

#### Example

* If you have a [71620000 |fracture of femur|](http://snomed.info/id/71620000) , the morphological abnormality [72704001 |fracture|](http://snomed.info/id/72704001) must be present. Therefore, [116676008 |morphology|](http://snomed.info/id/116676008) = [72704001 |fracture|](http://snomed.info/id/72704001) is a _necessary condition_ of [71620000 |fracture of femur|](http://snomed.info/id/71620000) .

## Sufficient Definitions

For each concept an author must decide if there are one or more sets of assertions that form a sufficient definition of that concept. A set of assertions is a sufficient definition if it distinguishes a concept and its subtypes from other concepts.

* This implies that if all assertions in the set are true for a concept, it must be an instance of the defined concept or a subtype of that concept.
* A sufficient definition is a set of characteristics which distinguish a concept and its subtypes from all other concepts.

#### Notes

* Any concept that matches the _sufficient definition_ is equivalent to or a subtype of the defined concept.
* A concept may have more than one _sufficient definition_. In that case any concept that matches at least one of these _sufficient definitions_ is equivalent to or a subtype of the defined concept.

#### Examples

* The following set of assertions is a sufficient definition for [74400008 |appendicitis (disorder)|](http://snomed.info/id/74400008) because any concept for which this set of assertions is true must either be the disorder _appendicitis_ or a subtype of _appendicitis_.

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><a href="http://snomed.info/id/18526009">18526009 |disorder of appendix|</a>  +<br>            <a href="http://snomed.info/id/302168000">302168000 |inflammation of large intestine|</a> :<br>            <a href="http://snomed.info/id/116676008">116676008 |associated morphology|</a>  =  <a href="http://snomed.info/id/23583003">23583003 |inflammation|</a> ,<br>            <a href="http://snomed.info/id/363698007">363698007 |finding site|</a>  =  <a href="http://snomed.info/id/66754008">66754008 |appendix structure|</a>  </p> |

* Both the following sets of assertions are sufficient definitions for the concept [8801005 |Secondary diabetes mellitus (disorder)|](http://snomed.info/id/8801005) :

[73211009 |Diabetes mellitus|](http://snomed.info/id/73211009) : [246075003 |Causative agent|](http://snomed.info/id/246075003) = [105590001 |Substance|](http://snomed.info/id/105590001)

[73211009 |Diabetes mellitus|](http://snomed.info/id/73211009) : [42752001 |Due to|](http://snomed.info/id/42752001) = [64572001 |Disease|](http://snomed.info/id/64572001)

* While each of the assertions [246075003 |Causative agent|](http://snomed.info/id/246075003) = [105590001 |Substance|](http://snomed.info/id/105590001) and [42752001 |Due to|](http://snomed.info/id/42752001) = [64572001 |Disease|](http://snomed.info/id/64572001) form part of a sufficient definition, neither of these assertions are necessary conditions because _only one_ of them needs to be true. This illustrates that an assertion that is part of a sufficient definition need not be a necessary condition.

## Concepts with no Sufficient Definitions

A concept that has no sufficient definitions is a primitive concept.

Because primitive concepts have no sufficient definitions it is not possible for a description logic classifier to determine if other concepts are subtypes of this concept. Similarly, it is not possible to automatically determine whether an expression is a subtype of a primitive concept. Therefore, only concepts or expressions that explicitly state they are subtypes of primitive concepts will be treated as subtypes when applying expression constraints or undertaking analysis.

However, note that this does not prevent a primitive concept being classified as a subtype of a sufficiently defined concept.

## Concepts with a Sufficient Definition

A concept that has at least one sufficient definition is a sufficiently defined concept.

A description logic classifier can determine whether the stated definitions of other concepts meet at least one of the sufficient definitions and if so will classify these concepts as its subtypes. Similarly, it is possible to determine whether an expression is equivalent to or a subtype of a sufficiently defined concept. Therefore, where expression constraints or queries refer to sufficiently defined concepts the results will include the inferred subtypes of these concepts.

## Sufficiently Defined Concepts with Necessary Conditions

If a sufficiently defined concept has one or more additional necessary conditions then any concept or expression that satisfies one of its sufficient definitions will also inherit any necessary conditions.

For example one sufficient definition of [397825006 |Gastric ulcer (disorder)|](http://snomed.info/id/397825006) is an ulcer in a stomach structure:

\=== [64572001 |disease|](http://snomed.info/id/64572001) : { [116676008 |associated morphology|](http://snomed.info/id/116676008) = [56208002 |ulcer|](http://snomed.info/id/56208002) ,\
[363698007 |finding site|](http://snomed.info/id/363698007) = [69695003 |stomach structure|](http://snomed.info/id/69695003) }

However, another definition could be created with a more specific site gastric mucosa:

\=== [64572001 |disease|](http://snomed.info/id/64572001) : { [116676008 |associated morphology|](http://snomed.info/id/116676008) = [56208002 |ulcer|](http://snomed.info/id/56208002) ,\
[363698007 |finding site|](http://snomed.info/id/363698007) = [78653002 |gastric mucosa|](http://snomed.info/id/78653002) }

In both cases these definition are equivalent to [397825006 |Gastric ulcer (disorder)|](http://snomed.info/id/397825006) . The more general definition is flexible when it comes to allowing refinement to a specific location of the ulcer within the stomach, which is actually useful information. It also avoids requiring an expression to refer specifically to the mucosa (stomach lining), which is where all gastric ulcers occur.

For example, an expression including the specific location could look like this

\=== [64572001 |disease|](http://snomed.info/id/64572001) : { [116676008 |associated morphology|](http://snomed.info/id/116676008) = [56208002 |ulcer|](http://snomed.info/id/56208002) ,\
[363698007 |finding site|](http://snomed.info/id/363698007) = [127869006 |Anterior wall of fundus of stomach|](http://snomed.info/id/127869006) }

This satisfies the sufficient definition because the finding site is a subtype of stomach structure. This will therefore classify as a type of [397825006 |Gastric ulcer (disorder)|](http://snomed.info/id/397825006) located in the anterior wall of the gastric fundus. The problem is that a query for disorders of the gastric mucosa will not find this expression. << [64572001 |disease|](http://snomed.info/id/64572001) : [363698007 |finding site|](http://snomed.info/id/363698007) = [78653002 |gastric mucosa|](http://snomed.info/id/78653002) However, adding the definition that refers to the gastric mucosa as an additional necessary condition can solve this problem. The expression satisfies the sufficient definition implying this is a type of [397825006 |Gastric ulcer (disorder)|](http://snomed.info/id/397825006) . The fact that it is a type of gastric ulcer causes it to inherit [363698007 |finding site|](http://snomed.info/id/363698007) = [78653002 |gastric mucosa|](http://snomed.info/id/78653002) so it will now be included in the query for disease in the gastric mucosa.

## A Definition that is Both Necessary and Sufficient

The definition shown in Table D.2-1 provides an example of a simple case.

* The === symbol indicates that the concept definition is equivalent to the concept.
  * This means that each of the assertions in the definition is **necessarily** true for all instance of the concept [710785000 |Laparoscopic repair of hernia|](http://snomed.info/id/710785000) .
  * It also means that this definition is **sufficient** , because if all the assertions are true, this implies this is either the concept or a subtype of the concept.

Table D.2-1: Stated view of the definition of <mark style="color:blue;">|</mark>Laparoscopic repair of hernia<mark style="color:blue;">|</mark>

<table data-header-hidden data-full-width="true"><thead><tr><th width="345.3038330078125"></th><th width="792.8768310546875"></th></tr></thead><tbody><tr><td><strong>Concept</strong></td><td><strong>Stated View of Concept Definition</strong></td></tr><tr><td><a href="http://snomed.info/id/710785000">710785000 | Laparoscopic repair of hernia|</a></td><td>===  <a href="http://snomed.info/id/71388002">71388002 |Procedure|</a>  :<br>            {  <a href="http://snomed.info/id/363700003">363700003 |Direct morphology|</a>  =  <a href="http://snomed.info/id/414402003">414402003 |Hernial opening (morphologic abnormality)|</a> , <br>               <a href="http://snomed.info/id/425391005">425391005 |Using access device|</a>  =  <a href="http://snomed.info/id/86174004">86174004 |Laparoscope, device|</a> , <br>               <a href="http://snomed.info/id/260686004">260686004 |Method|</a>  =  <a href="http://snomed.info/id/257903006">257903006 |Repair - action|</a>  }</td></tr></tbody></table>

<figure><img src="../../images/71172660.png" alt=""><figcaption></figcaption></figure>

## A Definition that is Necessary but Not Sufficient

The definition shown in [Table D.2-2](https://confluence.ihtsdotools.org/display/DOCRELFMT/D.2+Necessary+and+Sufficient+-+Examples#Table-stated-view-primitive) provides an example of another simple case.

* The <<< symbol indicates that the concept is a subtype of the concept definition.
  * This means that each of the assertions in the definition is **necessarily** true for all instance of the concept [173574009 | Acute benign pericarditis (disorder)|](http://snomed.info/id/173574009) .
  * However, this definition is **not sufficient** , because it is represent a more general meaning. Put another way, it does not capture one or more distinguishing features or the [173574009 | Acute benign pericarditis (disorder)|](http://snomed.info/id/173574009) . This means that even if all the assertions are true, it may or may not be this concept or one of its subtypes.

Table D.2-2: Stated view of the definition of |Acute benign pericarditis|

| **Concept**    | **Stated View of Concept Definition** |
| -------------- | ------------------------------------- |
| \[ 173574009   | Acute benign pericarditis (disorder)  |
| \[ 263502005   | Clinical course                       |
| { \[ 116676008 | Associated morphology                 |
| \[ 363698007   | Finding site                          |

<figure><img src="../../images/71172661.png" alt=""><figcaption></figcaption></figure>

## A Definition that is Sufficient with Assertions that are Not Necessarily True

The definition shown in [Table D.2-3](https://confluence.ihtsdotools.org/display/DOCRELFMT/D.2+Necessary+and+Sufficient+-+Examples#Table-stated-view-secondary-dm) provides an example of a more complex case.

* The >>> symbol indicates that the concept definition represents a subtype of the concept.
  * This means that each instance of the definition is **sufficient to represent a** subtype of the concept [8801005 | Secondary diabetes mellitus (disorder)|](http://snomed.info/id/8801005) .
  * The definition does not represent a necessary condition, i.e. the definition is not necessarily true for all instances of the concept [8801005 | Secondary diabetes mellitus (disorder)|](http://snomed.info/id/8801005) . Or, said in other words, not all cases of [8801005 | Secondary diabetes mellitus (disorder)|](http://snomed.info/id/8801005) are caused by a medicinal product or a disease.

Table D.2-3: Possible stated view of the definition of |Secondary diabetes mellitus|

| **Concept**  | **Stated View of Concept Definition**  |
| ------------ | -------------------------------------- |
| \[ 8801005   | Secondary diabetes mellitus (disorder) |
| \[ 246075003 | Causative agent                        |
| OR           |                                        |

> > > [73211009 |Diabetes mellitus|](http://snomed.info/id/73211009) :\
> > > [42752001 |Due to|](http://snomed.info/id/42752001) = [64572001 |Disease|](http://snomed.info/id/64572001)

<figure><img src="../../images/71172659.png" alt=""><figcaption><p>Sufficiently Defined</p></figcaption></figure>

1. A [sufficiently defined concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/sufficiently+defined+concept) is a [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept) with one or more [sufficient definitions](https://confluence.ihtsdotools.org/display/DOCGLOSS/sufficient+definition).

#### Notes

```
 * A [SNOMED CT concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+concept "Glossary link: SNOMED CT concept") is expressed in a human-readable form by its [fully specified name](https://confluence.ihtsdotools.org/display/DOCGLOSS/fully+specified+name "Glossary link: fully specified name") (FSN).
 * A  _sufficiently defined concept_ has at least one [sufficient definition](https://confluence.ihtsdotools.org/display/DOCGLOSS/sufficient+definition "Glossary link: sufficient definition") that distinguishes it from any [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") or [expressions](https://confluence.ihtsdotools.org/display/DOCGLOSS/expression "Glossary link: expressions") that are neither equivalent to, nor subtypes of, the defined concept.
```

**Examples**

```
 * The [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") [ 74400008 | appendicitis (disorder)|](http://snomed.info/id/74400008 "74400008 | appendicitis \(disorder\) |") is  _sufficiently defined_ by the following definition because any [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") for which these defining relationships are true, is either the disorder  _appendicitis_ or a subtype of  _appendicitis_.
```

[74400008 |appendicitis (disorder)|](http://snomed.info/id/74400008)\
\=== [18526009 |disorder of appendix|](http://snomed.info/id/18526009) :\
[116676008 |associated morphology|](http://snomed.info/id/116676008) = [23583003 |inflammation|](http://snomed.info/id/23583003) ,\
[363698007 |finding site|](http://snomed.info/id/363698007) = [66754008 |appendix structure|](http://snomed.info/id/66754008)

```
 * If a concept has a  _sufficient_ definition, it is possible to infer whether another concept or a [postcoordinated expression](https://confluence.ihtsdotools.org/display/DOCGLOSS/postcoordinated+expression "Glossary link: postcoordinated expression") is a [subtype](https://confluence.ihtsdotools.org/display/DOCGLOSS/subtype "Glossary link: subtype") of, or equivalent to, that [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept").  
```

2\. ## Primitive

A [primitive concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/primitive+concept) is a [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept) without a [sufficient definition](https://confluence.ihtsdotools.org/display/DOCGLOSS/sufficient+definition) in the [necessary normal form](https://confluence.ihtsdotools.org/display/DOCGLOSS/necessary+normal+form) distributed in the [relationship](https://confluence.ihtsdotools.org/display/DOCRELFMT/relationship+file).

#### Notes

```
 * The meaning of a [SNOMED CT concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+concept "Glossary link: SNOMED CT concept") is expressed in a human-readable form by its [fully specified name](https://confluence.ihtsdotools.org/display/DOCGLOSS/fully+specified+name "Glossary link: fully specified name"). Each [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") also has a formal [concept definition](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept+definition "Glossary link: concept definition") that provides a computer-processable representation of the meaning of the concept.

 * A  _primitive concept_ has a [concept definition](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept+definition "Glossary link: concept definition") that is not sufficient to computably distinguish it from other [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts").
```

#### Example

```
 * The concept [ 5596004 | atypical appendicitis (disorder)|](http://snomed.info/id/5596004 "5596004 | atypical appendicitis \(disorder\) |") is  _primitive_ because the following definition is not sufficient to distinguish _atypical appendicitis_ from any other type of _appendicitis:_
```

[5596004 |atypical appendicitis (disorder)|](http://snomed.info/id/5596004)\
<<< [116680003 |is a|](http://snomed.info/id/116680003) = [74400008 |appendicitis|](http://snomed.info/id/74400008)\
[116676008 |associated morphology|](http://snomed.info/id/116676008) = [23583003 |inflammation|](http://snomed.info/id/23583003)\
[363698007 |finding site|](http://snomed.info/id/363698007) = [66754008 |appendix structure|](http://snomed.info/id/66754008)

## Necessary Conditions

All SNOMED CT defining relationships currently released are necessarily (always) true for the concept defined. Relationships that are necessarily true are also know as necessary conditions.

A [necessary condition](https://confluence.ihtsdotools.org/display/DOCGLOSS/necessary+condition) is defined as a characteristic that is always true of a [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept).

#### Example

* If you have a [71620000 | fracture of femur|](http://snomed.info/id/71620000) , the morphological abnormality [72704001 | fracture|](http://snomed.info/id/72704001) must be present. Therefore, [116676008 | morphology|](http://snomed.info/id/116676008) = [72704001 | fracture|](http://snomed.info/id/72704001) is a _necessary condition_ of [71620000 | fracture of femur|](http://snomed.info/id/71620000) .

## Sufficient Sets of Conditions

In practice there can be several sufficient definitions for a concept. That is to say several different ways in which a concept could be sufficiently defined by different sets of [defining relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/defining+relationship) For example:

Gastric ulcer is defined as follows:

[397825006 |gastric ulcer|](http://snomed.info/id/397825006)\
\=== [116680003 |is a|](http://snomed.info/id/116680003) = [64572001 |disease|](http://snomed.info/id/64572001)\
{ [116676008 |associated morphology|](http://snomed.info/id/116676008) = [56208002 |ulcer|](http://snomed.info/id/56208002) ,\
[363698007 |finding site|](http://snomed.info/id/363698007) = [69695003 |stomach structure|](http://snomed.info/id/69695003) }

This is a _sufficient_ definition because any [56208002 | ulcer|](http://snomed.info/id/56208002) in a [69695003 | stomach structure|](http://snomed.info/id/69695003) is by definition a [397825006 | gastric ulcer|](http://snomed.info/id/397825006) . Based on this definition:

Any [postcoordinated expression](https://confluence.ihtsdotools.org/display/DOCGLOSS/postcoordinated+expression) that specified a disease involving an [56208002 | ulcer|](http://snomed.info/id/56208002) with [363698007 | finding site|](http://snomed.info/id/363698007) [69695003 | stomach structure|](http://snomed.info/id/69695003) would be equivalent to or a [subtype](https://confluence.ihtsdotools.org/display/DOCGLOSS/subtype) of [397825006 | gastric ulcer|](http://snomed.info/id/397825006)

However, a [query](https://confluence.ihtsdotools.org/display/WIPRELFMT/query+\(field\)) for all disorders involving [78653002 | gastric mucosa|](http://snomed.info/id/78653002) would incorrectly exclude [397825006 | gastric ulcer|](http://snomed.info/id/397825006) as the site is specified as [78653002 | gastric mucosa|](http://snomed.info/id/78653002) which is more specific than [69695003 | stomach structure|](http://snomed.info/id/69695003) . In reality there is another sufficient set defining relationships

[397825006 |gastric ulcer|](http://snomed.info/id/397825006)\
\=== [116680003 |is a|](http://snomed.info/id/116680003) = [64572001 |disease|](http://snomed.info/id/64572001)\
{ [116676008 |associated morphology|](http://snomed.info/id/116676008) = [56208002 |ulcer|](http://snomed.info/id/56208002) ,\
[363698007 |finding site|](http://snomed.info/id/363698007) = [78653002 |gastric mucosa|](http://snomed.info/id/78653002) }

but this is not currently represented in SNOMED CT. The reason for this is that currently the profile of description logic used by SNOMED CT does not support representation of multiple sufficient sets.

When multiple sufficient sets are supported, satisfying a single sufficient set enables an inference to be made that all necessary conditions must also be true. For example

* The definition [363698007 | finding site|](http://snomed.info/id/363698007) = [78653002 | gastric mucosa|](http://snomed.info/id/78653002) is a _necessary_ condition for [397825006 | gastric ulcer|](http://snomed.info/id/397825006) :
  * This is true because all gastric ulcers necessarily involve the [78653002 | gastric mucosa|](http://snomed.info/id/78653002)
* The definition [116676008 | morphology|](http://snomed.info/id/116676008) = [56208002 | ulcer|](http://snomed.info/id/56208002) and [363698007 | finding site|](http://snomed.info/id/363698007) = [69695003 | stomach structure|](http://snomed.info/id/69695003) is a _sufficient_ definition for [397825006 | gastric ulcer|](http://snomed.info/id/397825006) :
  * This is true because any ulcer in a stomach structure is a [397825006 | gastric ulcer|](http://snomed.info/id/397825006)
* Therefore, an assertion that a person has an [56208002 | ulcer|](http://snomed.info/id/56208002) with [363698007 | finding site|](http://snomed.info/id/363698007) [69695003 | stomach|](http://snomed.info/id/69695003) is _sufficient_ to imply that they have a [397825006 | gastric ulcer|](http://snomed.info/id/397825006) :
  * Since a gastric ulcer _necessarily_ involves the [78653002 | gastric mucosa|](http://snomed.info/id/78653002) it should be possible to deduce that a person with an "ulcer" with finding site [69695003 | stomach|](http://snomed.info/id/69695003) has a disorder of with a site [78653002 | gastric mucosa|](http://snomed.info/id/78653002)

However, as the current profile does not enable recognition of multiple sufficient sets, the general rule is to represent the most general sufficient set as this gives the greatest coverage for subsumption testing. This approach is taken because including more defining relationships, without distinguishing them from the sufficient set means some logically equivalent expressions will not compute as equivalent to or subsumed by the defined concept. This occurs in any cases where the expression does not include one of the attributes in the definition - even if it was not part of the logically sufficient set.
