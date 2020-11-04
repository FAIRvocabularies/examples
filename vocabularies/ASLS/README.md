# Australian Soil and Landscape Survey vocabularies

http://anzsoil.org/def/au/asls/soil-profile/field-texture-CS 

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

http://anzsoil.org/def/au/asls/soil-profile/field-texture-mineral
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