# id (field)

A field that provides the unique identifier of a [component](https://confluence.ihtsdotools.org/display/DOCGLOSS/component) ( [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept), [description](https://confluence.ihtsdotools.org/display/DOCGLOSS/description) or [relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship)) or [reference set member](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set+member) .

Note:

* The data type of the _id_ for a [component](https://confluence.ihtsdotools.org/display/DOCGLOSS/component) is [SCTID](https://confluence.ihtsdotools.org/display/DOCGLOSS/SCTID) and this identifier is used to refer to the [component](https://confluence.ihtsdotools.org/display/DOCGLOSS/component) .
* The data type of the _id_ for a [reference set member](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set+member) is [UUID](https://confluence.ihtsdotools.org/display/DOCGLOSS/UUID). This identifier is only used to support versioning of a rows ( [member](https://confluence.ihtsdotools.org/display/DOCGLOSS/member)) in a [Reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/Reference+set) it does not identify the Reference set itself (see [refsetId](https://confluence.ihtsdotools.org/display/DOCGLOSS/refsetId)) nor does it identify to a component refered to by the [Reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/Reference+set) (see [referencedComponentId](https://confluence.ihtsdotools.org/display/DOCGLOSS/referencedComponentId) ).
