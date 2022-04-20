---
layout: page
title: Tools
permalink: /Tools/
---


The goal of this page is to provide a quick overview of the available tool to aid securing cryptographic implementations against physical attacks. If a relevant tool is missing from this page, please contact me and I will add it. 


**EM side-channelleakage simulators**

**Post-silicon side-channel leakage simulators (power)**

|**Name**      | **Year**|**Leakage Model**|**Target**|**Function** |**Repo**|
|[ABBY](https://link.springer.com/chapter/10.1007/978-3-319-89641-0_5)    | 2022    | gray        | ARM Cortex-M0|  Detect     |   [link](https://github.com/cryptolu/maps)|       
|[ROSITA++](https://link.springer.com/chapter/10.1007/978-3-319-89641-0_5)| 2021    | gray        | ARM Cortex-M0|  Mitigate (2-order)|   [link](https://github.com/cryptolu/maps)|         
|[ROSITA](https://link.springer.com/chapter/10.1007/978-3-642-42001-6_12)  | 2021    | gray        | ARM Cortex-M0|  Mitigate (1-order)|      n.a. |  
|[ELMO](https://jin.ece.ufl.edu/papers/VTS19.pdf)    | 2017    | gray        | ARM Cortex-M0|  Detect     |  n.a.     |         
|[ASCOLD](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.113.638&rep=rep1&type=pdf)  | 2017    | gray        | ATMega163    | Detect     |         |              
|[SAVRASCA](https://arxiv.org/abs/1911.08813)| 2017    | gray        | ATMega163    |   n.a.      |         
|[Reparaz](https://eprint.iacr.org/2020/1192) | 2016    | black       | software     | Detect|    n.a.     |         
|[SLEAK](https://dl.acm.org/doi/10.1145/3383445)   | 2014    | black       | ARM Cortex-A8| [AES_LUT](http://satoh.cs.uec.ac.
jp/SAKURA/hardware/SAKURA-G.html)|Verify   |   n.a.  |       
|[SILK](https://www.esat.kuleuven.be/cosic/publications/article-3204.pdf)    | 2014    | black       | ATMega328P   |  Detect     |    link     |         
|[Gagnerot](https://link.springer.com/article/10.1007/s11227-021-03927-w)| 2013    | black       | RISC-V(not specified|  Mitigate   |     n.a.  |
|[Debande](https://pure.tugraz.at/ws/portalfiles/portal/30823144/main.pdf) | 2012    | gray        |not specified| Verify |[link](https://github.com/IAIK/coco-ibex)      |
|[Oscar](https://ieeexplore.ieee.org/document/8942173)   | 2009    | black       |AT90XX,ATMegaXX | Mitigate| n.a.|
|[InspectorSCA](https://ieeexplore.ieee.org/document/8942173)|2007 | black       |software | Mitigate| n.a.|
|[PINPAS](https://ieeexplore.ieee.org/document/8942173)     |2003  | black       |smartcards  | Mitigate| n.a.|

**Pre-silicon side-channel leakage simulators (power)**

|**Name**        | **Year**|**Abstraction**|**Target**    |**Function** |**Repo**|
|[MAPS](https://link.springer.com/chapter/10.1007/978-3-319-89641-0_5)      | 2018    | ISA          | ARM Cortex M3|  Detect     |   [link](https://github.com/cryptolu/maps)|         
|[AMASIVE](https://link.springer.com/chapter/10.1007/978-3-642-42001-6_12)   | 2013    | RTL          |      -       |  Detect     |      n.a.   |  
|[RT-PSC](https://jin.ece.ufl.edu/papers/VTS19.pdf)    | 2019    | RTL          |[AES-GF](http://www.aoki.
ecei.tohoku.ac.jp/crypto/web/cores.html), [AES_LUT](http://satoh.cs.uec.ac.
jp/SAKURA/hardware/SAKURA-G.html)| Detect       |  n.a.     |         
|[NCSIM](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.113.638&rep=rep1&type=pdf)     | 2007    | gate         | [SCARD](https://cordis.europa.eu/project/id/507270)  | Detect     | Detect        |              
|[PARAM](https://arxiv.org/abs/1911.08813)     | 2020    | gate         |RISC-V(ShaktiC)             | Verify     |   n.a.      |         
|[ACA](https://eprint.iacr.org/2020/1192)       | 2020    | gate         |RISC-V(LEON3)               | Detect|    n.a.     |         
|[SCRIPT](https://dl.acm.org/doi/10.1145/3383445)    | 2020    | gate         |[AES-GF](http://www.aoki.
ecei.tohoku.ac.jp/crypto/web/cores.html), [AES_LUT](http://satoh.cs.uec.ac.
jp/SAKURA/hardware/SAKURA-G.html)|  Verify   |   n.a.  |       
|[CASCADE](https://www.esat.kuleuven.be/cosic/publications/article-3204.pdf)   | 2020    | gate         |ASIC(custom)                |  Detect     |    link     |         
|[Patch](https://link.springer.com/article/10.1007/s11227-021-03927-w)     | 2021    | gate         |    AES                     |  Mitigate   |     n.a.  |
|[COCO](https://pure.tugraz.at/ws/portalfiles/portal/30823144/main.pdf)      | 2021    | gate         |RISC-V ([IBEX](https://github.com/lowRISC/ibex))| Verify |[link](https://github.com/IAIK/coco-ibex)      |
|[KARNA](https://ieeexplore.ieee.org/document/8942173)     |2019     | layout       |AES , SIMON  | Mitigate| n.a.|
