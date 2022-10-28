# 重新挂载lvm卷后如何更新磁盘metadata信息<a name="bms_faq_0105"></a>

## 操作场景<a name="section1984753616245"></a>

在重装操作系统后，重新挂载lvm卷后需要及时更新磁盘metadata信息，避免后续重启后进入不了操作系统。

## 操作步骤<a name="section169847449531"></a>

采用LVM分区的裸金属服务器重装操作系统后，如果存在重新挂载lvm卷的场景，请在挂载完lvm卷后执行如下命令及时更新磁盘metadata命令，确保再次重启操作系统后磁盘metadata信息和实际挂载信息保持一致。其中，“sysvg”为对应lvm分区的vg名称。

**lvm vgcfgrestore **_sysvg_

**lvm pvscan**

**lvm vgscan**

**lvm vgchange -ay**

