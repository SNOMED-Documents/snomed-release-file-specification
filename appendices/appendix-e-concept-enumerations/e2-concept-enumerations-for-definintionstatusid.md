# E.2 Concept Enumerations for definintionStatusId

This concept enumeration represents a value that can be applied to the concept.definitionStatusId field. This is used to indicate whether the current set of relationships applied to a _concept_ are sufficient to define it relative to its supertypes. The Table below shows the current set of values for this concept enumeration.

**Definition status (core metadata concept) (900000000000444006)**

<table data-header-hidden data-full-width="true"><thead><tr><th width="228.255126953125"></th><th></th></tr></thead><tbody><tr><td><strong>Concept</strong></td><td><strong>Comment</strong></td></tr><tr><td><a href="http://snomed.info/id/900000000000073002">900000000000073002 |Sufficiently defined by necessary conditions definition status|</a></td><td><p>The set of defining relationships applied to the concept are asserted to fully define the concept.</p><p>Any concept or expression for which all these defining <em>relationships</em> are true is either equivalent to or subsumed by this concept.</p><p>Any concept or expression for which any of these defining <em>relationships</em> is not true is neither equivalent to nor subsumed by this concept.</p></td></tr><tr><td><a href="http://snomed.info/id/900000000000074008">900000000000074008 |Not sufficiently defined by necessary conditions definition status|</a></td><td><p>The set of defining relationships applied to the concept are asserted to be incompletely define the concept. The concept is currently considered to be primitive.</p><p>A concept or expression for which all these defining <em>relationships</em> are true <strong>may</strong> be equivalent to or subsumed by this concept. However, it is not possible to compute this from the definition - because the missing element in the definition may or may not apply to the other concept or expression.</p><p>Any concept or expression for which any of these defining <em>relationships</em> is not true is neither equivalent to nor subsumed by this concept.</p></td></tr></tbody></table>

***






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Release+File+Specification&entry.670899847=E.2%20Concept%20Enumerations%20for%20definintionStatusId" class="button primary">Provide Feedback</a>
