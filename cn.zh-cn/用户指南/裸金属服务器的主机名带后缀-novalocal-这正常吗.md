# 裸金属服务器的主机名带后缀“novalocal”，这正常吗？<a name="bms_faq_0066"></a>

## 问题描述<a name="section10979141164416"></a>

用户使用**hostname**命令查看不同镜像的裸金属服务器主机名，发现部分镜像的裸金属服务器主机名带后缀“.novalocal“，如示例所示：

假设创建裸金属服务器时，用户自定义的主机名是“abc“，使用**hostname**命令查看不同镜像下，裸金属服务器的主机名以及重启裸金属服务器后的主机名，显示结果如[表1](#table168595206502)所示。

**表 1**  不同镜像查询的主机名

|镜像|重启前查询的主机名|重启后再次查询的主机名|
|--|--|--|
|CentOS 6.8|abc|abc.novalocal|
|CentOS 7.3|abc.novalocal|abc.novalocal|
|Ubuntu 16|abc|abc|


不同镜像的裸金属服务器，查询的主机名有的带后缀“.novalocal“，有的不带后缀“.novalocal“，这正常吗？

## 问题处理<a name="section152294541871"></a>

正常现象。

Linux裸金属服务器的静态主机名来源于创建裸金属服务器时，通过Cloud-init注入的用户自定义名称。经测试验证发现，Cloud-init和不同发行版本的操作系统在配合实现上，存在差异，具体表现为：查询的主机名有的带后缀“.novalocal“，有的不带后缀“.novalocal“。

如果您希望查询到的主机名不带后缀“.novalocal“，可以通过更改主机名进行规避，修改主机名的方法请参见[如何设置裸金属服务器的静态主机名](https://support.huaweicloud.com/bms_faq/bms_faq_0023.html)。

