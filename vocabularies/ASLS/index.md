---
permalink: /vocabularies/ASLS/
layout: default
title: Australian Soil and Landscape Survey vocabularies
---

# Australian Soil and Landscape Survey vocabularies

## Governance - who is the content-custodian

**Rule 1.** Determine the governance arrangements and custodian of the legacy vocabulary

The definitions in the [Australian soil and land survey field handbook (3rd edn)](https://www.publish.csiro.au/book/5230/) are organized in six chapters, each relating to a specific theme, such as Landform or Soil Profile. While the handbook is credited to the [National Committee on Soil and Terrain](https://www.directory.gov.au/portfolios/agriculture-and-water-resources/department-agriculture-and-water-resources/national-committee-soil-and-terrain), each chapter has separate authors. These authors were subject-matter experts who arranged the terms and definitions , acting as the content custodians for a theme. 

## Permission for re-purposing

**Rule 2.** Verify that the legacy-vocabulary license allows repurposing, and agree on the license for the FAIR vocabulary

The [Australian soil and land survey field handbook (3rd edn)](https://www.publish.csiro.au/book/5230/) includes definitions of a range of aspects of environmental land surveys. The print and ebook includes a conventional copyright statement containing the phrase ‘All rights reserved’ to [CSIRO Publishing: Melbourne](https://www.publish.csiro.au/). Prior to re-purposing the terms and definitions in FAIR vocabularies we contacted CSIRO Publishing to discuss our plans. After explaining the process and intentions, noting that publication as a FAIR vocabulary would allow better access and linkages between datasets and definitions, the publisher granted a specific permission to undertake the proposed re-purposing. 

## Maintenance environment

**Rule 4.** Establish a technical maintenance environment for the FAIR vocabulary artefacts

All of the technical artefacts, including the RDF-encoded content (as TTL files) are maintained in a [Bitbucket repository](https://bitbucket.csiro.au/projects/EIS/repos/australian-soil-vocabularies/browse/asls). 

The content is published in [CSIRO's Linked Data Registry](http://registry.it.csiro.au/def/soil/au/asls) which allows for continuous fine-grained update, with full version tracking.  

## Persistent unique identifiers

**Rule 5.** Assign a unique identifier to (a) the vocabulary and (b) each term in the vocabulary

Terms from the ASLS are denoted by URIs beginning [http://anzsoil.org/def/au/asls/](http://anzsoil.org/def/au/asls). 

Each chapter is denoted by a child URI
- Landform terms in [http://anzsoil.org/def/au/asls/landform](http://anzsoil.org/def/au/asls/landform)
- Soil profile terms in [http://anzsoil.org/def/au/asls/soil-prof](http://anzsoil.org/def/au/asls/soil-prof)

Collections and individual terms are further childern, e.g. 
- Collection of observable properties of soil-horizons [http://anzsoil.org/def/au/asls/soil-profile/observable-properties](http://anzsoil.org/def/au/asls/soil-profile/observable-properties)
- Individual observable property [http://anzsoil.org/def/au/asls/soil-profile/condition-of-surface-soil-when-dry](http://anzsoil.org/def/au/asls/soil-profile/condition-of-surface-soil-when-dry)
- Individual field-texture classification [http://anzsoil.org/def/au/asls/soil-profile/field-texture-LMC](http://anzsoil.org/def/au/asls/soil-profile/field-texture-LMC)

Note that the URI scheme for this vocabulary reflects the first-order arrangement of the source material (chapters in a book) as the path. 

Note that identifiers are non-opaque - the elements of the URI are based on the labels of the collections and concepts. 

## Term encoding

**Rule 6.** Create machine readable representations of the vocabulary terms 
 
### Landform vocabulary

Each item in this vocabulary is encoded as a `skos:Concept`. 

```turtle
<http://anzsoil.org/def/au/asls/landform/morphological-type-H>
  a skos:Concept ;
  dcterms:description "compound landform element comprising a narrow crest and short adjoining slopes, the crest length being less than the width of the landform element."@en ;
  dcterms:identifier "http://anzsoil.org/def/au/asls/landform/morphological-type-H"^^xsd:anyURI ;
  rdfs:label "Hillock"@en ;
  skos:definition "compound landform element comprising a narrow crest and short adjoining slopes, the crest length being less than the width of the landform element."@en ;
  skos:inScheme asls:landform ;
  skos:notation "H" ;
  skos:prefLabel "Hillock"@en ;
.
```

```turtle
<http://anzsoil.org/def/au/asls/landform/compound-morphological-types>
  a skos:Collection ;
  dcterms:description "Several types of landform feature have crests and adjoining slopes that are so small that a 20 m radius site would usually include both. Two compound morphological types are distinguished by the relative length of the crest: Hillock and Ridge"@en ;
  dcterms:identifier "http://anzsoil.org/def/au/asls/landform/compound-morphological-types"^^xsd:anyURI ;
  rdfs:label "Compound morphological types"@en ;
  skos:definition "Several types of landform feature have crests and adjoining slopes that are so small that a 20 m radius site would usually include both. Two compound morphological types are distinguished by the relative length of the crest: Hillock and Ridge"@en ;
  skos:member <http://anzsoil.org/def/au/asls/landform/morphological-type-H> ;
  skos:member <http://anzsoil.org/def/au/asls/landform/morphological-type-R> ;
  skos:prefLabel "Compound morphological types"@en ;
.
```

### Soil profile vocabulary

Each item in this vocabulary is encoded as a `skos:Concept`. 

```turtle
<http://anzsoil.org/def/au/asls/soil-profile/field-texture-CS>
  a                skos:Concept ;
  rdfs:comment     "Approximate clay content (%): 5 - 10%"@en ;
  rdfs:label       "Clayey sand"@en ;
  dct:description  "Behaviour of moist bolus: slight coherence; sand grains of medium size; sticky when wet; many sand grains stick to fingers; will form minimal ribbon of 5–15 mm; discolours fingers with clay stain."@en ;
  dct:identifier   "http://anzsoil.org/def/au/asls/soil-profile/field-texture-CS"^^xsd:anyURI ;
  skos:definition  "Behaviour of moist bolus: slight coherence; sand grains of medium size; sticky when wet; many sand grains stick to fingers; will form minimal ribbon of 5–15 mm; discolours fingers with clay stain."@en ;
  skos:inScheme <http://anzsoil.org/def/au/asls/soil-profile> ;
  skos:narrower    <http://anzsoil.org/def/au/asls/soil-profile/field-texture-CKS> , <http://anzsoil.org/def/au/asls/soil-profile/field-texture-CS-light> , <http://anzsoil.org/def/au/asls/soil-profile/field-texture-CFS> , <http://anzsoil.org/def/au/asls/soil-profile/field-texture-CS-heavy> ;
  skos:notation    "CS" ;
  skos:prefLabel   "Clayey sand"@en ;
.
```

```turtle 
<http://anzsoil.org/def/au/asls/soil-profile/field-texture-mineral>
  a skos:Collection ;
  a sosa:ObservableProperty ;
  dct:description """<p><img src=\"http://anzsoil.org/resources/yellowbook/Figure16.png\" /></p> 
<p> Figure 16 Triangular texture diagram based on International fractions (Marshall 1947). </p>"""^^rdf:HTML ;
  dct:identifier "http://anzsoil.org/def/au/asls/soil-profile/field-texture-mineral"^^xsd:anyURI ;
  ui:isMemberOf <http://anzsoil.org/def/au/asls/soil-profile/field-textures> ;
  rdfs:label "Mineral soils field texture grade"@en ;
  skos:definition """The following description of determination of field texture is adapted from Northcote (1979).
Field texture is a measure of the behaviour of a small handful of soil when moistened and kneaded into a ball and then pressed out between thumb and forefinger.
Take a sample of soil sufficient to fit comfortably into the palm of the hand. Moisten the soil with water, a little at a time, and knead until the ball of soil, so formed, just fails to stick to the fingers. Add more soil or water to attain this condition, known as the sticky point, which approximates field capacity for that soil. Continue kneading and moistening until there is no apparent change in the soil ball, usually a working time of 1–2 minutes. The soil ball, or bolus, is now ready for shearing manipulation, but the behaviour of the soil during bolus formation is also indicative of its field texture. The behaviour of the bolus and of the ribbon produced by shearing (pressing out) between thumb and forefinger characterises the field texture. Do not assess field texture grade solely on the length of ribbon.
The recommended field texture grades as characterised by the behaviour of the moist bolus are described. The approximate percentage content of clay (particles less than 0.002 mm in diameter) and silt (particles between 0.02 and 0.002 mm in diameter) are given as a guide. These percentages must not be used to determine a field texture, that is, do not use them to convert a laboratory particle size value to a field texture grade. Similarly, do not adjust a field texture grade when laboratory particle size data become available.""" ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-CL> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-CLS> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-CS> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-HC> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-L> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-LC> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-LMC> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-LS> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-MC> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-MHC> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-S> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-SCL> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-SL> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-ZCL> ;
  skos:member <http://anzsoil.org/def/au/asls/soil-profile/field-texture-ZL> ;
  skos:prefLabel "Mineral soils field texture grade"@en ;
.
```

## Vocabulary metadata

**Rule 7.** Add vocabulary metadata

### Landform vocabulary

```turtle
<http://anzsoil.org/def/au/asls/landform>
  a skos:ConceptScheme ;
  dcterms:contributor <https://orcid.org/0000-0002-0693-1899> ;
  dcterms:contributor <https://orcid.org/0000-0002-3884-3420> ;
  dcterms:created "2018-01-16"^^xsd:date ;
  dcterms:creator <mailto:asris@csiro.au> ;
  dcterms:description """<p>This register contains a machine-readable representation of the classifiers described in chapter 5 <i>Landform</i>, by J.G. Speight, in <a href='https://www.publish.csiro.au/book/5230'>Australian soil and land survey field handbook (3rd edn)</a>.</p>
<p>In this technique for describing landforms, the whole land surface is viewed as a mosaic of tiles of odd shapes and sizes. The scheme is intended to produce a record of observations rather than inferences.</p>
<p>The data was converted from the print representation to this linked-data form by <a href='https://orcid.org/0000-0002-0693-1899'>Linda Gregory</a> assisted by <a href='https://orcid.org/0000-0002-3884-3420'>Simon J D Cox</a>."""^^rdf:HTML ;
  dcterms:isFormatOf "<p>Chapter 5 <i>Landform</i>, by J.G. Speight, in <a href='https://www.publish.csiro.au/book/5230'>Australian soil and land survey field handbook (3rd edn)</a></p>"^^rdf:HTML ;
  dcterms:license <http://creativecommons.org/licences/by/4.0> ;
  dcterms:modified "2020-09-16"^^xsd:date ;
  dcterms:publisher <http://www.publish.csiro.au/> ;
  dcterms:rights "copyright CSIRO 2009, 2020. All rights reserved." ;
  dcterms:source "National Committee on Soil and Terrain (2009), 'Australian soil and land survey field handbook (3rd edn).' (CSIRO Publishing: Melbourne)" ;
  rdfs:label "Landform classifiers"@en ;
  rdfs:seeAlso <http://www.publish.csiro.au/nid/22/pid/5230.htm> ;
  skos:changeNote "2020-09-16 - made asls:landform a skos:ConceptScheme and added skos:inScheme link from all concepts" ;
.
```

### Soil profile vocabulary

```turtle
<http://anzsoil.org/def/au/asls/soil-profile>
  a skos:ConceptScheme ;
  dct:contributor <https://orcid.org/0000-0002-0693-1899> ;
  dct:contributor <https://orcid.org/0000-0002-3884-3420> ;
  dct:created "2017-10-26"^^xsd:date ;
  dct:creator <mailto:asris@csiro.au> ;
  dct:description """<p>This register contains a machine-readable representation of the classifiers described in chapter 8 <i>Soil Profile</i>, by R.C. McDonald and R.F. Isbell, in <a href='https://www.publish.csiro.au/book/5230'>Australian soil and land survey field handbook (3rd edn)</a>.</p>
<p>A soil profile is a vertical section of a soil from the soil surface through all its horizons to parent material, other consolidated substrate material or selected depth in unconsolidated material.</p>
<p>The data was converted from the print representation to this linked-data form by <a href='https://orcid.org/0000-0002-0693-1899'>Linda Gregory</a> assisted by <a href='https://orcid.org/0000-0002-3884-3420'>Simon J D Cox</a>.</p>"""^^rdf:HTML ;
  dct:isFormatOf "<p>Chapter 8 <i>Soil Profile</i>, by R.C. McDonald and R.F. Isbell, in <a href='https://www.publish.csiro.au/book/5230'>Australian soil and land survey field handbook (3rd edn)</a></p>"^^rdf:HTML ;
  dct:license <http://creativecommons.org/licences/by/4.0> ;
  dct:modified "2020-09-16"^^xsd:date ;
  dct:publisher <http://www.publish.csiro.au/> ;
  dct:rights "copyright CSIRO 2009, 2016, 2018. All rights reserved."@en ;
  dct:source "National Committee on Soil and Terrain (2009), 'Australian soil and land survey field handbook (3rd edn).' (CSIRO Publishing: Melbourne)"@en ;
  rdfs:label "Soil Profile classifiers"@en ;
  rdfs:seeAlso <http://www.publish.csiro.au/nid/22/pid/5230.htm> ;
  skos:changeNote "2020-09-16 - Added skos:inScheme and skos:topConceptOf links to asls:soil-profile; removed redundant owl:sameAs links" ;
.
```

## Vocabulary registration

**Rule 8.** Register the vocabulary

The FAIR ASLS vocabularies are registered in 
- Research Vocabularies Australia
  - [Soil Profile](https://vocabs.ardc.edu.au/viewById/313)
  - [Landform](https://vocabs.ardc.edu.au/viewById/314)
  - [Land surface](https://vocabs.ardc.edu.au/viewById/315)
 - Bioportal
  - [Soil Profile](https://fairsharing.org/bsg-s001603/)
  - [Landform](https://fairsharing.org/bsg-s001604/)
  - [Land surface](https://fairsharing.org/bsg-s001605/)
 - FAIRsharing
  - [Soil Profile](https://bioportal.bioontology.org/ontologies/SOIL-PROF)
  - [Landform](https://bioportal.bioontology.org/ontologies/LANDFORM)
  - [Land surface](https://bioportal.bioontology.org/ontologies/LAND-SURFACE)


## Vocabulary access

**Rule 9.** Make the vocabulary accessible for humans and machines 

The FAIR ASLS vocabularies are published on the 
- CSIRO Linked Data Registry
  - [Soil Profile](http://registry.it.csiro.au/def/soil/au/asls/soil-prof)
  - [Landform](http://registry.it.csiro.au/def/soil/au/asls/landform)
  - [Land surface](http://registry.it.csiro.au/sandbox/soil/asls/land-surface)
- Research Vocabularies Australia
  - [Soil Profile](https://vocabs.ardc.edu.au/viewById/313)
  - [Landform](https://vocabs.ardc.edu.au/viewById/314)
  - [Land surface](https://vocabs.ardc.edu.au/viewById/315)


