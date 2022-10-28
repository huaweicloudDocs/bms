# 怎么确定裸金属服务器规格的board\_type？<a name="bms_faq_1601"></a>

## 问题背景<a name="section747243020476"></a>

裸金属服务器不同规格存在公共镜像兼容性差异，您可以在管理控制台查看每种规格所支持的公共镜像，也可以通过“[查询镜像列表](https://support.huaweicloud.com/api-ims/ims_03_0602.html)”接口来查询。在调用接口时，需要填入裸金属服务器规格的board\_type信息，那么如何确定该参数值呢？本章节为您详解。

## 处理方法<a name="section91113735411"></a>

裸金属服务器规格组成方式：physical.AB.C，例如physical.s1.large

其中，

-   A表示系列，例如：s表示通用型、c表示计算型、m表示内存型。
-   B表示系列号，例如：s1中的1表示通用型I代。
-   C表示当前系列中的规格大小，例如：large、medium、xlarge。

board\_type为规格的缩写，包括：AB+C中前1位或多位字母。例如，规格为physical.s1.large，则board\_type为s1l。更多规格的board\_type示例请参考[表1](#table498012513417)。

**表 1**  裸金属服务器规格对应的board\_type

|裸金属服务器规格|board_type|
|--|--|
|physical.m2.medium|m2m|
|physical.h2.large|h2l|
|physical.hs2.large|hs2l|
|physical.io2.xlarge|io2xl|
|physical.kl1.3xlarge|kl13xl|


