# R-synbreed
R包synbreed不能使用官方命令下载。

# 在R语言中使用synbreed包可以方便地进行基因组选择和育种分析。本文将介绍如何在R中安装synbreed包。

# 第一种

if (!requireNamespace("BiocManager", quietly = TRUE))

install.packages("BiocManager")

BiocManager::install() #安装

BiocManager包工具

BiocManager::install(c("regress", "LDheatmap","doBy","qtl")) #安装依赖包

library(synbreed) #使用包

# 但是失败了，接下来推荐第二种方法

#安装依赖包

install.packages("regress")

install.packages("LDheatmap")

install.packages("doBy")

install.packages("qtl")

install.packages("synbreed",repos="http://r-forge.r-project.org")

安装完成后，可以通过以下命令加载synbreed包：

library(synbreed)

但是有可能需要安装其他可能的包

install.packages("")

在2023年3月，笔者下载发现LDheatmap已经不能从官方下载，可考虑从在GitHub安装LDheatmap的旧版本。

总之，安装synbreed包比较麻烦，需要先安装必要的依赖包，然后使用install.packages()函数或者devtools::install_github()函数安装。如果有需要，可以通过library()函数加载synbreed包，并开始使用其中的函数。

参考自synbreed包安装https://link.zhihu.com/?target=https%3A//www.jianshu.com/p/42259c4ce95d
