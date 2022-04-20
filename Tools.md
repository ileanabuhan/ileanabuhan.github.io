---
layout: page
title: Tools
permalink: /Tools/
---


The goal of this page is to provide a quick overview of the available tool to aid securing cryptographic implementations against physical attacks. If a relevant tool is missing from this page, please contact me and I will add it. 

**Pre-silicon side-channel leakage simulators**


| -------- | ------- | ---------  | ----------- | ---------| ------- | ------- | ------- | 

|**Name**| **Year**|**Abstraction**|**Target**|**Detect** |**Verify**|**Mitigate** |**Link** to repo|
|[MAPS](https://link.springer.com/chapter/10.1007/978-3-319-89641-0_5)      | 2018    | ISA        | ARM Cortex M3|  yes     |         |         |         |         
|[AMASIVE](https://link.springer.com/chapter/10.1007/978-3-642-42001-6_12)   | 2013    | RTL        |      -      |  yes     |         |         |         |         
|[RT-PSC](https://jin.ece.ufl.edu/papers/VTS19.pdf)    | 2019    | RTL        |AES-GF, AES_LUT|yes     |         |         |         | 
|[NCSIM](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.113.638&rep=rep1&type=pdf)     | 2007    | gate       | CARD         |  yes     |         |         |         |         
|[PARAM](https://arxiv.org/abs/1911.08813)     | 2020    | gate       |RISC-V(ShaktiC)|yes     |         |         |         |         
|[ACA](https://eprint.iacr.org/2020/1192)       | 2020    | gate       |RISC-V(LEON3)|  yes     |         |         |         | 
|[SCRIPT](https://dl.acm.org/doi/10.1145/3383445)    | 2020    | gate       |AES-GF, AES_LUT|yes     |     yes    |         |    n.a.   | 
|[CASCADE](https://www.esat.kuleuven.be/cosic/publications/article-3204.pdf)   | 2020    | gate       |ASIC(custom) |  yes     |         |         |         | 
|[Patch](https://link.springer.com/article/10.1007/s11227-021-03927-w)     | 2021    | gate       |      -      |  yes     |     yes    |     yes    |    n.a.     | 
|[COCO](https://pure.tugraz.at/ws/portalfiles/portal/30823144/main.pdf)      | 2021    | gate       |RISC-V ([IBEX](https://github.com/lowRISC/ibex))|  yes     |    yes     |         | [link](https://github.com/IAIK/coco-ibex)      |
|[KARNA](https://ieeexplore.ieee.org/document/8942173)     |2019     | layout     |AES , SIMON  |  yes| yes |yes|n.a.|

