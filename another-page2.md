---
layout: default
---

# SPARQL QUERIES

## FIND ALL THE ITEMS “abito da sposa” PRESENT IN THE CLOTHING DESCRIPTION ONTOLOGY 
```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>

SELECT ?ArtisticProperty ?label
WHERE {
?ArtisticProperty rdf:type a-cd:Clothing ;
rdfs:label ?label
FILTER(REGEX(?label, "abito da sposa", "i"))
}
```

## COUNT ALL THE ITEMS abito da sposa - (14)
```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>

SELECT (COUNT(DISTINCT ?ArtisticProperty) AS ?count)
WHERE {
  ?ArtisticProperty rdf:type a-cd:Clothing ;
                    rdfs:label ?label .
  FILTER(REGEX(?label, "abito da sposa", "i"))
}
```

## Are there any wedding dresses made of Silk and Cotton?
```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>
PREFIX dc: <http://purl.org/dc/elements/1.1/>
PREFIX a-dd: <https://w3id.org/arco/ontology/denotative-description/>

SELECT ?ArtisticProperty ?label?material
WHERE {
  {
    ?ArtisticProperty rdf:type a-cd:Clothing ;
                      rdfs:label ?label ;
                      a-dd:hasMaterial ?material .
    ?material rdfs:label "seta" .
    FILTER(REGEX(?label, "abito da sposa", "i"))
  }
  UNION
  {
    ?ArtisticProperty rdf:type a-cd:Clothing ;
                      rdfs:label ?label ;
                      a-dd:hasMaterial ?material .
    ?material rdfs:label "cotone" .
    FILTER(REGEX(?label, "abito da sposa", "i"))
  }
}
```

## Who are the creators of the wedding dresses?
```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>
PREFIX dc: <http://purl.org/dc/elements/1.1/>

SELECT DISTINCT ?ArtisticProperty ?label ?creator
WHERE {
?ArtisticProperty rdf:type a-cd:Clothing ;
rdfs:label ?label ;
dc:creator ?creator .
FILTER(REGEX(?label, "abito da sposa", "i"))
}
ORDER BY ?creator
```

## Which are the wedding dresses made of silk which have Marucelli Germana as the creator? - (None)
```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>
PREFIX dc: <http://purl.org/dc/elements/1.1/>
PREFIX a-dd: <https://w3id.org/arco/ontology/denotative-description/>
PREFIX agent: <https://w3id.org/arco/resource/Agent/>

SELECT *
WHERE {
  ?ArtisticProperty rdf:type a-cd:Clothing ;
                    rdfs:label ?label ;
                    dc:creator agent:5c2b2a7e6b736bd45176a1270f1063db ;
                    a-dd:hasMaterial ?material .
  ?material rdfs:label "seta" .
  FILTER(REGEX(?label, "abito da sposa", "i"))
}
```
## Which are the materials used by Marucelli Germana for the wedding dresses? - (Cotone and Lino)
```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>
PREFIX dc: <http://purl.org/dc/elements/1.1/>
PREFIX a-dd: <https://w3id.org/arco/ontology/denotative-description/>
PREFIX agent: <https://w3id.org/arco/resource/Agent/>

SELECT *
WHERE {
  ?ArtisticProperty rdf:type a-cd:Clothing ;
                    rdfs:label ?label ;
                    dc:creator agent:5c2b2a7e6b736bd45176a1270f1063db ;
                    a-dd:hasMaterial ?material .
  FILTER(REGEX(?label, "abito da sposa", "i"))
}
```
## Which are the wedding dresses made of silk which have Marucelli Germana as the creator? For all results provide the depiction if any is available.
```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>
PREFIX dc: <http://purl.org/dc/elements/1.1/>
PREFIX a-dd: <https://w3id.org/arco/ontology/denotative-description/>
PREFIX agent: <https://w3id.org/arco/resource/Agent/>

SELECT *
WHERE {
  ?ArtisticProperty rdf:type a-cd:Clothing ;
                    rdfs:label ?label ;
                    dc:creator agent:5c2b2a7e6b736bd45176a1270f1063db .
  FILTER(REGEX(?label, "abito da sposa", "i"))
OPTIONAL {?ArtisticProperty a-cd:depiction ?depiction }
}
```
[back](./)
