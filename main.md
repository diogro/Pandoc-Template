---
title: Super serious manuscript on imporant science
version: "0.1"
author:
  - Diogo Melo:
      institute: 
        - usp
      email: damelo@ib.usp.br
      orcid: 0000-0002-7603-0092
      correspondence: "yes"
      initial: DM
institute:
  - usp:
      name: "Departamento de Genética e Biologia Evolutiva, Instituto de Biociências, Universidade de São Paulo, São Paulo, SP, Brasil"
output: pdf_document
indent: false
geometry:
- top=20mm
- left=25mm
- right=25mm
- bottom=20mm
header-includes:
- \usepackage{indentfirst}
- \setlength\parindent{24pt}
- \usepackage[left]{lineno}
- \modulolinenumbers[1]
- \usepackage{multicol}
- \usepackage{setspace}
- \usepackage{float}
- \usepackage{afterpage}
- \usepackage{stfloats}
- \usepackage{graphicx}
- \newcommand{\hideFromPandoc}[1]{#1}
- \hideFromPandoc{ \let\Begin\begin \let\End\end}
- \usepackage[labelfont=bf]{caption}
- \captionsetup{labelfont=bf}
- \usepackage{amsmath}
- \DeclareMathOperator\arctanh{arctanh}
link-citations: yes
figureTitle: "Fig"
figPrefix:
  - "Fig"
  - "Figs"
mainfont: Skolar PE
sansfont: Skolar Sans PE
titlefont: Skolar Sans PE
sectionfont: Skolar Sans PE
mainfontoptions:
- Numbers=Lowercase
- Numbers=Proportional
csl: ./pandoc/plos.csl
bibliography: ['./references.bib']
keywords: [modularity, gene co-expression, WGCNA, MMC, clustering, RNA-seq, GO enrichment]
---

\normalsize
# Abstract
Evolutio genetica lorem ipsum dolor sit amet, consectetur adipiscing elit. Mutatio DNA in populationes per tempus, selectio naturalis adaptationesque. Hereditatem traits per generationes, geni fluxus in ecosystemata. Variatio alleles frequentia, fitness reproductiva in ambientia. 
Genomica comparativa revelavit homologiam inter species, demonstrans communem originem. Epigenetica regulatio gene expressione sine mutatione sequentiae DNA. Speciatio et divergentia per isolationem reproductivam, accumulatio differentiarum geneticarum.
Molecularis horologia evolutionis, fossilia DNA ex speciminibus antiquis. Horizontalis gene translatio inter bacterias, archaeas, et eucaryotas. Coevolutio inter species symbioticas, Red Queen hypothesis in arms race genetica.
Pleiotropy, epistasis, et gene-environment interactiones in phenotypica expressione. Neutral theory molecularis evolutionis, genetic drift in populationes parvas. Balancing selectio et frequentia-dependens selectio in polymorphismi conservatione.
Evolutio convergenta in traits similibus inter lineas non-related. Evolutio reticula in plantis et bacteriis per hybridisationem et horizontalem gene translationem. Evo-devo explorat genes regulatorias in evolutione morphologica.
Metagenomics revelat diversitatem microbialem incognitam in ecosystematis. Evolutio resistentiae ad medicamenta in pathogenis et cancer cellulis. Genomica populationis et phylogeographia in historia migrationum reconstruction.

\newpage

# Introduction

\linenumbers
\doublespacing

Evolutio biologica fundamentum scientiae vitae, explicans diversitatem specierum et adaptationem ad ambientem. Genetica, mechanismus hereditatis, central rola in processu evolutionis jocat. Darwin's theoria selectionis naturalis et Mendel's leges hereditatis fundamenta moderna syntheseos evolutionis posuerunt. Investigationes recentae in genomica et biologia moleculari nova luce in processus evolutionis effundunt.

Populationes evolutione per tempus mutantur, influentia selectionis naturalis, genetic drift, et fluxus genorum. Variatio genetica in populationibus materia prima evolutionis est, oriens ex mutationibus, recombinationibus, et migrationibus. Adaptatio ad pressionem ambientalem per selectionem naturalem fit, ubi individua cum traits advantageis maiorem succesorum reproductionis habent. @Lande1979-jl demonstravit quomodo selectio multivariata in correlatas characteres evolutionem phenotypicam populationum influat.

Moderna syntheseos evolutionis integrat conceptus ex genetica populationum, paleontologia, systematica, et ecologia evolutionaria. Conceptus claves includunt speciationem, coevolutionem, et evolutionem molecularem. Evolutio non solum in morphologia et physiologia, sed etiam in comportamento et ecological interactionibus observatur. Investigationes in evo-devo explorant quomodo mutationes in genes regulatorias magnas mutationes evolutionarias causare possint.

# Methods

Investigatio haec methodologiam sequentem adhibuit ad analysandum evolutionem geneticam in populationibus Drosophila melanogaster:

1. Collectio speciminum: Drosophilae ex quinque locis geographicis diversis collectae sunt, utendo esca fructuum fermentatorum. Minimum 100 individua per locum collecta sunt.

2. Extractio DNA: Genomicum DNA ex singulis muscis extractum est utendo protocollo phenol-chloroform modificatione @Smith_et_al_2020.

3. Sequentiatio genomica: Bibliothecae DNA praeparatae sunt utendo Illumina TruSeq kit et sequentiatae in Illumina NovaSeq 6000, cum 150bp paired-end reads.

4. Analysis bioinformatica: Sequentiae raw processae sunt utendo pipeline customed in environment Linux. Reads qualitate filtratae sunt cum FastQC, alignatae ad genomam referentiae D. melanogaster (release 6) utendo BWA-MEM, et variantes appellatae sunt utendo GATK HaplotypeCaller.

5. Analysis populationis geneticae: Structura populationis et diversitas genetica evaluatae sunt utendo R packetis adegenet et hierfstat. Selectio naturalis investigata est utendo tests neutralitatis et scans genomicos pro signaturis selectionis.

Parametri sequentiationis et analysis summarizati sunt in Tabula 1.

| Parametrus | Valor |
|------------|-------|
| Read length | 150 bp |
| Coverage medio | 30X |
| Q30 percentage | >80% |
| Mapping rate | >95% |
| SNP calling threshold | QUAL>30 |
| Minimum allele frequency | 0.01 |

Table: Parametri sequentiationis et analysis genomici. Valori repraesentant media acros omnia specimina (n=500). {#tbl:seqparams}

Analysis statisticae perfectae sunt utendo R (v4.1.0) @R_Core_Team_2021. Significantia statistica determinata est ad p < 0.05 pro omnibus testibus. Visualisationes datorum creatae sunt utendo ggplot2 packetum in R @Wickham_2016.

# Results

Analysis genomica populationum Drosophila melanogaster ex quinque locis geographicis diversis revelavit structuram geneticam significantem et signaturas selectionis.

## Diversitas genetica et structura populationis

Diversitas nucleotidica (π) variavit inter populationes, cum valoribus a 0.0042 in populatione boreali ad 0.0068 in populatione tropicali (Tabula 2). Analysis componentium principalium (PCA) genomicorum datorum demonstravit claram separationem inter populationes (@fig:pca), cum primis duobus componentibus explicantibus 37.2% et 18.5% variationis, respective.

## Signa selectionis

Scans genomici pro signaturis selectionis identificaverunt regiones multiples sub selectione positiva. Notabiliter, geni implicati in resistentia ad pesticidas (e.g., Cyp6g1) et tolerantia thermica (e.g., Hsp70) demonstraverunt signa fortes selectionis in populationibus ex regionibus agricolis et calidis, respective.

Test Tajima's D revelavit patrones non-neutrales evolutionis in 12.3% genomae, cum valoribus significanter negativis in regionibus contentibus genos adaptivos cognitos.

## Fluxus genorum et isolatio per distantiam

Analysis fluxus genorum inter populationes demonstravit correlationem negativam significantem inter distantiam geographicam et similitudinem geneticam (r = -0.78, p < 0.001), indicans patronem isolation is per distantiam.

![Analysis Componentium Principalium (PCA) genomicorum datorum ex quinque populationibus Drosophila melanogaster. Puncta repraesentant individua singula, colores indicant populationes originis. Axes demonstrant primos duos componentes principales (PC1 et PC2) cum proportione variationis explicatae in parenthesibus. Ellipses indicant intervalla confidentiae 95% pro quaque populatione. Separatio clara inter gruppos geographicos observatur, cum populationibus vicinis propioribus in spatio PCA.](./figures/placeholder_image.png){#fig:pca height=10cm}

@fig:pca demonstrat structuram geneticam claram inter populationes studitas. Populationes ex regionibus geographicis similibus (e.g., tropicales vs. temperatae) tendunt ad clusterizationem, suggerens adaptationem localem ad conditiones ambientales diversas. Separatio maxima observatur inter populationes maxime distantes geographice, congruens cum hypothesi isolationis per distantiam.

# Discussion

Investigatio nostra genomica populationum Drosophila melanogaster ex quinque locis geographicis diversis revelavit insights significantes in patterns evolutionis adaptivae et structurae populationis. Resultati nostri demonstrant rrolam centralem selectionis naturalis in formatione diversitatis geneticae, simulac effectus importantes historiis demographicae et fluxus genorum.

### Structura populationis et historia demographica

Analysis componentium principalium (PCA) demonstravit separationem claram inter populationes studitas, indicans differentiam geneticam significantem. Hoc pattern congruens est cum studiis prioribus in D. melanogaster quae demonstraverunt structurationem geneticam fortam inter populationes geographice distantes (Johnson et al., 2018). Correlatio negativa inter similitudinem geneticam et distantiam geographicam supportat modelum isolationis per distantiam, suggerens quod fluxus genorum limitatus est inter populationes remotas.

Diversitas nucleotidica maior in populationibus tropicalibus comparata cum populationibus temperatis potest reflectere originem Africanam speciei (Li & Stephan, 2006). Alternativiter, hoc pattern posset resultare ex populationibus maioribus et stabilioribus in climatibus tropicalibus, permittens accumulationem maiorem variationis geneticae.

### Signa selectionis et adaptatio localis

Identificatio regionum genomicarum sub selectione positiva, praesertim genorum implicatorum in resistentia ad pesticidas et tolerantia thermica, providet evidentiam fortem pro adaptatione locali in responsu ad pressiones selectivas specificas ambientis. Selectio fortis in geno Cyp6g1 in populationibus ex regionibus agricolis consonat cum studiis prioribus demonstrantibus rolam huius geni in resistentia ad insecticidas (Schmidt et al., 2010).

Similiter, signa selectionis in genibus familiae Hsp70 in populationibus ex regionibus calidis supportant hypothesim quod tolerantia thermica est trait adaptivus clavus in D. melanogaster. Hoc concordat cum studiis experimentalibus demonstrantibus augmentationem expressionis Hsp70 in responsu ad stressum thermicum (Feder & Hofmann, 1999).

### Implicationes pro conservatione et evolutione futura

Resultati nostri habent implicationes importantes pro conservatione et praedictione responsorum evolutivorum ad mutationes ambientales futuras. Structura populationis observata suggerit quod populationes locales possunt habere adaptationes unicas ad conditiones suas specificas. Hoc emphasizat importantiam conservationis non solum speciei in toto, sed etiam diversitatis geneticae intra et inter populationes.

Praeterea, evidentia pro adaptatione rapidae ad pressiones selectivas anthropogenicas (e.g., usum pesticidorum) demonstrat potentiale D. melanogaster ad adaptandum ad mutationes ambientales. Tamen, haec adaptabilitas potest esse limitata in populationibus cum diversitate genetica reducta, ut observatum in quibusdam populationibus temperatis nostris.

### Limitationes et directiones futurae

Dum studium nostrum providet insights valorosas in evolutionem adaptivam D. melanogaster, limitationes quaedam notandae sunt. Primo, sampling noster geographicus, etsi extensus, non est exhaustivus. Inclusion populationum additionarum, praesertim ex regionibus intermediis, posset providere imaginem magis completam structurae geneticae et historiae evolutionis speciei.

Secundo, dum identificavimus regiones genomicas sub selectione, characterizatio functionalis mutationum specificarum responsabilium pro adaptatione observata remanet tema pro investigatione futura. Studia expressione genorum et analyses experimentalis functionum phenotypicarum variantium geneticorum identificatorum essent proximi passus logici.

In conclusione, studium nostrum demonstrat complexitatem forces evolutivorum operantium in populationibus naturalibus D. melanogaster. Combinatio approaches genomicorum cum studies ecologicis et functionalis promittit ad illuminandas subtilitates adaptionis et evolutionis in this specie modali importantes.

## Supporting information

Supporting information can be found at [https://github.com/diogro/Pandoc-Tamplate](https://github.com/diogro/Pandoc-Tamplate). 

1. SI Data 1 -- Raw data

2. SI Figure 1 -- SI results

3. SI table 1 -- SI tables

# Author Contributions

**Conceptualization**: D.M. 
**Data Curation**: D.M.
**Formal Analysis**: D.M.
**Funding Acquisition**: D.M.
**Investigation**: D.M.
**Methodology**: D.M.
**Project Administration**: D.M.
**Resources**: D.M.
**Software**: D.M.
**Supervision**: D.M.
**Validation**: D.M.
**Visualization**: D.M.
**Writing – Original Draft Preparation**: D.M.
**Writing – Review & Editing**:	D.M.

# Acknowledgments

We thank all members of the Systems Biology, Genetics and Evolution Lab for their support. We thank Monique Simon and Cara Weisman for their thoughtful comments on an earlier version of the manuscript. 


# References

