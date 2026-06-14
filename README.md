# MVTD-project
TEI encoding and visualization of two manuscript witnesses: "Nota quod sancto concilio non est detrahendum"

## Project Description

This project presents the transcription, encoding and visualization of two manuscript witnesses of Johann Hildessen's text *Nota quod sancto concilio non est detrahendum*.
Written around 1415 by the Bohemian master Jan Hildessen, this short text is a formal defense
of the Council of Constance and its supreme authority within the Church. In the midst of the
Hussite disputes, Hildessen argued that it was necessary to accept the decisions of ecumenical
councils and not to disparage them, specifically to defend the conciliar decree that
prohibited communion under both kinds (chalice and host) for the laity.

The work was developed within the ANTIDOTE project and is presented here for the course "Modelling and Visualizing Textual Data".

## **Sources**

The project is based on two manuscript witnesses:

| **Witness** | **Repository** | **Shelfmark** | **Folios** |
|----------|-----------|------------|------------|
| Witness 1 | Prague, Archiv Pražského hradu, Knihovna Metropolitní kapituly | D.54 | 166r–167v, 240r |
| Witness 2 | Vienna, Austrian National Library | MS 4941 | 14 |

Digital reproductions are available in the `images` folder.

## Manuscript Witnesses

### Prague D.54


## Data Modelling

The witnesses were encoded according to the TEI Guidelines.

The two manuscript witnesses were encoded in a single TEI document.

Each witness is represented as a separate textual division (`<div>`), allowing both witnesses to be navigated within the same TEI Publisher environment.

This solution was adopted to facilitate visualization on the same page through TEI Publisher.

The encoding represents:

- `<teiHeader>` for metadata;
- `<div>` for manuscript segmentation;
- `<pb>` for page breaks;
- `<lb>` for line breaks;
- `<expan>` and `<ex>` for abbreviation expansion;
- `<title>` for title statements;
- `<msDesc>` for manuscript description.

METTI ESEMPIO

## Customization and Visualization

The project uses a custom ODD specification (`hildessen.odd`) together with a TEI Publisher template (`expansions_template.XHT`).

The encoded text was visualized through TEI Publisher.

## Repository Structure

README.md

data/
    merged_manuscripts.xml

odd/
    hildessen.odd

templates/
    expansions_template.XHT

images/
    ONB.pdf
    KMK.pdf

screenshots/
    tei-publisher-view.png

## Repository History
This repository reorganizes and documents materials originally developed within the collaborative ANTIDOTE project.

Original repository:

[https://github.com/magdalukackovacova/GroupE]

The present repository was created to provide a clearer documentation of the modelling and visualization process for the purposes of the exam.

## Workflow and Reflections
1. Acquisition of manuscript reproductions
2. Transcription
3. TEI Encoding
4. ODD Customization
5. TEI Publisher Visualization
6. Revision and testing

AGGIUNGI

AGGIUNGI CHALLENGES
