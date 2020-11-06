# Geological Timescale
## Permission for re-purposing

  - **Rule 1. Verify that the source license allows repurposing**

The basic temporal-topology of the Geologic Timescale is standard knowledge in the geology community. 

The more specialized aspects of the information in the vocabulary relate to the 'stratotypes' for the boundaries in the timescale - i.e. (i) the location of the type-section that has been agreed to best represent the interval spanning the boundary, and the position within the section that corresponds with the actual boundary, and (ii) the best estimate of the age of samples of rock taken from the boundary point, which calibrates the age of the boundary. All these details are published on a per-boundary basis in the scientific literature, so can be transcribed from there. The standard information for each boundary, that is used by the [International Commission on Stratigraphy](https://stratigraphy.org/) to officially assign dates to the timescale are summarized in the [tabulation of Global Boundary Stratotype Section and Points](https://stratigraphy.org/gssps/). 

However, starting in 2020, the [International Commission on Stratigraphy](https://stratigraphy.org/) has agreed to used the FAIR vocabulary as the point-of-truth, all the resources on their website (the table of GSSPs, and the coloured chart) will be generated from the semantic resources.  

## Governance - who is the content-custodian

  - **Rule 2. Determine the governance arrangements and custodian responsible for the legacy vocabulary**

Global Boundary Stratotype Section and Points are officially ratified by the [International Commission on Stratigraphy](https://stratigraphy.org/).  


## Term encoding

  - **Rule 6. Create a semantic-standards based vocabulary - address Interoperability** 

Maintained in https://github.com/CGI-IUGS/timescale-data 

Namespaces: 
```turtle
@prefix dct: <http://purl.org/dc/terms/> .
@prefix geo: <http://www.opengis.net/ont/geosparql#> .
@prefix gts: <http://resource.geosciml.org/ontology/timescale/gts#> .
@prefix isc: <http://resource.geosciml.org/classifier/ics/ischart/> .
@prefix iso-trs: <http://def.isotc211.org/iso19108/2006/TemporalReferenceSystem#> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix rank: <http://resource.geosciml.org/ontology/timescale/rank/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix sf: <http://www.opengis.net/ont/sf#> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix thors: <http://resource.geosciml.org/ontology/timescale/thors#> .
@prefix time: <http://www.w3.org/2006/time#> .
@prefix ts: <http://resource.geosciml.org/vocabulary/timescale/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
```

Some individual members from https://github.com/CGI-IUGS/timescale-data/blob/master/rdf/isc2020.ttl

```turtle
isc:Phanerozoic
#
# SKOS representation at the top
#
  a skos:Concept ;
  rdfs:comment "older bound -541.0 +|-1.0 Ma"@en ;
  rdfs:comment "younger bound -0.0 Ma"@en ;
  rdfs:label "Phanerozoic Eon"@en ;
  skos:inScheme ts:gts2020 ;
  skos:narrower isc:Cenozoic ;
  skos:narrower isc:Mesozoic ;
  skos:narrower isc:Paleozoic ;
  skos:notation "a1.1"^^gts:EraCode ;
  skos:prefLabel "Fanerosoikum"@et ;
  skos:prefLabel "Fanerotsoikum"@fi ;
  skos:prefLabel "Phanerozoic"@en ;
  skos:prefLabel "Phanerozoikum"@de ;
  skos:prefLabel "Phanerozoisk"@da ;
  skos:prefLabel "Фанерозой"@bg ;
  skos:prefLabel "显生宙"@zh ;
  skos:prefLabel "顕生代"@ja ;
  skos:topConceptOf ts:gts2020 ;
#
# domain specific elements below here
#
  a gts:Eon ;
  a gts:GeochronologicEra ;
  a time:ProperInterval ;
  gts:rank rank:Eon ;
  time:hasBeginning isc:BasePhanerozoic ;
  time:hasEnd isc:Present ;
  time:intervalContains isc:Mesozoic ;
  time:intervalFinishedBy isc:Cenozoic ;
  time:intervalMetBy isc:Ediacaran ;
  time:intervalMetBy isc:Neoproterozoic ;
  time:intervalMetBy isc:Precambrian ;
  time:intervalMetBy isc:Proterozoic ;
  time:intervalStartedBy isc:Paleozoic ;
.
```

```turtle
isc:BasePhanerozoic
#
# SKOS representation at the top
#
  a skos:Concept ;
  rdfs:label "Base of Phanerozoic"@en ;
  skos:altLabel "Base of Cambrian"@en ;
  skos:altLabel "Base of Fortunian"@en ;
  skos:altLabel "Base of Paleozoic"@en ;
  skos:altLabel "Base of Terreneuvian"@en ;
  skos:inScheme ts:gts2020 ;
  skos:prefLabel "Base of Phanerozoic"@en ;
#
# domain specific elements below here
#
  a gts:GeochronologicBoundary ;
  a thors:EraBoundary ;
  a time:Instant ;
  gts:stratotype isc:BasePhanerozoicSP ;
  time:inTemporalPosition isc:BasePhanerozoicTime ;
.
```

```turtle
isc:BasePhanerozoicSP
#
# SKOS representation at the top
#
  a skos:Concept ;
  dct:source "Episodes 17/1 2, p. 95 100, 1994"@en ;
  rdfs:comment "Fortune Head, SE Newfoundland, Canada"@en ;
  rdfs:label "Stratotype Point Base of Fortunian"@en ;
  rdfs:seeAlso <http://www.stratigraphy.org/GSSP/Fortunian.pdf> ;
  rdfs:seeAlso <http://www.stratigraphy.org/GSSP/index.html> ;
  rdfs:seeAlso <https://timescalefoundation.org/gssp/image.php?periodid=156&top_parentid=0&imageid=341> ;
  skos:altLabel "Stratotype Point Base of Cambrian"@en ;
  skos:altLabel "Stratotype Point Base of Paleozoic"@en ;
  skos:altLabel "Stratotype Point Base of Phanerozoic"@en ;
  skos:altLabel "Stratotype Point Base of Terrenuvian"@en ;
  skos:prefLabel "Stratotype Point Base of Fortunian"@en ;
#
# domain specific elements below here
#
  a gts:StratigraphicPoint ;
  gts:boundaryLevel "2.4m above the Base of Member 2 in the Chapel Island Formation"@en ;
  gts:correlationEvent "Trace fossil FAD Trichophycus pedum"@en ;
  gts:ratifiedGSSP true ;
  gts:representsBoundary isc:BasePhanerozoic ;
  gts:status "Ratified 1992"@en ;
  geo:hasGeometry isc:BasePhanerozoic-location ;
.
```

```turtle
isc:BasePhanerozoicTime
#
# domain specific elements below here
#
  a time:TimePosition ;
  gts:positionalUncertainty isc:BasePhanerozoicUncertainty ;
  time:hasTRS <http://resource.geosciml.org/classifier/cgi/geologicage/ma> ;
  time:numericPosition 541.0 ;
.
```

## Vocabulary resource with metadata

  - **Rule 7. Add rich metadata - address vocabulary Reusability** 

```turtle
ts:gts2020
  a skos:ConceptScheme ;
  dct:contributor "Chinese and Japanese preferred labels from SKOS by Xiaogang Ma, adopted from Asian Multilingual Thesaurus of Geosciences."@en ;
  dct:contributor "International Commission on Stratigraphy"@en ;
  dct:contributor "OneGeology Europe preferred labels merged in by S.M. Richard."@en ;
  dct:contributor "S M Richard"@en ;
  dct:created "2020-06-05"^^xsd:date ;
  dct:creator "Simon J D COX, CSIRO"@en ;
  dct:description "RDF representation of the Geologic Time Scale, as defined in the International Chronostratigraphic Chart (ICC) from the International Commission on Stratigraphy (ICS). The ICC embraces both chronostratigraphic (time-rock) units and their equivalent geochronologic (geologic-time) units, the former being related to the ‘Stratigraphic points’ referred to below, and the latter (geochronologic units) being employed in this RDF representation."@en ;
  dct:license <https://creativecommons.org/licenses/by/4.0/> ;
  dct:modified "2020-09-20"^^xsd:date ;
  dct:replaces ts:gts2018 ;
  dct:rights "Original version Copyright © 2020 International Commission on Stratigraphy"@en ;
  dct:rights "RDF version Copyright © 2020 CSIRO, IUGS"@en ;
  dct:source "Cohen, K.M., Finney, S.C., Gibbard, P.L. & Fan, J.-X. (2013; updated) The ICS International Chronostratigraphic Chart. Episodes 36: 199-204."@en ;
  dct:source "International Chronostratigraphic Chart 2020"@en ;
  dct:subject <http://dbpedia.org/page/Geologic_time_scale> ;
  dct:title "Geologic Time Scale (2020)"@en ;
  rdfs:label "Geologic Time Scale (2020)"@en ;
  rdfs:seeAlso <http://resource.geosciml.org/classifier/ics/ischart/2020> ;
  rdfs:seeAlso <http://stratigraphy.org/GSSP/index.html> ;
  rdfs:seeAlso <http://www.episodes.co.in/contents/2013/september/p199-204.pdf> ;
  rdfs:seeAlso <http://www.stratigraphy.org/GSSP/index.html> ;
  rdfs:seeAlso <https://stratigraphy.org/icschart/ChronostratChart2020-01.pdf> ;
  owl:versionInfo "gts2020:2020-01-13" ;
  skos:altLabel "International Chronostratigraphic Chart (2020)"@en ;
  skos:hasTopConcept isc:Phanerozoic ;
  skos:hasTopConcept isc:Precambrian ;
  skos:prefLabel "Geological Timescale (2020)"@en ;
  sdo:codeRepository <https://github.com/CGI-IUGS/timescale-data.git> ;
  skos:changeNote "2009-05-01 Introduced Holocene subdivisions, as shown in 2018 version from stratigraphy.org - see "@en ;
  skos:changeNote """2017-02-22 Added additional collections for eras of each rank;
classified rank-based collections using XKOS;
cleaned out legacy Base* instances that did not have links;
renamed *[GS]SP individuals to *SP;
removed all boundaries as TopConcepts, leaving on PreCambrian and Phanerozoic as TopConcepts"""@en ;
  skos:changeNote "2017/02 - Paleogene: Base of Chattian: The numeric age is updated to that at the ratified GSSP (27.82 Ma; Nanno et al. exp. 2017; by request of Simonetti Monechi)"@en ;
  skos:changeNote "2018-09-27 fixed some broken namespaces and prefixes, mostly related to SPARQL - some kind of search/replace error"@en ;
  skos:changeNote """2019-05-01 - Updated to 2018-08 version; 
removed StratigraphicPoints, Ranks, TimePositions collections; 
nested sub-collections in GeochronologicEra"""@en ;
  skos:changeNote """2019-06-10 - This revision adjusts the nomenclature of units to use only chronologic terminology rather than stratigraphic terminology [e.g. Cambrian-Age 2 in place of Cambrian-Stage 2; Cambrian-Epoch 2 in place of Cambrian-Series 2; Early/Late in place of Lower/Upper (namely in application to Epoch/time units rather than their equivalent Series/stratigraphic units—e.g. Early Jurassic Epoch rather than Lower Jurassic Series)]; and the whole artefact is renamed ‘Geologic Time Scale’. 
Also: changed samfl:shape --> geo:hasGeometry"""@en ;
  skos:changeNote "2020-01-13 - fix errors in Permian/Carboniferous - see https://github.com/GeoscienceAustralia/geosciml.org/issues/3#issuecomment-560054965"@en ;
  skos:changeNote "2020-01-13 - updated to 2019 version see http://stratigraphy.org/ICSchart/ChangeLog2012-2013-2014-2015-2016-2017-2018-2019.txt"@en ;
  skos:changeNote "2020-06-05 - updated to 2020 version see https://stratigraphy.org/icschart/ChangeLog2012-2013-2014-2015-2016-2017-2018-2019-2020.txt"@en ;
  skos:changeNote """2020-08-26 - 
1. removed concepts added to spoof the RVA preview; 
2. added rdf:type skos:Concept classification to all individuals whose type is a sub-class of skos:Concept 
3. remove time:TimePosition subClassOf skos:Concept . and axioms following from that 
4. mark concepts that are replaced owl:deprecated true 
5. remove most object-properties and rdf:type properties from deprecated resources"""@en ;
  skos:changeNote """2020-09-08
Changed all collections of eras of a single rank into OrderedCollections""" ;
  skos:changeNote "See <http://stratigraphy.org/ICSchart/ChangeLog2012-2013-2014-2015-2016-2017-2018.txt> for changes from prior versions"@en ;
  skos:editorialNote """<p>This dataset is being <a href=\"https://github.com/CGI-IUGS/timescale-data/\">maintained in GitHub</a></p>
 
<p>Please report errors, or propose improvements, using the <a href=\"https://github.com/CGI-IUGS/timescale-data/issues\">GitHub issue-tracker</a>."""^^rdf:HTML ;
  a gts:GeologicTimescale ;
  a time:TRS ;
.
```
