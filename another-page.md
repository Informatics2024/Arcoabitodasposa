---
layout: default
---

# METHODOLOGY.
>
## PROMPTING TECHNIQUES

The LLMS used were: CHAT GPT and GEMINI.

### The prompting techniques used were Zero-shot Prompting, Few-Shot Prompting, Chain-of-thought, and Generated-knowledge-prompting. To enrich the knowledge graph we asked the following questions:

## Enriching on the set of the wedding dress

### Q: Appartenente ad un completo da sposa costituito anche da un giacchino e da un cappello con velo. Abito lungo, a vita alta, con corpino e gonna, dalla linea leggermente svasata, senza maniche, chiuso posteriormente da cerniera. Il corpino è confezionato in tela batista di lino, la gonna in piqué di cotone rivestito da uno strato di merletto chimico a motivi geometrici, simili ad occhielli con mandorle centrali; sul retro, in corrispondenza della cerniera, il merletto presenta un piccolo spacco chiuso da bottoni. Privo di fodera. Presenta etichetta che ne attesta la provenienza sartoriale. Take the main elements of the wedding costume 

**- Chat GPT**

GPT A: Sure, here are the main elements of the wedding costume described:
1. Overall Ensemble:
Part of a bridal set including a jacket (giacchino) and a hat with a veil.
2. Dress Features:
Long dress.
High waist.
Sleeveless design.
Slightly flared line.
Back closure with a zipper.
No lining.
3. Materials:
Bodice (corpino): Made of linen batiste.
Skirt (gonna): Made of cotton piqué, covered with a layer of chemical lace featuring geometric patterns resembling eyelets with central almond shapes.
4. Additional Details:
Small slit on the back of the lace layer, aligned with the zipper, closed with buttons.
Sartorial label indicating custom tailoring.

    
- **GEMINI**

 Based on the provided description, the main elements of the wedding costume are:
1. Dress:
Type: Long, high-waisted dress
Silhouette: Slightly flared
Neckline: Sleeveless
Closure: Back zipper
Construction:
Bodice: Made of linen batiste
Skirt: Made of cotton piqué lined with geometric lace (resembling buttonholes with almond-shaped centers)
Back: Small slit at the back zipper, closed with buttons
Unlined
2. Jacket:
No specific details provided in the description, but it's likely a short jacket or bolero to complement the dress.
3. Hat with Veil:
No specific details provided in the description, but it's likely a delicate hat with a veil to match the overall style of the ensemble.
Additional Notes:
The dress is made of high-quality materials, including linen batiste and cotton piqué.
The lace detailing on the skirt adds a touch of elegance and sophistication.
The overall style is classic and timeless.
Overall, the wedding costume is a beautiful and elegant ensemble that would have been perfect for a special occasion.


## GIACCA (IMAGE)

```js
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>

SELECT ?ArtisticProperty ?label
WHERE {
?ArtisticProperty rdf:type a-cd:Clothing ;
rdfs:label ?label
FILTER(REGEX(?label, "giacca, da nozze", "i"))
}
```

## CAPPELLO- (NONE)
```js
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>
 
SELECT ?ArtisticProperty ?label
WHERE {
?ArtisticProperty rdf:type a-cd:Clothing ;
rdfs:label ?label
FILTER(REGEX(?label, “cappello da nozze”, “i”))
}
```

### Enriching on other clothes by Marucelli Germana exposed in the same museum


## What are the other clothes by Marucelli Germana exposed in Galleria del costume, in Firenze?


**- Chat GPT**

 The Galleria del Costume in Florence, housed in Palazzo Pitti, is showcasing a comprehensive exhibition titled "Germana Marucelli (1905-1983): A Visionary at the Origins of Made in Italy." This exhibition, running until September 24, 2023, presents around 150 pieces including clothes, jewelry, artworks, photographs, and sketches that reflect the creative genius of Germana Marucelli, an influential figure in Italian fashion.

Marucelli's work is displayed alongside the creations of Italian artists such as Paolo Scheggi, Pietro Gentili, and Getulio Alviani, emphasizing the relationship between fashion, art, and culture. Key pieces in the exhibition include various thematic collections that embody her innovative approach, like the op-dress, inspired by kinetic art, and dresses symbolizing the evolving female identity such as the Warrior-Priestess and the Mystical Woman​ (ARTEMORBIDA)​​ (www.okfirenze.com)​​ (Destination Florence)​​ (Le Gallerie degli Uffizi Shop)​.

The exhibition also recreates historical settings from Marucelli's life, including her cultural salon frequented by prominent poets and intellectuals, and her atelier designed by Paolo Scheggi in 1964. This immersive experience provides a unique insight into the historical and cultural context that influenced Marucelli's pioneering contributions to fashion​ (ARTEMORBIDA)​​ (www.okfirenze.com)​.

- **GEMINI**
  
Unfortunately, the information you provided about the wedding costume description doesn't directly reveal other Marucelli Germana garments exhibited at the Galleria del Costume in Florence.
Here are some ways to find out about other Marucelli Germana pieces:
Museo della Moda e del Costume website: Check the official website of the Museo della Moda e del Costume https://www.uffizi.it/en/pitti-palace/costume-and-fashion-museum for their online collections or virtual exhibitions. They might have a section dedicated to Marucelli Germana's work.
Exhibition Catalog: If you know the name of the specific exhibition where you encountered the wedding dress description, try searching for the exhibition catalog online or at a library. The catalog might list all the showcased garments, including other Marucelli Germana pieces.
Contact the Museum: You can contact the Museo della Moda e del Costume directly through their website or email (https://www.uffizi.it/palazzo-pitti/museo-della-moda-e-del-costume). They might be able to provide information about other Marucelli Germana garments in their collection.
Search for News Articles and Museum Publications: Look for news articles or publications related to the recent "Una visionaria alle origini del Made in Italy" exhibition dedicated to Marucelli Germana (from June to September 2023). These sources might discuss other garments displayed in the exhibition.
While these methods can't guarantee results, they offer possibilities for finding information about other Marucelli Germana garments in the museum's collection.


### Can you give me some examples?


- **Chat GPT**

Here are some notable examples of Germana Marucelli's clothes displayed at the Galleria del Costume in Florence:

Op-Dress: This dress showcases Marucelli's engagement with kinetic art, reflecting her collaboration with artist Paolo Scheggi. The design incorporates optical illusions and geometric patterns that create a dynamic, moving effect on the fabric, emphasizing the interplay between art and fashion.

Guerriera-Sacerdotessa (Warrior-Priestess): This ensemble represents Marucelli's vision of women as powerful and multifaceted. The design combines elements of strength and spirituality, featuring structured lines and intricate detailing that convey both power and grace.

Mystical Woman in Saio: Inspired by religious and mystical themes, this dress evokes a sense of serenity and introspection. The simple, flowing lines and muted colors reflect a contemplative aesthetic, highlighting Marucelli's ability to blend fashion with deeper cultural and spiritual narratives.

Cinetica (Kinetic Woman): Another example of Marucelli's collaboration with contemporary artists, this dress is characterized by bold patterns and shapes that give the illusion of movement. The design reflects the kinetic art movement's influence on fashion during the 1960s.

Crisalide (Chrysalis): This dress symbolizes transformation and evolution, with a design that suggests metamorphosis. The fabric and cut create a sense of fluidity and change, capturing the essence of a woman in constant development.

These pieces are part of a larger collection that includes not only clothing but also jewelry, artworks, and sketches, highlighting Marucelli's multidisciplinary approach and her role as a pioneer in the fusion of fashion and art​ (ARTEMORBIDA)​​ (www.okfirenze.com)​​ (Destination Florence)​​ (Le Gallerie degli Uffizi Shop)​.

```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
PREFIX a-cd: <https://w3id.org/arco/ontology/clothing-description/>
PREFIX dc: <http://purl.org/dc/elements/1.1/>

SELECT *
WHERE {
  ?ArtisticProperty rdf:type a-cd:Clothing ;
                    rdfs:label ?label ;
                    dc:creator <https://w3id.org/arco/resource/Agent/5c2b2a7e6b736bd45176a1270f1063db> .
  FILTER(REGEX(?label, "la donna cinetica", "i"))
}
```
>
## [SPARQL QUERIES](./another-page2.html)


[back](./)
