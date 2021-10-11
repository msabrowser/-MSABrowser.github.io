![MSABrowser Logo](https://user-images.githubusercontent.com/65191506/81839302-06123400-9550-11ea-92d2-ac904ccd32c6.png)

---

# 🧬 MSABrowser
**Table of Contents**

- [🧬 MSABrowser](#-msabrowser)
  - [What is *MSABrowser* and the aim of this library?](#what-is-msabrowser-and-the-aim-of-this-library)
  - [Screenshot](#screenshot)
  - [Citing the *MSABrowser*](#citing-the-msabrowser)
  - [Feature Comparison Table](#feature-comparison-table)
  - [Requirements and Installation](#requirements-and-installation)
  - [How to use *MSABrowser*?](#how-to-use-msabrowser)
  - [Parameters & Examples for the Functions](#parameters--examples-for-the-functions)
    - [Color Schemas List](#color-schemas-list)
    - [Adding Annotations (Protein Domains) & Example](#adding-annotations-protein-domains--example)
    - [Adding Variations and Modifications & Example](#adding-variations-and-modifications--example)
  - [Example Usages (Use Cases) of *MSABrowser*](#example-usages-use-cases-of-msabrowser)
    - [Evolutionary/Comparative Genomics Study](#evolutionarycomparative-genomics-study)
    - [NIPBL Protein Homologs Study](#nipbl-protein-homologs-study)
    - [COVID-19 / Virology Study](#covid-19--virology-study)
    - [Spike Proteins Example](#spike-proteins-example)
    - [Simulated FASTA Example](#simulated-fasta-example)
    - [Do you have another study which is not listed here?](#do-you-have-another-study-which-is-not-listed-here)
  - [Contributing & Feedback](#contributing--feedback)
  - [Developers](#developers)

---

##  What is *MSABrowser* and the aim of this library?
MSABrowser is developed as a new JavaScript tool with an ultimate goal of dynamic and fast visualization of sequence alignments, variations, and annotations. Also, it does not require any installation at any platform such as Linux, Mac OS X, and Windows. 

*MSABrowser* is able to import pairwise sequence alignment (PSA) and multiple sequence alignment (MSA) data in FASTA format, and variations and sequence annotations in the format of JSON (JavaScript Object Notation). 

For the nucleotides or amino acids that are annotated, one can hover them for triggering a pop-up that shows the details of variations and modifications or any other provided notes for the position. 

## Screenshot

<br>
1. MSABrowser Overview

  ![MSABrowser Screenshots](https://user-images.githubusercontent.com/49681382/136694235-509b6f32-423f-4ecd-aa9f-9b3089a8bdee.jpg)

  <details>
    <summary>➤ An overview of the MSABrowser tool. (Click here to see the full description for the image)</summary>
    MSA for homologous proteins of the human TUBA1A is depicted in this figure, along with genetic variations on the corresponding positions on sequences and associated intervals such as protein domains. (A) 
  
  (I) The annotation part represents the specified intervals for the sequence and in this example, it is used for illustrating the positions of the protein domains with cross-link features that enable users to locate the website or page of the original database or article. 
  
  (II) The notification part shows any type of defined modifications as a red asterisk above the sequence per position and displays the searched position in a species above the alignments. 
  
  (III) The sequence alignment part contains the imported alignment data with the previously selected colour scheme. Also, rounded (circle) positions indicate that at least one genetic variation or modification exists in this position. A rectangular white background pop-up box appears when the mouse hovers the specific position in the sequence and the genetic variations and modifications are listed in this pop-up box. On the bottom, an auto-generated ‘Consensus’ sequence is displayed. On the left side, species names contain cross-reference links for referring to the dedicated page of the sequence according to its protein identifier such as a UniProt number and the near-white ‘x’ button enables users to hide the sequence from the alignment together with its identifier. 
  
  (IV) A position in the sequence of any species listed in the alignment can be searched and the sequence alignment data in FASTA format can be downloaded with the blue button and visualization of alignment data can be exported as PNG format. Also, with the green ‘Reset’ button, it is available to reload the viewer. 
  
  (B) Visualization of MSAs of six virus spike proteins with the MSABrowser tool. The positions with the annotations are marked in a circle, while the positions without annotations are displayed in a square. The full MSA comparisons with annotations can be found at our dedicated GitHub site https://thekaplanlab.github.io/ 
  
  (C) Shown is the display of orthologous variants (OrthoVars), the positions of amino acid position or nucleotide, or PTMs with the programmable notification part of MSABrowser
  </details>

<br>

2. MSABrowser 
  
  ![MSABrowser Comparison](https://user-images.githubusercontent.com/49681382/136694363-816f4c27-a969-4601-878c-5036c9dfecad.jpg)

  <details>
    <summary>➤ Comparison of MSA visualizers. (Click here to see the full description for the image)</summary>
Comparison of MSA visualizers. The MSA of different genomes of the severe acute respiratory syndrome coronavirus 2 isolates (SARS-CoV-2: MT123293, MT152824, MT252708, MN988713 and MT039888) was created, followed by visualization with separate MSA viewers. 
  
  (A) Shown is the MSA visualization with MSABrowser, which enables the addition of annotations (e.g. domains and notes) on top of the MSA. MSABrowser allows users to incorporate variant-specific annotations (missense variation, disease associations, variant ID, allele frequency, etc.). A pop-up will show up when users click on the circled amino acid or nucleotide position to display the annotations. Shown is a missense variation (G6537T) in SARS-CoV, an example of a particular annotation of a nucleotide position, MSABrowser enables users to remove the desired sequence by clicking the X button which appears in the far left of each line. Users can look up positions, download the FASTA and save the MSA as PNG. 
  
  (B) Shown is MSAViewer tool on the same alignment as in A. Users can scroll to the left and right to see the rest of MSA. When the user clicks on a position, the amino acid is highlighted with a red square as in the position 88. 
  
  (C) Shown is JSAV. It is possible to sort and delete sequences, add new sequences, change the colour schema and export FASTA with the buttons listed below the MSA. 
  
  (D) Shown is Wasabi in which zoom in and zoom out options are enabled and scrolling is necessary to see the rest of the sequence. 
  
  (E) Shows Proviz where users are able to search for a motif, switch to full screen, export the MSA and share it as a URL using the buttons located in the top right corner. 
  
  (F) Shown is AlignmentViewer. For each sequence in the alignment, gaps ratio and identification ratio to the reference sequence is provided. Gaps and conservation per position are also shown above the MSA
</details>

##  Citing the *MSABrowser*

Furkan M Torun, Halil I Bilgin, Oktay I Kaplan, MSABrowser: dynamic and fast visualization of sequence alignments, variations and annotations, Bioinformatics Advances, Volume 1, Issue 1, 2021, vbab009, [https://doi.org/10.1093/bioadv/vbab009](https://doi.org/10.1093/bioadv/vbab009)
    
## Feature Comparison Table

| Features / Tools | MSABrowser | Plotly Needle Plot | AlignmentViewer | MSAViewer | ProViz | Wasabi | JavaScript Sequence Alignment Viewer (JSAV) | JalView Version 2 |
|-|-|-|-|-|-|-|-|-|
| OVERALL |  |  |  |  |  |  |  |  |
| Publication Date | April 2021 | 2019 | 22 February 2018 | 13 July 2016 | 16 April 2016 | 03 December 2015 | 23 October 2014 | 16 January 2009 |
| Technology | JavaScript | JavaScript, Python | JavaScript | JavaScript | JavaScript | JavaScript, Python | JavaScript | Java |
| Open-source code | Available | Available | Available | Available | Available | Available | Available | Available |
| Open-source entity | https://github.com/thekaplanlab/msabrowser | https://github.com/plotly/dash-bio | https://github.com/sanderlab/alignmentviewer | https://github.com/wilzbach/msa | https://bitbucket.org/daveylab/proviz/ | https://github.com/veidenberg/wasabi | https://github.com/AndrewCRMartin/JSAV/ | https://source.jalview.org/crucible/browse/jalview |
| Embeddable component to a website | Available | Available | Not available | Available | Not available | Not available | Available | Not available |
| VISUALIZABLE DATA SOURCES |  |  |  |  |  |  |  |  |
| MSA/PSA data source | Fasta | Not available | Fasta, Stockholm | Fasta, Clustal | Fasta, UniProt Data Retrieving | Fasta, Clustal, Ensembl Data Retrieving, NEXUS, Phylip | Fasta | Fasta, Clustal, Stockholm, Phylip |
| Alignment data export | Fasta, Image | Fasta, NEXUS, Phylip | Fasta, Stockholm | Fasta, Image | Available | Fasta, NEXUS, Phylip | Fasta | Fasta, Clustal, Stockholm, Phylip, Image |
| Variations / PTMs / Modifications | Available | Available | Not available | Not available | Automatic retrieval | Not available | Not available | Available, Automatic retrieval |
| Annotations (Domains/Sequence intervals) | JSON | JSON | Not available | GFF | Automatic retrieval | Not available | Not available | GFF |
| Sequence annotation formats | JSON | Not available | Tab separated text file | JalView and GFFv3 | Automatic retrieval | Not available | Not available | GFF |
| Phylogenetic tree data | Not available | Not available | Not available | Newick | Not available | Newick, NEXUS, Ensembl Data Retrieving | Not available | Newick |
| USER INTERFACE & EXPERIENCE |  |  |  |  |  |  |  |  |
| Direct jumping to a specific position (i.e.residue) | Available | Available | Not available | Available | Not available | Not available | Not available | Not available |
| Addressing a specific position in a sequence (i.e. species) | Available | Not available | Not available | Not available | Not available | Not available | Not available | Not available |
| Searching a motif in the sequence(s) | Not available | Not available | Not available | Available | Available | Not available | Not available | Available |
| Change among different color schemas | Available | Not available | Not available | Available | Not available | Available | Available | Available |
| Removing sequence(s) | Available | Not available | Available | Available | Available | Available | Available | Available |
| Generating consensus | Available | Not available | Available | Available | Not available | Not available | Not available | Available |
| Linking the identifiers to the resources | Ensembl, UniProtKB, NCBI, Pfam | Not available | UniProtKB, Pfam | UniProtKB, GenBank | UniProtKB | Not available | Not available | EMBL-EBI Search |

##  Requirements and Installation
*MSABrowser* is entirely developed in JavaScript and works on a web browser at any platform including Linux, Mac OS X and Windows systems without any installation.

##  How to use *MSABrowser*?
 - Create a directory and download any example listed below or use CDN (Content Delivery Network) links for required files on your page or clone the repository via Git using following command:
 
    `git clone https://github.com/thekaplanlab/msabrowser.git`

    **CDN Links:**

    - JS: [https://cdn.jsdelivr.net/gh/thekaplanlab/msabrowser/javascript/msabrowser.js](https://cdn.jsdelivr.net/gh/thekaplanlab/msabrowser/javascript/msabrowser.js)

    - CSS: [https://cdn.jsdelivr.net/gh/thekaplanlab/msabrowser/css/style.css](https://cdn.jsdelivr.net/gh/thekaplanlab/msabrowser/css/style.css)


    > **NOTES for CDN:**
    > 
    > The CDN is used to minimize delays for fetching the required files (JS, CSS, or others) and for loading web page content in less time. 
    > The links for CDN files should be integrated into `<head> </head>` tags using proper tags `<link type="text/css">` for CSS and `<script>` for JS. To see how it looks at the end, the following example or other case studies might be checked.
    > [Click here to reach MSABrowser basic template to learn how these CDN files are used and to see how a basic example can be done.](https://github.com/thekaplanlab/msabrowser/blob/master/examples/template.html)
    
    <br>
    
    > **NOTES for Custom Styling:**
    > 
    > We develop MSABrowser and implement the features after taking a number of comments about to make user interface and user experience of the tool better.
    > 
    > However, one has always a chance to customize the CSS and JS files according to their needs. As an example, the shadow color of the nucleotides with an alteration might be updated or red asterisk might be converted to another proper sign in blue based on the requirements of the users.    

- Then, place your pairwise or multiple sequence alignment (MSA) result file as **FASTA** format in the folder.

- Afterwards, set your parameters and define the title, specify the annotations such as protein domains and add your variations. 

- It's ready to use and visualize now! 

##  Parameters & Examples for the Functions

**Parameters for MSABrowser**

| Parameter | Description | Example |
|-----------------------|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| id | *It defines the ID of the element where you place MSABrowser component.* |`<section id="MSABrowserDemo"></section>` |
| fasta | *It refers a variable that holds your sequence alignment or the name of the file in FASTA format* | `sample_msa.txt` or `sample_msa.fasta` |
| hasConsensus  | *It asks whether you would like to display the consensus sequence or not.* | Please state as either `true` or `false`. |
| annotations  | *It refers a variable that holds your annotations such as protein domains.* | Please check the example below. |
| alterations | *It serves for adding variations and modifications on the corresponding positions.* | Please check the example below. |
| colorSchema  | *It defines the name of the color schema you would like to display.* | Please the check the list of color schemas below. |

<br>

**Functions for MSABrowser**

| Function | Description | Example |
|-----------------------|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `scrollToPosition(sequenceIndex, position)` | *It enables addressing a specific position in a species.* | Please, specify the `sequenceIndex` according to the order of sequence in the alignment file and give the  `position` for the navigating. **The dashes/gaps should not be considered while counting the positions, in other words, the real position/residue number in sequence alone should be entered.**  |
| `export("MSA_export.fasta")` | *It serves for downloading the alignment data. You can give a filename for the output into the function.* | Default name is `"MSA_export.fasta"`, might be changed always. |


###  Color Schemas List

> You need to select a color schema and put the name of the color schema into the variable:

Example for this:
> `colorSchema = "clustal";`

**List of the color schemas:**

- `hydrophobicity`
- `buried`
- `cinema`
- `clustal`
- `clustal2`
- `helix`
- `lesk`
- `mae`
- `strand`
- `taylor`
- `turn`
- `zappo`
- `nucleotide`


###  Adding Annotations (Protein Domains) & Example

> You are able to visualize the protein domains above the sequence aligner in the annotation part.

> Also, you might consider to add more than one annotation parts in the *MSABrowser*.

Here is the example use of `annotations` variable.
```
var annotations = [
    {
        source: "SourceName1",
        data: [
            {
                'annotation_id': 'AnnotationID',
                'annotation_name': 'AnnotationName',
                'annotation_external_link': 'https://thekaplanlab.github.io',
                'annotation_start_point': 15,
                'annotation_end_point': 290
            },
            {
                'annotation_id': 'SecondAnnotationID',
                'annotation_name': 'SecondAnnotationName',
                'annotation_external_link': 'https://thekaplanlab.github.io',
                'annotation_start_point': 450,
                'annotation_end_point': 570
            }
        ]
    }, 
    {
        source: "SourceName2",
        data: [
            {
                'annotation_id': 'AnnotationID',
                'annotation_name': 'AnnotationName',
                'annotation_external_link': 'https://thekaplanlab.github.io',
                'annotation_start_point': 25,
                'annotation_end_point': 160
            },
            {
                'annotation_id': 'SecondAnnotationID',
                'annotation_name': 'SecondAnnotationName',
                'annotation_external_link': 'https://thekaplanlab.github.io',
                'annotation_start_point': 250,
                'annotation_end_point': 490
            }
        ]
    }
]
```

**Here is the details for use of `annotations` :**

| Key | Description | Example |
|---------------------------------------------------|--------------------------------------------------------|----------------------------------------------------------|
| annotation_id | ID of the annotation/sequence interval to be shown in the annotations bar. | PF00091.25|
| annotation_name | A name of the annotation can be provided. | Tubulin |
| annotation_external_link | The link might be provided for referring the source of the annotation once it is clicked. | https://pfam.xfam.org/family/PF00091.25 |
| annotation_start_point | It refers to starting point of the defined sequence interval. **The dashes/gaps in alignment should not be considered while counting the positions, in other words, the real position/residue number in sequence alone should be entered.**  | `3` should be provided if we start it from `"L"` within such a sequence: "MA---LKER--MA--R" |
| annotation_end_point | It refers to end point of the defined sequence interval. **The dashes/gaps in alignment should not be considered while counting the positions, in other words, the real position/residue number in sequence alone should be entered.**  | `9` should be provided if we start it from `"R"` within such a sequence: "MA---LKER--MA--R" |



###  Adding Variations and Modifications & Example

> You are able to add variations and modifications or any types of notes on the corresponding positions.

**Here is the details for use of `alterations` :**


| Key | Description | Example |
|---------------------------------------------------|--------------------------------------------------------|----------------------------------------------------------|
| sequenceIndex | The order of the species in the sequence alignment | 1 |
| position | The (real) position of the amino acid in the protein.* | 5 |
| note | The annotation part for this position. | M->A : Pathogenic and causes a disease with a name of X. |
| source | The source of the information. | Surname et. al (2020) |
| type | *The type of the alteration: Variation or modification* | If it is modficiation, state as `Alteration.Modification`. |



**Here is the example how to add a variation or modification:**
```
var alterations = [
    {
        'sequenceIndex': 2, 
        'position': 5, 
        'note': 'M->A : Pathogenic and causes a disease X', 
        'source': 'Surname et. al (2020)'
    },
]
```

> Here, this variation will be added onto the `5th` position in the sequnce of `2nd` species in the alignment data with a note of "`M->A : Pathogenic and causes a disease with a name of X`" and source of "`Surname et. al (2020)`". 

> In addition, if you state the `type` as `Alteration.Modification` (i.e. post-translational modification), it also will be notified as `red asterisk` in the viewer.

> **NOTE**:
> 
> Also, you might want to add several other HTML tags such as `a`, `div`, `p`, or `img` into the `notes` section of an alteration to provide more detail about your variation or modification. 
> 
> For instance, cross-reference link by adding it within the `note` after changing the link in `href` attribute:
> 
> `<a href="http://thekaplanlab.github.io" target="_blank">For details, visit here</a>`
>
> Moreover, use of other tags (`div`, `p`, and `img` in addition `a`) is provided as an example in the template file. [Please click here to reach MSABrowser basic template to learn how you other HTML tags are used and to see how a basic example can be done.](https://github.com/thekaplanlab/msabrowser/blob/master/examples/template.html)


##  Example Usages (Use Cases) of *MSABrowser*

###  Evolutionary/Comparative Genomics Study 
In this example, human TUBA1A protein and its homologous proteins are aligned and human protein domains are added. Additionaly, some genetic variations are also included from different sources such as gnomAD and ClinVar. 

> [Click here to reach *MSABrowser* example for Evolutionary/Comparative Genomics Study.](https://github.com/thekaplanlab/msabrowser/blob/master/examples/TUBA1A.html)

<iframe height="640" style="width: 100%;" scrolling="no" title="MSABrowser | TUBA1A" src="https://codepen.io/bilginhalil/embed/NWGzgdy?height=640&theme-id=light&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/bilginhalil/pen/NWGzgdy'>MSABrowser | TUBA1A</a> by halil bilgin
  (<a href='https://codepen.io/bilginhalil'>@bilginhalil</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### NIPBL Protein Homologs Study
In this example, human NIPBL protein and its homologous sequences are aligned and human sequence annotations are added.
Additionaly, some genetic variations are also included from available sources.

> [Click here to reach *MSABrowser* example for NIPBL Protein Homologs Study.](https://github.com/thekaplanlab/msabrowser/blob/master/examples/NIPBL.html)

<iframe height="748" style="width: 100%;" scrolling="no" title="MSABrowser | NIPBL" src="https://codepen.io/bilginhalil/embed/bGVxJGY?height=748&theme-id=light&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen MSABrowser | NIPBL by halil bilgin @bilginhalil) on CodePen.</iframe>

###  COVID-19 / Virology Study 
In this example, some available SARS-CoV-2 sequences are aligned with default options of MUSCLE and their genetic variations received from [China National Center for Bioinformation 2019 Novel Coronavirus Resource (2019nCoVR)](https://bigd.big.ac.cn/ncov/) are added.

> [Click here to reach *MSABrowser* example for COVID-19 / Virology Study.](https://github.com/thekaplanlab/msabrowser/blob/master/examples/SarsCov2.html)

<iframe height="565" style="width: 100%;" scrolling="no" title="MSABrowser | SARS - CoV-2 Example" src="https://codepen.io/bilginhalil/embed/QWjxgwa?height=565&theme-id=light&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/bilginhalil/pen/QWjxgwa'>MSABrowser | SARS - CoV-2 Example</a> by halil bilgin
  (<a href='https://codepen.io/bilginhalil'>@bilginhalil</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Spike Proteins Example
In this example, spike proteins are retrieved and aligned. Additionaly, some genetic variations and modifications are also added.

> [Click here to reach *MSABrowser* example for Spike Proteins.](https://github.com/thekaplanlab/msabrowser/blob/master/examples/SpikeProteins.html)

<iframe height="614" style="width: 100%;" scrolling="no" title="MSABrowser | Spike Proteins" src="https://codepen.io/bilginhalil/embed/JjYBBGz?height=614&theme-id=light&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true"> See the Pen MSABrowser | Spike Proteins by halil bilgin @bilginhalil) on CodePen</iframe>

### Simulated FASTA Example
In this example, we created a FASTA file with 75 sequences each have more than 75000 amino acids. This is to show the power of our visualization tool. It works smoothly even if the FASTA file is huge.

> [Click here to reach *MSABrowser* example for Simulated fasta.](https://github.com/thekaplanlab/msabrowser/blob/master/examples/Simulated.html)
<iframe height="614" style="width: 100%;" scrolling="no" title="MSABrowser | Spike Proteins" src="https://codepen.io/bilginhalil/embed/xxqogqp?height=614&theme-id=light&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true"> See the Pen MSABrowser | Spike Proteins by halil bilgin @bilginhalil) on CodePen</iframe>

###  Do you have another study which is not listed here?
Please do not hesitate to [contact us](#developers) for adding your study! 

We would be very happy to list your study here!


##  Contributing & Feedback
MSABrowser is released as an open-source and web-based software under MIT license. The visualizer, documentation, all source code and examples are available on [https://thekaplanlab.github.io/](https://thekaplanlab.github.io/) and at GitHub repository [https://github.com/thekaplanlab/msabrowser](https://github.com/thekaplanlab/msabrowser).

Moreover, please do not hesitate to `open an issue via Github` if you have any suggestion or feedback.


##  Developers

**Halil I. Bilgin ([@halilbilgin](https://github.com/halilbilgin)) |  [bilginhalil@gmail.com](mailto:bilginhalil@gmail.com) | 
Academia: [Google Scholar Profile](https://scholar.google.com/citations?user=U1jyUGkAAAAJ&hl=en&oi=ao)**

**Furkan M. Torun ([@furkanmtorun](http://github.com/furkanmtorun)) |  [furkanmtorun@gmail.com](mailto:furkanmtorun@gmail.com) |
Academia: [Google Scholar Profile](https://scholar.google.com/citations?user=d5ZyOZ4AAAAJ)**

**Oktay I. Kaplan |  [oktaykaplan@gmail.com](mailto:oktaykaplan@gmail.com) | 
Academia: [Google Scholar Profile](https://scholar.google.com/citations?user=YFzvQQUAAAAJ&hl=en)**

