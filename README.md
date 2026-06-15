# MVTD-project
TEI encoding and visualization of two manuscript witnesses: "_Nota quod sancto concilio non est detrahendum_"

## Project Description

This project presents the transcription, encoding and visualization of two manuscript witnesses of Johann Hildessen's text "_Nota quod sancto concilio non est detrahendum_".
Written around 1415 by the Bohemian master, this short text is a formal defense of the Council of Constance and its supreme authority within the Church. In the midst of the Hussite disputes, Hildessen argued that it was necessary to accept the decisions of ecumenical councils and not to disparage them, specifically to defend the conciliar decree that prohibited communion under both kinds (chalice and host) for the laity.

The work was developed within the ANTIDOTE project and is presented here for the course "Modelling and Visualizing Textual Data".

## Sources

The project is based on two manuscript witnesses:

| **Witness** | **Repository** | **Shelfmark** | **Folios** |
|----------|-----------|------------|------------|
| Witness 1 | Prague, Archiv Pražského hradu, Knihovna Metropolitní kapituly | D.54 | 166r–167v, 240r |
| Witness 2 | Vienna, Austrian National Library | MS 4941 | 14 |

Digital reproductions are available in the `images` folder.

## Data Modelling

The witnesses were encoded according to the TEI Guidelines in a single TEI document.

Each witness is represented as a separate textual division (`<div>`), allowing both texts to be navigated on the same page through TEI Publisher.

The encoding represents:

- bibliographic and manuscript metadata;
- textual structure;
- layout information;
- abbreviation and expansion phenomena;
- uncertain readings;
- quotations and references.

Below are some examples of the main TEI elements used in the project.

| **Feature** | **TEI Element** | **Example in the text** | **Purpose**
|----------|----------|----------|----------|
| Abbreviations | `<expan>`, `<ex>` | `<expan>comm<ex>un</ex>icat</expan>` | Expansion of abbreviated forms while preserving editorial intervention. |
| Underlined text | `<title rendition="underline">` | `<title rendition="underline">Quod no<ex>n</ex> sit com<ex>mun</ex>icandum sub utra<ex>que</ex></title>` | Representation of graphic emphasis found in the manuscript. |
| Quotations | `<quote source="">` | `<quote source="St. Augustine, Contra epistulam Manichaei quam vocant fundamenti, ch. 5, n. 6">Aug<ex>ustinus</ex> Ew<ex>a</ex>n<ex>geli</ex>o no<ex>n</ex> cred<ex>er</ex>em nisi me eccl<ex>es</ex>ia com<ex>m</ex>ov<ex>er</ex>et</quote>` | Identification of quotations and attribution of their source. |
| Uncertain readings | `<unclear>` | `dic<unclear type="unclear">i?</unclear>` | Marking text that cannot be read or interpreted with certainty. |
| Supplied text | `<supplied>` | `<supplied desc="supplied">medicacione</supplied>` | Representation of text supplied by the encoder where the manuscript reading is incomplete or problematic. |


## Customization and Visualization

The encoded text was visualized through TEI Publisher.

The project uses a custom ODD specification (`hildessen.odd`) together with a modified template (`expansions_template.XHT`). 

Several visualization choices were made in order to represent manuscript features in a readable digital environment:

- expansions are highlighted in green;
- editorial corrections (`sic`) are displayed in red;
- underlined passages preserve the original manuscript emphasis;
- supplied text is displayed in grey;
- quotations are rendered in italics and accompanied by a tooltip containing the bibliographic reference;
- unclear readings are marked by question marks.

These choices were intended to preserve significant manuscript features while improving readability and user navigation.

> **Note:** the "Highlight Expansions" toggle is currently not functioning as intended. As a result, expansions remain permanently highlighted in the current version of the interface.

**Here's the link to the final visualization:**
http://localhost:8080/exist/apps/tei-publisher/test/Hildessen_xml.xml?view=div&odd=Hildessen%2520deff&template=facsimile.html 


## Workflow and Reflections

1. Acquisition of manuscript reproductions
2. Transcription
3. TEI Encoding
4. ODD and Template Customization
5. TEI Publisher Visualization
6. Revision and testing

One of the main challenges of the project concerned the representation and visualization of multiple manuscript witnesses. The original corpus consisted of six manuscript witnesses. For the current phase of the project, only two witnesses were selected and integrated into the TEI Publisher interface.

This decision was motivated by visualization and usability considerations: displaying a larger number of witnesses simultaneously would have resulted in a cluttered and less readable interface.


## Repository Structure

```
.
├── README.md
├── data/
│   └── merged manuscripts.xml
├── images/
│   ├── KMK D 54 fol 14 (1).pdf
│   └── ÖNB 4941 fol 166r–167v, 240r (1).pdf
├── odd/
│   └── Hildessen (1).odd
├── screenshots/
│   └── screenshot.png
└── templates/
    └── expansions_template.XHT

```

## Repository History
This repository reorganizes and documents materials originally developed within the collaborative ANTIDOTE project, 2025/26. 

The original work was carried out in collaboration with Magdaléna Lukáč Kováčová, Michaela Szabóová and Michal Hokeš

Original repository:

[https://github.com/magdalukackovacova/GroupE]

The present repository was created to provide a clearer documentation of the modelling and visualization process for the purposes of the exam.
