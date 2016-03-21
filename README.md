# Bdelloid genomes project
Scripts and pipelines for the bdelloid genomes project

## 1. Data QC
### 1.1 Adapter and quality trimming
Use skewer for trimming adapter sequences and for removal of low quality bases from reads:
```
~/bin/skewer \
-x adapters.fa \
-m pe \
-q 25 \
-Q 25 \
-e \
-l 36 \
-L 148 \
-n \
-o Rmag \
-z \
-t 32 \
Rmag_1.raw.fq.gz \
Rmag_2.raw.fq.gz
```
Minimum quality score set to 25 (equivalent to about 3 errors per kb).

#### Data counts
Library | Reads pre | Reads post | Bases pre | Bases post | % retained
---|---|---|---|---|---
Rmag | 324,285,548 | 305,771,780 | 48,711,622,622 | 45,639,584,412 | 94.3%
Rmac |  |  |  |  |
Rsoc |  |  |  |  |
Rsor |  |  |  |  |
Rtar |  |  |  |  |
