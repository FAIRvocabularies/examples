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