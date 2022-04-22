---
layout: page
title: Tools
permalink: /Tools/
---

A quick overview of  available tools for aid in securing cryptographic implementations against *physical side-channel attacks*. A detailed analysis of the tools listed below can be found in our [paper](https://eprint.iacr.org/2021/497) **SoK: Design Tools for Side-Channel-Aware Implementations** authored with *Lejla Batina, Patrick Schaumont and Yuval Yarom*, which will appear at ASIACCS 2022.

**Post-silicon side-channel leakage emulators (power)**
The list is ordered by publication year.

|**Name**      | **Year**|**Leakage Model**|**Target**|**Function** |
|:--------------|:-------|:------|:--------------|:--------------|
|[ABBY](https://eprint.iacr.org/2021/1569)    | 2022    | gray        | ARM Cortex-M0| Detect     |
|[ROSITA++](https://eprint.iacr.org/2021/1181), [**repo**](https://github.com/0xADE1A1DE/Rositaplusplus)| 2021    | gray        | ARM Cortex-M0| Mitigate (high order)|
|[ROSITA](https://eprint.iacr.org/2019/1445), [**repo**](https://github.com/0xADE1A1DE/Rosita)  | 2021    | gray        | ARM Cortex-M0| Mitigate (1-order)|
|[ELMO](https://eprint.iacr.org/2016/517), [**repo**](https://github.com/sca-research/ELMO)   | 2017    | gray        | ARM Cortex-M0| Detect     |
|[ASCOLD](https://eprint.iacr.org/2017/345), [**repo**](https://github.com/nikita-veshchikov/ascold) | 2017    | gray        | ATMega163    | Detect     |
|[SAVRASCA](https://ieeexplore.ieee.org/document/7961951), [**repo**](https://github.com/nikita-veshchikov/savrasca)| 2017    | gray        | ATMega163    | Verify    |
|[Reparaz](https://www.iacr.org/archive/fse2016/97830195/97830195.pdf) | 2016    | black       | software     | Detect|
|[SLEAK](https://www.mitre.org/publications/technical-papers/sleak-a-side-channel-leakage-evaluator-and-analysis-kit)|2014   | black | ARM Cortex-A8 | Verify |
|[SILK](https://dl.acm.org/doi/10.1145/2689702.2689706), [**repo**](https://github.com/nikita-veshchikov/silk)|2014   | black  |ATMega328P|Detect|
|[Gagnerot](http://aurore.unilim.fr/ori-oai-search/notice/view/unilim-ori-59315)    | 2013 |     black  | RISC-V(not specified) |  Verify  |
|[Debande](https://eprint.iacr.org/2012/703.pdf) | 2012    | gray        |not specified| Verify |
|[Oscar](https://dl.acm.org/doi/10.1109/CSE.2009.119)  | 2009    | black       |AT90XX,ATMegaXX | Verify |
|[InspectorSCA](https://www.riscure.com/security-tools/inspector-sca)|2007 | black       |software | Verify |
|[PINPAS](https://research.utwente.nl/en/publications/pinpas-a-tool-for-power-analysis-of-smartcards)     |2003  | black       |smartcards  | Verify |

**EM side-channel leakage emulation**


|**Name**      | **Year**|**Leakage Model**|**Target**|**Function** |
|:--------------|:-------|:------|:--------------|:--------------|
|[EMSIM](https://ieeexplore.ieee.org/document/9065440)    | 2020    | white        | Risc-V(custom)| Detect     |

**Pre-silicon side-channel leakage emulators (power)**
The list of tools is ordered according to the design abstraction level. 

|**Name**        | **Year**|**Abstraction**|**Target**    |**Function** |
|:--------------|:---------|:-----------|:--------------|:--------------|
|[MAPS](https://link.springer.com/chapter/10.1007/978-3-319-89641-0_5), [**repo**](https://github.com/cryptolu/maps)      | 2018    | ISA          | ARM Cortex M3              |  Detect     |
|[AMASIVE](https://link.springer.com/chapter/10.1007/978-3-642-42001-6_12)   | 2013    | RTL          |      -                     |  Detect     |
|[RT-PSC](https://jin.ece.ufl.edu/papers/VTS19.pdf)    | 2019    | RTL          |[AES-GF](http://www.aoki.ecei.tohoku.ac.jp/crypto/web/cores.html),  [AES_LUT](http://satoh.cs.uec.ac.jp/SAKURA/hardware/SAKURA-G.html)|Detect|
|[NCSIM](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.113.638&rep=rep1&type=pdf)|2007|gate|[SCARD](https://cordis.europa.eu/project/id/507270)|Detect|
|[CASCADE](https://www.esat.kuleuven.be/cosic/publications/article-3204.pdf), [**repo**](https://github.com/dsijacic/CASCADE)| 2020   |  gate |ASIC(custom)|Detect|
| [Patch](https://link.springer.com/article/10.1007/s11227-021-03927-w) | 2021 | gate     | AES                               | Mitigate |
|[PARAM](https://arxiv.org/abs/1911.08813)     | 2020    | gate         |RISC-V(ShaktiC)             | Verify     |
|[ACA](https://eprint.iacr.org/2020/1192)       | 2020    | gate         |RISC-V(LEON3)               | Detect|
|[SCRIPT](https://dl.acm.org/doi/10.1145/3383445)    | 2020    | gate         |[AES-GF](http://www.aoki.ecei.tohoku.ac.jp/crypto/web/cores.html), [AES_LUT](http://satoh.cs.uec.ac.jp/SAKURA/hardware/SAKURA-G.html)| Verify       |
| [COCO](https://pure.tugraz.at/ws/portalfiles/portal/30823144/main.pdf) |2021|gate|RISC-V ([IBEX](https://github.com/lowRISC/ibex))|Verify|
|[COCOALMA](https://graz.pure.elsevier.com/en/publications/cocoalma-a-versatile-masking-verifier), [**repo**](https://github.com/IAIK/coco-alma)| 2021 | Tab |Tab|Tab|
|[KARNA](https://ieeexplore.ieee.org/document/8942173)   | 2019 | layout   |AES , SIMON                | Mitigate |

