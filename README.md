# plink2R_for_win

## 简介：

plink2R_for_win是一个R包，只用于安装到windows系统的R语言中，是专门用于读取PLINK (http://pngu.mgh.harvard.edu/~purcell/plink)格式的文件.bed/.bim/.fam文件到R，我改造这个包主要是配合我的另一个R包：friendly2MRPro中的TWAS分析（[FUSION](https://github.com/gusevlab/fusion_twas/)）模块。

## 来源：

plink2R_for_win包是在[gabraham](https://github.com/gabraham)/[plink2R](https://github.com/gabraham/plink2R)包的基础上改造而来，改造过程参考了该链接：[installing the package. · Issue #1 · gabraham/plink2R (github.com)](https://github.com/gabraham/plink2R/issues/1#issuecomment-1337177621)

## 下载：

```R
if (!requireNamespace("remotes", quietly = TRUE))install.packages("remotes")
if (!requireNamespace("plink2R", quietly = TRUE))remotes::install_github("xiechengyong123/plink2R_for_win/plink2R")
library(plink2R)
```

## [原文参考：](https://github.com/gabraham/plink2R)

plink2R natively reads PLINK (http://pngu.mgh.harvard.edu/~purcell/plink)
BED/BIM/FAM files into R.

Missing genotypes are imputed by assigning missing values the per-SNP average.

Depends on Rcpp, RcppEigen

Example:

```R
   library(plink2R)
   dat <- read_plink("data")
   dim(dat$bed)
   dim(dat$fam)
   dim(dat$bim)
```

Also see the file plink2.R for an example.

If there are missing genotypes, these will by default be assigned as NA. To do
simple imputation of missing genotypes (for each SNP, randomly assigning to
the missing genotypes values sampled proportionally to the non-missing
genotypes in the SNP), use `read_plink("data", impute="random")`.

## 欢迎联系交流：

微信：shengxinxiedaoren
