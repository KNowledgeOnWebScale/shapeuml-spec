# Constraints

First, we provide a mapping from semantic constructs of RDF constraint languages
to visual elements of ShapeUML (see figures).
Next, we explain splitting rules with respect to the visualization of property shapes.
Finally, we provide a complete visual example.

## Semantic constructs

The SHACL specification [[SHACL]] contains core constraints and other concepts relevant for data validation.
We provide a mapping of semantic constructs to visual representations with ShapeUML,
i.e. in the first figure we provide the mapping from SHACL core constraints
and in the second figure we provide the mapping from other relevant SHACL concepts.

<figure id="semantic-constructs"> 
  <img src="./resources/images/2020-journal-mapping-shapeuml-core-constraints-summary.svg" style="height:100%;width:100%" />
  <figcaption>
    Semantic constructs of SHACL core constraints
    and their visual representation in ShapeUML.
  </figcaption>
</figure>

<figure id="semantic-constructs"> 
  <img src="./resources/images/2020-journal-mapping-shapeuml-other-concepts-summary.svg" style="height:100%;width:100%" />
  <figcaption>
    Semantic constructs of validation-related SHACL concepts
    and their visual representation in ShapeUML.
  </figcaption>
</figure>
 
 
## Splitting rules

Node shapes can be reused by a directed dashed connectioni and property shapes can be reused by directed solid connections.
Property shapes are visualized only once, however, ingoing solid connections with a property path as label and cardinalities on the arrow head are splitted.
I.e. a property shape which is reused <code>n</code> times will be visualized only once
but will have <code>n</code> ingoing solid edges with the property path as label
and cardinalities on the arrow head.

## Example

Below you can find an example for constraints expressed with ShapeUML.

<figure id="example-shapeuml"> 
  <img src="./resources/images/example-shapeuml.svg" style="height:100%;width:100%" />
  <figcaption>
    Constraints visualized using ShapeUML: A subject valid to the Person data shape should have an IRI (1),
    at least one but maximum two <code>ex:address</code> properties (2) of class <code>schema:PostalAddress</code> (3)
    and the object of at least one <code>ex:address</code> property should comply with the existing data shape <code>ex:validAddress</code> (4).
    Additionally, the subject valid to person should either have exactly one <code>ex:fullName</code> or at least one <code>schema:givenName</code> (5)
    and at least one <code>schema:familyName</code> all of datatype <code>xsd:string</code>.
	The value of <code>ex:fullName</code> must not comply with the data shape <code>ex:organizationShape</code> (6).
	Addresses must only have values for the property <code>postalAddress</code> with an exception for <code>rdf:type</code> (7).
	Constraints of the <code>ex:organizationShape</code> are not considered for validation (8). 
  </figcaption>
</figure>

