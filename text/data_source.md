# 数据来源

&emsp;&emsp;本项目使用的数据来自于RNA STRAND数据库和RCSB PDB数据库。前者提供RNA的二级结构信息(ct文件)和二级结构分析信息(txt文件)，后者提供RNA的一级序列信息(fasta文件)和三维结构信息(pdb文件)。下面分别就如何从这两个数据库中获取数据做简要介绍。

***
## RNA STRAND数据库
### Link

* [RNA STRAND](http://www.rnasoft.ca/strand/)

### Introduction

RNA STRAND contains known RNA secondary structures of any type and organism. The ultimate goal of this database is to incorporate a comprehensive collection of known RNA secondary structures, and to provide the scientific community with simple yet powerful ways of analysing, searching and updating the proposed database.

### Download
&emsp;&emsp;RNA STRAND提供检索-批量下载功能。它的高级搜索页面链接为：[RNA STRAND SEARCH](http://www.rnasoft.ca/strand/search.php)。本研究在高级搜素页面设定的条件为：长度在500bp以下，来源为RCSB PDB数据库（这可以确保每个二级结构有其对应的三级结构文件）。检索得到的结果如下图所示：

[![检索结果](https://s2.ax1x.com/2019/04/23/EEriUH.md.png)](https://imgchr.com/i/EEriUH)

&emsp;&emsp;检索页面的最底部提供批量下载，可以下载fasta或ct、dp、RNAML等文件。文件名为该RNA分子在PNA STRAND数据库中的编号，形如PDB_XXXXX。检索结果的二级界面提供该RNA分子的详细二级结构信息，其样例如下图所示：

[![二级界面](https://s2.ax1x.com/2019/04/23/EEr8Gn.md.png)](https://imgchr.com/i/EEr8Gn)

&emsp;&emsp;在二级界面中还提供对该RNA分子二级结构的详细分析。该文件不提供批量下载，需要爬取。经过观察可以发现，二级结构分析文件的url格式为：

```
http://www.rnasoft.ca/strand/analyser_output.php?molecule_ID=PDB_XXXXX&check_out_the=View+the+output+of+the+RNA+Secondary+Structure+Analyser+for+molecule++PDB_XXXXX
```

&emsp;&emsp;其中包含两个PDB_XXXXX形式的字符串，只需要将这两个字符串替换，即可得到对应ID的RNA分子二级结构分析文件页面。然后根据检索结果表中的对应关系，将其重命名为对应的PDB数据库ID。对上文中批量下载的二级结构文件也做重命名处理。至此，从RNA STRAND数据库中成功下载了 **二级结构文件** 和 **二级结构分析文件** 。

## RCSB PDB数据库
### Link

* [RCSB PDB](http://www.rcsb.org/)

### Introduction

This resource is powered by the Protein Data Bank archive-information about the 3D shapes of proteins, nucleic acids, and complex assemblies that helps students and researchers understand all aspects of biomedicine and agriculture, from protein synthesis to health and disease.The RCSB PDB builds upon the data by creating tools and resources for research and education in molecular biology, structural biology, computational biology, and beyond.

### Download
* 咕咕咕……
