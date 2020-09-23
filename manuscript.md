---
author-meta:
- Tiago Lubiana
bibliography:
- content/manual-references.json
date-meta: '2020-09-23'
header-includes: "<!--\nManubot generated metadata rendered from header-includes-template.html.\nSuggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html\n-->\n<meta name=\"dc.format\" content=\"text/html\" />\n<meta name=\"dc.title\" content=\"Towards a pragmatic definition of cell type\" />\n<meta name=\"citation_title\" content=\"Towards a pragmatic definition of cell type\" />\n<meta property=\"og:title\" content=\"Towards a pragmatic definition of cell type\" />\n<meta property=\"twitter:title\" content=\"Towards a pragmatic definition of cell type\" />\n<meta name=\"dc.date\" content=\"2020-09-23\" />\n<meta name=\"citation_publication_date\" content=\"2020-09-23\" />\n<meta name=\"dc.language\" content=\"en-US\" />\n<meta name=\"citation_language\" content=\"en-US\" />\n<meta name=\"dc.relation.ispartof\" content=\"Manubot\" />\n<meta name=\"dc.publisher\" content=\"Manubot\" />\n<meta name=\"citation_journal_title\" content=\"Manubot\" />\n<meta name=\"citation_technical_report_institution\" content=\"Manubot\" />\n<meta name=\"citation_author\" content=\"Tiago Lubiana\" />\n<meta name=\"citation_author_institution\" content=\"Computational Systems Biology Laboratory, University of S\xE3o Paulo\" />\n<meta name=\"citation_author_orcid\" content=\"0000-0003-2473-2313\" />\n<link rel=\"canonical\" href=\"https://lubianat.github.io/technotype/\" />\n<meta property=\"og:url\" content=\"https://lubianat.github.io/technotype/\" />\n<meta property=\"twitter:url\" content=\"https://lubianat.github.io/technotype/\" />\n<meta name=\"citation_fulltext_html_url\" content=\"https://lubianat.github.io/technotype/\" />\n<meta name=\"citation_pdf_url\" content=\"https://lubianat.github.io/technotype/manuscript.pdf\" />\n<link rel=\"alternate\" type=\"application/pdf\" href=\"https://lubianat.github.io/technotype/manuscript.pdf\" />\n<link rel=\"alternate\" type=\"text/html\" href=\"https://lubianat.github.io/technotype/v/4a4eff99aacb86eb3c4d548e58aecf72d824696a/\" />\n<meta name=\"manubot_html_url_versioned\" content=\"https://lubianat.github.io/technotype/v/4a4eff99aacb86eb3c4d548e58aecf72d824696a/\" />\n<meta name=\"manubot_pdf_url_versioned\" content=\"https://lubianat.github.io/technotype/v/4a4eff99aacb86eb3c4d548e58aecf72d824696a/manuscript.pdf\" />\n<meta property=\"og:type\" content=\"article\" />\n<meta property=\"twitter:card\" content=\"summary_large_image\" />\n<link rel=\"icon\" type=\"image/png\" sizes=\"192x192\" href=\"https://manubot.org/favicon-192x192.png\" />\n<link rel=\"mask-icon\" href=\"https://manubot.org/safari-pinned-tab.svg\" color=\"#ad1457\" />\n<meta name=\"theme-color\" content=\"#ad1457\" />\n<!-- end Manubot generated metadata -->"
keywords:
- cell type
- nomenclature
- classification
lang: en-US
manubot-clear-requests-cache: false
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
title: Towards a pragmatic definition of cell type
...






<small><em>
This manuscript
([permalink](https://lubianat.github.io/technotype/v/4a4eff99aacb86eb3c4d548e58aecf72d824696a/))
was automatically generated
from [lubianat/technotype@4a4eff9](https://github.com/lubianat/technotype/tree/4a4eff99aacb86eb3c4d548e58aecf72d824696a)
on September 23, 2020.
</em></small>

## Authors



+ **Tiago Lubiana**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0003-2473-2313](https://orcid.org/0000-0003-2473-2313)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [lubianat](https://github.com/lubianat)<br>
  <small>
     Computational Systems Biology Laboratory, University of São Paulo
  </small>



## Abstract {.page_break_before}




# Introduction

One of the basic classes in any undergraduate major in life sciences is the histology class. The students are tasked with identifying cel types across various tissues, looking for color and shape patterns in hematoxylin-eosin stains. The text-books, such as the one by Junqueira & Carneiro[@isbn:9788527723114], work as manuals (in the Kuhnian sense)[@isbn:9780226458113] that perpetuate the paradigms of what we know about a couple hundred cell types.

Our concept of "cell type", thus, is still based on century-old histochemical techniques -  such as the Golgi-stains of neurons immortalized by Ramon y Cajal[@doi:10.1016/j.cub.2004.06.035]. The histological influence is noticeable even in names given to cell types: "erithrocytes", "eosinophil", "basophils", "oxyphilic cell of the thyroid". The concepts we use are drawn from studies of microanatomy. The connection with anatomy leads to thinking about cell types as anatomical entities as if they were clearly dissectable and fixed in an organism. This may be the reason why attempts to quantify cell types use the scale of "hundreds" of human cell types [@https://bionumbers.hms.harvard.edu/bionumber.aspx?id=103626] [@https://askabiologist.asu.edu/questions/human-cell-types] [@doi:10.1016/j.cels.2017.03.006.].

New techniques have challenged this anatomy based conceptualization. From flow cytometry to patch clamping, to single-cell RNA-seq, we saw a burst of new categories, and novel cell "subtypes" and "families" popped up in the literature. The bursting intensified explosively in the past few years, with the rise of projects to characterize _all_ human cell types [@doi:10.7554/eLife.27041] HUBMAP [@pmid:31597973].

The advances in biology require us to find better answers for how to define a cell type. The concept might not have a "true" meaning, in a philosophical-realistic sense. Nevertheless, we can strive to find nominal, pragmatic definitions for the pragmatic challenges of large scale biology. Otherwise, how can we precisely label single-cell data? How can we formalize the discovery of new cell types? How can we integrate the knowledge from the millions of scientific articles published every year? 

The need for conceptual advance is perceived by the community [@pmid:28334573], and new perspectives are arising. One core line of thought is evolutionary: the cell type as an evolutionary unit defined by a Core Regulatory Complex (CoRC) of transcription factors. That definition enables the drawing of parallels between the evolution of other biological entities (such as genes, proteins and species) to the evolution of cell types. Models of how multicellular life works greatly benefit from concepts such as "sister types" (cell types that diverged from a single ancestor), "cell type homology," (cell types in different species that share a common evolutionary origin) and "cell type convergence" (cell types that execute similar functions, but which are not directly evolutionarily related). [@pmid:18927580] [@doi:10.1038/nrg.2016.127] 

However, as much as different concepts of species coexist [@doi:10.1080/10635150701701083], our quest to define cell types may take various forms. The challenge of representing cell types in the context of evolution is conceptually different from the challenge of representing cell types in biomedical experimentation. In that second direction,  the groundwork of the Cell Ontology [@doi:10.1186/gb-2005-6-2-r21] [@doi:10.1186/1471-2105-12-6] [@doi:10.1186/s13326-016-0088-7] project and the International Workshop on Cells in Experimental Life Sciences[@doi:10.1186/s12859-017-1976-2] [@doi:10.1186/s12859-019-2721-9] are notable. Their contributions base much of the views here and will be discussed in detail throughout the article. 

The conceptual quest addressed by this work is one of the research synthesis and is summarized in the following question: which cell type definition can be crafted for rigorously describing biomedical experiments?

For that goal, the body of the article is divided in 4 parts. In Part 1, I will bring a proposal of a set of rules that are sufficient for defining  cell types. In Part 2, I'll propose a small set of names for differentiating main classes of cell types. In Part 3, I will address the logical consequences of the proposed definitions. And in Part 4, I will discuss the pragmatic challenges for employing such definitions.

# A set of 3 + 1 rules for defining a cell type

In an opinion article published in Cell Systems in 2017, researchers presented their views on  the "Conceptual Definition of 'Cell Type' in the Context of a Mature Organism?" [@pmid:28334573]. The opinions vary, and do not converge to a consensus. Many of the scientists see a core role of cells' functions in defining cell types, a slippery road, as the meaning of "function" in biology is elusive [@doi:10.7554/eLife.47014].

In one recent attempt to define cell types for single cell RNA-Seq, Aevermann et al came up with a set of needs: "The minimum set of necessary and sufficient marker genes selectively expressed by the cell type", "A parent cell class in the CL", and "A specimen source description (anatomic structure þ species)." [@pmid:29590361] They have great merit in defining clear guidelines for marking a cell type. The requirement of markers is reasonable for the field of single-cell RNA-seq, where marker information is abundant. The Cell Ontology  has used markers for defining cell types, an approach specially employed for immune cells [@doi:10.1186/1471-2105-12-6] .   

The use of markers, however, leaves us with a conceptual problem: definitions of cell type used by electrophysiologists, or even in the manuals of histology classes, are not based on markers. Rigorously, this would leave aside a whole part of what we consider biomedical knowledge. Moreover, gene markers are not defined for cell types that span multiple species, a problem already discussed on the Cell Ontology report of 2011 [@doi:10.1186/1471-2105-12-6]. Multispecies markers would require us to explicitly consider homology, adding an extra layer of confusion. 

My pragmatic definition of cell type (for eukaryotic, multicellular organisms) consists of 3 + 1 simple rules. A cell type is a class of cells that _must_ be:

- Explictly defined
- Theoretically useful 
- Identifiable for a defined taxon


And that _should_ be:

- Logically related to other cell types

For that specification, _must_ represents an "an absolute requirement" and _should_ represents that "there may exist valid reasons in particular circumstances to ignore a particular item" (as per RFC 2119 [@url:https://www.ietf.org/rfc/rfc2119.html])_.

For rule 1, by "explicitly defined", I mean that the cell type needs to be followed by a clear definition, that would allow rational judgements of whether a singular cell belongs or not to the type.  The definition _should_ be complete, providing the necessary and sufficient criteria for classification. An example is a cell type defined by "expression of the proteins CD3 and CD4, but lacking CD8." Even though there is still some ambiguity in that definition (see [@doi:10.1186/s12859-019-2725-5] for a longer discussion), it already states clear, reasonable criteria. Any combination of markers (or lack thereof) can define a different _cell type_. This extends to _any_  definition, and small differences are enough for constituting new cell types. The degree of rigorousness cannot be decided a priori, as we still do not have a rigorous framework for representing biological knowledge, but we _should_ strive to make definitions as rigorous as possibles. Other examples of what could be explicit definitions: 

- A "big cell", defined a class of cells with a length of more than 50 micrometers on any axis.
- A "human cortical neuron" is any cell in a human cortex that is able of producing an action potential.
- A "leukocyte" is a class of achromatic cells found in animal blood.  

The recognition of multiple valid types of rules is not new. The first Cell Ontology article, in 2005, explicitly acknowledged criteria based on function, histology, lineage and ploidy.[@doi:10.1186/gb-2005-6-2-r21]. These features were combined in the definitions of "species-neutral" cell types[@doi:10.1186/s13326-016-0088-7], arguably useful for integrating databases, or for teaching biology. Gradually, we are acknowledging that we might need more specific classes to characterize experimental biology, leading to definition of species-specific types defined by granular characteristics. [@doi:10.1186/s12859-017-1980-6] [@doi:10.1186/1471-2105-12-6].

Rule number 2  is, thus, an explicit criteria that _must_ be followed when talking about cell types scientifically: we need to define the taxons for which a given cell type is expected to manifest. The cell type, then needs to be findable in any individual of the taxon (or taxons) of interest, given the appropriate conditions (e.g. stage of life and biological sex). The set of taxons covered by a cell type is called here a _taxonomy scope_ (or just _scope_) of the cell type. Note that, as cell types can be defined by function, and functions can converge, the taxonomix scope is not restricted to monophyletic taxa ("clades"). The definition of taxon used here is liberal, as any class of organisms that any researcher identify explicitly as a unit. 

Knowing the scope is important to avoid the pitfalls of extrapolation. One recurrent extrapolation is that theories corroborated by mouse experiments are valid for human cells. This extrapolation is an instance of the classic problem of induction, detailed thoroughly in the Logic of Scientific Discovery. A specification of the scope a researcher is referring to would make inductional claims explicit and enable proper evaluation of claims. It is not safe to assume that a "mouse neutrophil" is simply a "neutrophil" that happens to be in a "mouse".  A definition of scope is essential to tease apart general claims from study-specific claims. 

Rule number 3 is a rule of practical concern. There is a massive amount of "explicit definitions" that one scientist might come up with, due to the combinatorial nature of classes, far outnumbering the reported number of atoms in the observable universe. For that reason, a criterion of usefulness is necessary for deciding when a class of cells is considered a cell type. The simplest criteria of usefulness is one based on the individual: a valid cell type is whatever class any individual rationally finds useful. 

Rule number 4 is one practical extension of the "usefulness" rule: a cell type has to be logically anchored to other cell types for increased usefulness. Which means that a definition of a cell class is (for research synthesis concerns) of lower usefulness if it can't be considered a "subclass" of other cell type. For our practical concerns, all imaginable cell types are subclasses of "cell of eukaryotes". This is presented as a recommendation instead of a requirement as, in practice, it might be an overhead not strictly necessary for claims of discovery of new cell types and similar tasks.  

The ontological organization is important for integrating knowledge across studies. A "transcriptomically-defined" cell type and a "electrophysiologically-defined" cell type are not the same,  but they can be grouped in a "superclass" that contains cells that match either one or the other criteria. Practically, when describing a cell type, one should make an effort to insert it into the universe of interrelated cell types, even if that implies creating new "superclasses". 

The consequences of these set of criteria will be discussed further in the following sections. 

# Naming classes of cell types


In parallel to the criteria raised on part 1,I propose a set of naming conventions for different classes of cell types, to facilitate communication. Much of the literature mixes cell types in one species (e.g., when dealing with a cell type as an evolutionary unit) and multispecies (e.g., in the cell ontology). It is arguably useful to distill these different concepts into their own names.. Given the importance of the concept of species in biological classification [@https://en.wikipedia.org/wiki/PhyloCode] [@http://phylonames.org/code/divisions/1/], I derive a "species-centric" view on the naming of classes of cell types. The three classes I propose are: 

- Archetypes, for when the _taxonomic scope_ of the type is beyond the level of species. For example, "mammal neutrophils." 
- _Stricto sensu_ cell types, for when the _taxonomic scope_ of the type corresponds to a single species. For example, "human neutrophils."
- Infratypes, for when the _taxonomic scope_ is below the level of species. For example, considering the mouse strain "C57BL/6J" [@https://www.jax.org/strain/000664], "C57BL/6J neutrophils".

 By adopting a more precise vocabulary, we can flesh out misunderstandings and communicate clearly. At the level of individual scientific experiments, we usually work at the "infratype" level: the samples come only from a subpopulation of the species of interest, and cannot be assumed to be "randomly sampled" from all individuals. This has important practical considerations for, once more, avoiding failing implicitly for the problem of induction. 

In addition, in individual experiments, we work with cells of very specific classes. They are not only infratypes, but very specific infratypes, defined by non-random research setups and pragmatic choices. For example, we might call "CD4 T cells" what are actually CD3+, CD4+, CD8+ cells from the axillary lymph node of 2-month-old chow-fed female C57BL6/J mice from the mouse-house of the Institute of Biochemistry of the University of São Paulo collected in several mornings around 10 pm. Albeit really specific, all the mentioned facets (markers, anatomical location, age, biological sex, strain, housing conditions, circadian clock and diet) are known to alter what we know about cell types. Thus, we benefit from using a name for these very specific classes: 

- Technotype: A specific, experimentally defined cell type, which harbors on its definitions the precise conditions of the cells sampled. 

Even if really specific, a technotype is still a class. Unless a study used only one single-cell, it likely contained some sampling method. Samples are sampled from a specific population, for which hypothesis are actually tested. This is the most "granular' cell type in my pragmatic view for research synthesis. This is the type that can be strictly annotated in single-cell RNA-seq analysis, for example. 

Single claims are made and tested for technotypes, and the claims can be logically combined in "upper" ontological levels for making claims with a higher degree of universality. The propagation of knowledge to upper levels cannot be implicit. (see Yarkoni 2020 for an analogous problem in the psychological sciences [@doi:10.31234/osf.io/jqw35]). As defended by Popper, knowledge should travel "quasi-inductionally" by fostering hypothesis with higher degrees of generality, which can then be tested for the more universal class [@isbn:9788531612503]. 

# Logical consequences of the definition


One notable logical consequence of the proposed set of criteria is that the definition of a "cell state" is left as a subclass for "cell type".  For the pragmatic purpose adopted here, I  avoid dissecting dissection of the differences between persistent classes of cells (which I refer to as "traditional cell types") or the transient, fugacious classes of cells (which I refer to as the "traditional cell state"). Even though such a distinction is an important topic for theoretical research, it is not a requirement for representing biomedical experiments. 

One example of this entailment is that the class "human cells in metaphase of mitosis" can be considered a cell type, as they can be explictly defined and restricted to a taxon. Even though "metaphase" itself is a  biological process, we can describe all cells executing this process as a single cell type. 

However, does a dividing fibroblast stop being a fibroblast, even if temporarily? Again, I do not aim to answer this in a philosophical-ontological sense. Pragmatically, if the explicit definition used for fibroblast (e.g., expression of a marker) still holds during duplication, this cell can be assigned to two disjunct classes: "fibroblasts" and "doubling cells"! It is, thus, essential to consider that cells can belong to at least two disjunct classes. 

 If cells can be assigned to disjunct classes, it is not possible to annotate cell types with a single identifier using a taxonomic tree, in which each concept is represented by a single node with one (and only one) direct parent node. This is conflicting with attempts to classify cell-types using single hierarchies in the form of a tree [@doi:10.1093/nar/gkz543] [@doi:10.7554/eLife.38619] [@doi:10.1146/annurev-cellbio-100616-060818].  Cell types need to be represented ontologically (in the computational sense), which can be thought of multiple, intertwining trees, which take into account different ways of classifying cells. 

Another logical consequence of the definition is that concepts of "subtype" become redundant with "cell type." A "subtype," then, is a concept that only makes sense when talking about classes with different degrees of universality. Thus, claims to discover new cell "subtypes" or "types" differ only stylistically and can be considered indistinguishable in the perspective of research synthesis. 


# Practical consequences of the definition


In the previous section, I discussed the logical entailments of accepting the proposed rules as valid. Here, I will extend the pragmatic considerations on using such a system for real-world applications. 

By using the set of rules, we can better evaluate claims of discover of new cell types. With vast amounts of data and loose definition of cell types, it becomes uncannily easy to claim a new cell type. Converserly, if one explictly claims to discover a new "stricto sensu" cell type, one has to provide enough evidence that cells from this class are identifiable across all individuals of a species. A claim of an "archetype" would require  evidence for existence in more than one species. Consequently, experiments that only use a specific strain of mice can only claim to discover an infratype.

An example of the discovery of a new "archetype" is the pair of articles published in Nature in 2018 [@doi:10.1038/s41586-018-0393-7] [@doi:10.1038/s41586-018-0394-6] about the newly found "ionocyte", a class of cells in the trachea enriched for expression of genes homologous to the _CFTR_ gene. Both studies displayed evidence for such a class in both mouse and human samples, corroborating the existence of an archetype. This discovery of an archetype has been denominated by both articles as a discovery of a new cell type. 

Another example of cell type discovery is a pioneer article by Villani et al [@doi:10.1126/science.aah4573]. It describes subclasses of monocytes and dendritic cells in humans, and pragmatically uses markers for their definition. The patients were recruited from "the Boston-based PhenoGenetic project (...) and the Newcastle community." It is arguable that they did not have a random sample of humanity, and the observed results might not hold for different populations. This discovery of infratypes has also been described as a discovery of a new "cell type". 

An example from the article is the discovery of the  "AS Dendritic cell" (and two subpopulations of it), characterized by expression of the antigens for the proteins AXL and SIGLEC6. This and other cell types are presented in the article  as part of a "Human dendritic cell atlas", generalizing the theory for the whole humanity. However, it is not clear if the population sampled included individuals from different human background. Thus, it is technically possible that the existence of the "cell type" exactly as described might be restricted to some human groups. The jump from technotype (which takes into consideration also descriptors like "healthy" and "age between 25 and 40 years") to infratype ("all humans in this population scope") to cell type _strictu sensu_(all humans) is depicted in the figure @fig:villani and exemplifies the logical flow. 

"Dendritic cells" is one of the cell types most thoroughly modelled by Cell Ontology. [@doi:10.1186/1471-2105-10-70] [@doi:10.1016/j.jbi.2010.01.006]. The current natural language definition of dendritic cell ([CL_0000451](http://purl.obolibrary.org/obo/CL_0000451)) states that a dendritic cell is "A cell of hematopoietic origin, typically resident in particular tissues, specialized in the uptake, processing, and transport of antigens to lymph nodes for the purpose of stimulating an immune response via T cell activation. These cells are lineage negative (CD3-negative, CD19-negative, CD34-negative, and CD56-negative)." The structured definitions are derived from the leukocyte ([CL_0000738](http://purl.obolibrary.org/obo/CL_0000738)) definition, which defines such cells as "achromatic cell of the myeloid or lymphoid lineages capable of ameboid movement." These definitions are not reconcilable to the "dendritic cells" studied by Villani et al's . We have no way of knowing if the cells in their work are "typically resident in particular tissues", "achromatic" or "capable of ameboid movement". That might sound pedantic, but the logical requirements of computational systems leads to both [biocurators](https://www.biocuration.org/community/biocuration-generic-job-description/) and  [computers](https://eloquentjavascript.net/00_intro.html) being seen as pedantic. This high level of precision is necessary to accurately depict not only the complexities of cell types, but the complexities of research settings.


![ Conceptualization of a set of the cell types in Villani et al, 2017 [@doi:10.1126/science.aah4573]. The depicted cell types were manually curated from the article, where they are either implicitly or explicitly mentioned. The set of cell types is not comprehensive, and represent only a small fraction of the concepts handled by the authors. Identifiers for cell types are written in pseudocode based on the Turtle serialization for RDF knowledge graphs (https://www.w3.org/TR/turtle/) and represent valid URIs (described in the database https://celltypes.wiki.opencura.com/wiki/Main_Page). URI: Universal Resource Identifier; RDF: Resource Description Framework.](images/villani_asdcs.png  ){#fig:villani}

Even if we are not yet able to formally represent all the aspects that go into a cell type definition, we can use an explicit "natural language definition" property to define cell types. As David Osumi-Sutherland puts in a 2017 article about cell type classification, there is a "_mismatch between quantified logic, which records assertions about all members of a class, and the messy, noisy reality of biology and the data we collect about it._." [@doi:10.1186/s12859-017-1980-6]. We do not need complex assertions to create a logically valid ontology of cell types. Taking as example in  figure @fig:villani, all cell types treated as "dendritic cells" in the literature are valid subclasses of  the dendritic cell archetype (ct:Q20). Such a subclassing system might lack the power to computationally check the validity of definitions. However, by the principle of minimal commitment [@doi:10.1.1.89.5775], it could already be be a suitable scaffold for representing experimental data (e.g from single-cell transcriptomics) and allow logically robust data integration. 

However, a new problem arises. How to name all these specific cell types? How to humanely understand so many "cell types" with such subtle differences? Which names should we use to differ cells that were selected by slightly different combinations of markers?  

For accurately classifying cell types from the perspective of research synthesis, we need explicit definitions, and they should be as rigorous as possible. This makes the task of finding common names specially hard. I avoid this challenge, focusing on the identification of concepts that are computationally useful. Common names can be agreed in a context by referencing to identifiers, similarly to common names and scientific names of species.  

Sabina Leonelli stated that the challenges brought up by big data in biology require an advance of our philosophical theories [@doi:10.7554/eLife.47381]. I agree, and argue that the inverse is also true: to advance the theoretical foundations of modern biology, we need to harness the power of computational tools. Computational ontologies provide a solution for dealing with complex concepts. Classes in ontologies can have alpha-numeric identifiers. We can, thus assign each technotype a Unique Resource Identifier, a URI, similar to the Cell Ontology (CL) [@doi:10.1186/gb-2005-6-2-r21] [@doi:10.1186/1471-2105-12-6] [@doi:10.1186/s13326-016-0088-7] or Wikidata [@doi:10.7554/eLife.52614] [@https://www.wikidata.org/].The quest for naming cell types becomes simpler when the goal doesn't require human readability at every step. Instead, by harnessing the computer power to record the identifiers and their explicit definitions, we can focus on higher level abstractions

The idea of "technotype" can theoretically solve labeling cell types in single-cell experiments. The non-existence of exact matches in CL (even when combined with other ontologies) renders it theoretically impossible to annotate articles and datasets without incurring in induction issues. The "technotype" avoids that imprecision by giving power to every researcher to craft their "cell type" of interest. As mentioned in the previous section, by having a knowledge connecting the concepts, we would still be able to compare results from different researchers, but now explicitly stating the level of abstraction in which they can be compared.

Specifically, for single-cell transcriptomics, the technotype refines our model for lalbeling cells (and, consequently, cell clusters). A branch of computational single-cell development has dedicated itself to find tools for labeling single-cell experiments. While some approaches ignore ontologies [@doi:10.1093/nar/gkz543] [@doi:10.1101/2020.01.05.895441], others aim at finding the best class among the Cell Ontology [@https://www.bioconductor.org/packages/release/bioc/vignettes/ontoProc/inst/doc/ontoProc.html#conceptual-overview-of-ontology-with-cell-types] or MeSH IDs[@doi:10.1101/2020.05.29.124743] [@doi:10.1038/s41467-020-17281-7]. Manual matches have been fed to algorithms such as BLAST2CO [@doi:10.1038/s41467-020-17281-7] to predict best "matches" for a single-cell cluster. However, unless the cells were sampled in the same way across articles, and drawn at random from the same population of individuals, they represent strictly different classes, even if very similar. Thus, we must change the task from finding a "match" to the cells in a given current experiment to finding a  "point of insertion" in an ontological network. By acknowledging these real differences, we can have precise metadata, enabling precise statements and facilitating valid reuse of publically available data. 


# Final remarks

In this article, I proposed a set of 3 rules (rigorous description, taxon scope restriction, and theoretical usefulness) and 1 recommendation (link to an ontology of cell types) to define cell types.  I  proposed 4 namings to clarify discussions on the topic: archetypes (a class with a scope above species level), _stricto sensu_ cell types (a class with scope equal to  one species), infratypes (a class with scope below the species level) and technotypes (the exact cell type defined for an experimental setup). The concept of the "technotype" can be harnessed as the unit for classifying cells, in an analogous way of how the "species" is the conventional unit for classifying organisms into higher-order taxa. 

 I dissected some logical entailments of such definition, which, admittedly,  might conflict with current views on defining cell types. I do not aim at solving such conflicts but propose a different way of organizing our knowledge about cell types. Of note, 

This article is intended to clarify some of the meanings and provide directions to the future development of the theoretical basis of cell type definition. The discussion on cell types' definition is still on its infancy, and we need human power to tackle the huge theoretical challenges. Biologists, philosophers, and computer scientists ought to distill the details of defining cell types, powering the Human Cell Atlas, and the life sciences research enterprise of this century.  

# Supplementary notes

A set of notes that may be incorporated into the final text, or become appendices, or end up as blog posts somewhere. 

## What to do when two researchers disagree on a definition?

Cell type names are notoriously ambiguous and one definition might collide with an other, specially regarding the natural language name used to described. There are many different, equally valid definitions of a "dendritic cell." I do not aim to solve this problem from a societal standpoint. However, from a computational-ontology standpoint, there is one simple solution: split the concept. 

This approach is similar to King Solomon's solution in a famous bible story, called the [Judgement of Solomon](https://en.wikipedia.org/wiki/Judgment_of_Solomon). In a dispute between two women that claimed to be the mothers of a child, the solution of the king was simple: split the baby. However, babies are notoriously indivisible, and the true mother did not really like the idea. 

It may be that some scientists are attached to their names, as mothers are to their babies. However, unlike babies, namings can be divided. Each of the scientists gets to name their specific conceptualization however they choose. Many names might "collide" in that way, and that is okay. Under the hood, however, the names refer to different identifiers. Computationally there would be no ambiguity. Then, it is just a matter of the researcher to respect the choice of their peers of calling something by the _wrong_ name, as long as the identifier is correct.


Splitting concepts upon conflicts in the end is more the multiplication of bread and fish in the [Feeding the multitude](https://en.wikipedia.org/wiki/Feeding_the_multitude) episode, and everyone gets to eat.


But ontologies are different from ordinary babies and magical fish. The splitting of concepts would not only create new concepts, but leave a trace. They would be immediate subclasses of their conjunction. An equally valid superclass that can be defined by "a cell containing characteristics of any of their subclasses".

In a parallel with text-book mitosis, the concept gets divided in two new, equally real concepts. And as we can trace cells in an animal to a single zygote, we can keep track of concepts while they keep dividing, whenever a new conflict pops up.   


## The big assumption of continuity in time

One assumption that underlies the validity of the models proposed here is that taxons preserve their characteristics throughout time. 

In Popper's Logic of Scientific Research, he states that he has a metaphysical faith on the continuity of laws of nature through time. 

We have no way of testing this metaphysical faith, and it is absolutely necessary for the scientific endeavour as we understand. 

While in physics this assumption seems to be reasonable, evolution makes biology quite more complicated. Statements that we have about the human species, for example, might be valid today, but were not valid 2000 years ago, and vice-versa. 

When I talk about sub-species taxons, which might be a local population of a town, for example, this unit is not immutable. The population of Newcastle, as per the example, might change in time, with imigration and emigration, mutation, natural selection, neutral evolution and the many forms of modifications of a gene pool. 

It is, thus, and heuristic, to call "population of Newcastle" a class. We could specify a period in time for which we expect the information to be valid. For example, we may say we are sampling from "the Newcastle population in the years 2019-2020." This would be a valid statement, but it would not be falsifiable, as by 1st of January 2021, no independent tests of the theory can be done. 

It is technically possible to have a technotype so precise as to have a scope with a time constraint. In fact, that might be the right way of representing information, if we want to compare experiments done in evolving populations.

While evolutionary definitions take this dimension into account, they are fit to theoretical research, but still lack the rigour for explaining real world experiments.

All research that uses human samples are subject to strong influence of time. I started this as a note, but it is so important that I'll have to add to the main text. 


## Clusters are not cells 

In the era of large-scale omics, we are starting to see declarations of cell types that are not based on pre-selected criteria, but derived from unsupervised clustering followed by labelling.

This is a powerful exploratory approach, which, as mentioned in the main text, has led to discoveries of ionocytes and new classes of dendritic cells, for example. 

Many algorithms and "expert-based" annotation protocols focus on labeling _clusters_ instead of labeling _cells_. 

Cells in a cluster are arbitrarily similar (as determined by the clustering algorithm) and so they will, by definition, differ from other cells in the sample.

For single-cell RNA-seq, one usually checks which genes are differentially expressed when comparing the cells in a cluster with cells in other clusters. These genes are called "markers" and used for labeling a cell cluster. 

What does it mean to label a cell cluster, though? Does it mean that _all_ cells there conform to the cell type? Does it mean that _most_ cells there conform to the cell type? Does it mean that cells from other clusters in the dataset _definitely do not_ conform to the cell type? 

So far, I haven't seem a clear, explicit, coherent definition for a cluster label. Not even once. 

Marker-based definitions are assumed for the group as a whole, but in current pipelines, nothing blocks one cell in a cluster to lack the expression of a "name-giver" marker. 

The classification scheme proposed here works to classify _cells_, but is not sufficient for labeling unsupervisedly-defined _cell clusters_. 

What is possible, though, is to use clustering for data exploration. From then on, strict patterns can be decided (ex: a cell that expresses A and B, but not C) and then apply this pattern to the whole dataset. For clusters with consistent markers, this approach should be roughly equivalent to the previously described. 

Using such "regular expressions" might lead to a cell being assigned to multiple clusters. Even if we assume that the sample is free of doublets, that cannot be a problem. Cells may have multiple functions. As argued in the main text, each cell can be labeled by multiple standards.

We may avoid multiple labeling if we really need in practice, though, and make preferential claims (if a  cell matches defintiions X and Y, it is assigned only to X, for example). 

By having explicit "regular expression" patterns for cell definitions in single-cell datasets, the "cell-type assesment" problem becomes trivial: a cell in  a new dataset is of the _exact_ same type if (and only if) it matches the _exact_ definition.

When that is not the case, current algorithms for reconciling single cell datasets can still be successfully employed. But instead of propagating a label, it would propagate a parent class, looking for cells of a similar, sister class. 


# Additional notes 

The   Immune Epitope Database and Analysis Resource (IEDB)  announced it in 2006  [doi:10.1371/journal.pcbi.0020125]: 

"the goal of the IEDB is to present as much information as possible without subjective interpretation, we can never presume any information, but rather we must try to capture the data exactly as presented in the reference, while maintaining the conclusions of the reference in a uniform manner. For example, if all experiments are performed with a whole cell population, but the authors attribute the response to a particular cell type without any evidence, we must capture the effector cells as the entire population."

That is the kind of challenge that the "technotype" solves in theory, as it gets the objective population sampled in any article. 





## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>