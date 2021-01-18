## Terminology

Throughout the document, the following terminology is used.

### General

<dl>
  <dt><dfn id="dfn-entity">(anonymous) entity</dfn></dt>
  <dd>
    An entity is something that exists as a distinct, independent, or self-contained unit.
    Examples are people, companies, buildings and so on.
    If you want to uniquely address an entity then it needs to have a unique name.
    Therefore, entities use HTTP URIs.
    However, when a entity does not have a URI we call it an <span class="emph">anonymous</span> entity [[MapVOWL]].
  </dd>
  
  <dt><dfn id="dfn-attribute">attribute</dfn></dt>
  <dd>
    More information is provided about an entity by adding attribute to it.
    Examples are the name of a person, the VAT number of a company and so on [[MapVOWL]].
  </dd>
  
  <dt><dfn id="dfn-relationship">relationship</dfn></dt>
  <dd>
    An entity and its attributes are connected with each other using relationships.
    A relationship describes how a attribute relates to its entity [[MapVOWL]].
  </dd>
  
  <dt><dfn id="dfn-constraints">constraints</dfn></dt>
  <dd>
    A constraint is a condition on data which should be satisfied. Several types of constraints exist,
    e.g. a datatype constraint on a property restricts the value of that property to be of a specific datatype
    and a cardinality constraint on a property restricts the number of that property [[SHACL-core-constraints]].
  </dd>
  
  <dt><dfn id="dfn-data-shape">data shape</dfn></dt>
  <dd>
    A data shape is a set of conditions on RDF data [[SHACL-abstract]].
    It provides context for constraints, i.e. a datatype constraint can be used
    in different data shapes which corresponds to different contexts.
  </dd>
  
  <dt><dfn id="dfn-node-shape">node shape</dfn></dt>
  <dd>
    A node shape is a specific data shape which represents conditions on nodes,
    i.e. subjects and objects of triples [[SHACL]].
  </dd>
  
  <dt><dfn id="dfn-property-shape">property shape</dfn></dt>
  <dd>
    A property shape is a specific data shape which represents conditions on properties and their values,
    i.e. predicates and related objects of triples [[SHACL]].
  </dd>
  
  <dt><dfn id="dfn-closed-data-shape">closed data shape</dfn></dt>
  <dd>
    A closed data shape may only have values for the properties explicitly enumerated via property shapes [[SHACL]].
  </dd>
  
  <dt><dfn id="dfn-severity">severity</dfn></dt>
  <dd>
    Each data shape has a severity which qualifies the violation of the stated conditions, i.e. it categorizes validation results [[SHACL]].
    By default a data shape has the severity "violation" but other severities can be defined,
    i.e. the SHACL core specifies the three severities "violation", "warning" and "information".
  </dd>
  
</dl>

### Visualization

<dl>
            
  <dt><dfn id="dfn-node">node</dfn></dt>
  <dd>
    A node is a visual representation of either an entity or an attribute [[MapVOWL]].
  </dd>
  
  <dt><dfn id="dfn-edge">edge</dfn></dt>
  <dd>
    An edge is a line connecting two nodes.
    It represents the relationship between two entities or one entity and one attribute [[MapVOWL]].
  </dd>
 
  <dt><dfn id="dfn-graph">graph</dfn></dt>
  <dd>
    A graph is a collection of nodes and edges [[MapVOWL]].
  </dd>

</dl>

