---
permalink: /vocabularies/Geological-Timescale/
layout: default
title: Geological Timescale
---

# Geological Timescale
## Governance - who is the content-custodian
**Rule 1.** Determine the governance arrangements and custodian of the legacy vocabulary

Global Boundary Stratotype Section and Points are officially ratified by the [International Commission on Stratigraphy](https://stratigraphy.org/).  
## Permission for re-purposing
**Rule 2.** Verify that the legacy-vocabulary license allows repurposing, and agree on the license for the FAIR vocabulary

The basic temporal-topology of the Geologic Timescale is standard knowledge in the geology community. 

The more specialized aspects of the information in the vocabulary relate to the 'stratotypes' for the boundaries in the timescale - i.e. (i) the location of the type-section that has been agreed to best represent the interval spanning the boundary, and the position within the section that corresponds with the actual boundary, and (ii) the best estimate of the age of samples of rock taken from the boundary point, which calibrates the age of the boundary. All these details are published on a per-boundary basis in the scientific literature, so can be transcribed from there. The standard information for each boundary, that is used by the [International Commission on Stratigraphy](https://stratigraphy.org/) to officially assign dates to the timescale are summarized in the [tabulation of Global Boundary Stratotype Section and Points](https://stratigraphy.org/gssps/). 

However, starting in 2020, the [International Commission on Stratigraphy](https://stratigraphy.org/) has agreed to used the FAIR vocabulary as the point-of-truth, all the resources on their website (the table of GSSPs, and the coloured chart) will be generated from the semantic resources.  

## Maintenance environment
**Rule 4.** Establish a technical maintenance environment for the FAIR vocabulary artefacts

Maintained in https://github.com/CGI-IUGS/timescale-data 

## Persistent unique identifiers
**Rule 5.** Assign a unique identifier to (a) the vocabulary and (b) each term in the vocabulary

## Term encoding
**Rule 6.** Create machine readable representations of the vocabulary terms 


## Vocabulary metadata
**Rule 7.** Add vocabulary metadata 

This vocabulary has a long history, so alongside the usual descriptive metadata, there is a set of dated `skos:changeNote` entries (many omitted here). 

```turtle
ts:gts2020
  a skos:ConceptScheme ;
  dct:title "Geologic Time Scale (2020)"@en ;
  rdfs:label "Geologic Time Scale (2020)"@en ;
  skos:altLabel "International Chronostratigraphic Chart (2020)"@en ;
  skos:hasTopConcept isc:Phanerozoic ;
  skos:hasTopConcept isc:Precambrian ;
  skos:prefLabel "Geological Timescale (2020)"@en ;
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
  rdfs:seeAlso <http://resource.geosciml.org/classifier/ics/ischart/2020> ;
  rdfs:seeAlso <http://stratigraphy.org/GSSP/index.html> ;
  rdfs:seeAlso <http://www.episodes.co.in/contents/2013/september/p199-204.pdf> ;
  rdfs:seeAlso <http://www.stratigraphy.org/GSSP/index.html> ;
  rdfs:seeAlso <https://stratigraphy.org/icschart/ChronostratChart2020-01.pdf> ;
  owl:versionInfo "gts2020:2020-01-13" ;
  sdo:codeRepository <https://github.com/CGI-IUGS/timescale-data.git> ;
  skos:editorialNote """<p>This dataset is being <a href=\"https://github.com/CGI-IUGS/timescale-data/\">maintained in GitHub</a></p>
<p>Please report errors, or propose improvements, using the <a href=\"https://github.com/CGI-IUGS/timescale-data/issues\">GitHub issue-tracker</a>."""^^rdf:HTML ;
  a gts:GeologicTimescale ;
  a time:TRS ;
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
.
```

## Vocabulary registration
**Rule 8.** Register the vocabulary

## Vocabulary access
**Rule 9.** Make the vocabulary accessible for humans and machines

