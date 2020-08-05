# 自定义策略示例：自定义网络和自定义网络ACL<a name="bms_umn_0058"></a>

自定义网络和自定义网络ACL相关策略未在BMS FullAccess、BMS CommonOperations或BMS ReadOnlyAccess系统策略中定义，您需要创建自定义策略来实现创建、修改、删除自定义网络和自定义网络ACL等操作。

本章节仅介绍各场景下自定义网络和自定义网络ACL策略的JSON文本内容，关于如何授权请参见[创建用户并授权使用BMS](创建用户并授权使用BMS.md)。

>![](public_sys-resources/icon-note.gif) **说明：** 
>在如下介绍中，涉及的其他服务授权项请参考各服务API参考的“权限策略和授权项”章节了解。

## 场景一：自定义网络和自定义网络ACL依赖的授权项<a name="section19628134719583"></a>

自定义网络和自定义网络ACL依赖的授权项必须包含：ecs:servers:list、bms:servers:list

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list"
                        ]
                }
        ]
}
```

如果未添加这些授权项，用户将无法进入裸金属服务器列表页面，也就无法进行任何自定义网络和自定义网络ACL相关的操作。

## 场景二：创建自定义网络<a name="section8829143016149"></a>

创建自定义网络对应授权项为：bms:virtualNetworks:create。

除了依赖[场景一：自定义网络和自定义网络ACL依赖的授权项](#section19628134719583)中的授权项外，还依赖vpc:vpcs:list，因为自定义网络创建页面会查询VPC列表。

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:create"
                        ]
                }
        ]
}
```

## 场景三：查询自定义网络列表<a name="section153318120156"></a>

查询自定义网络列表对应授权项为：bms:virtualNetworks:list

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:list"
                        ]
                }
        ]
}
```

## 场景四：查询自定义网络详情<a name="section124249253156"></a>

查询自定义网络详情对应授权项为：bms:virtualNetworks:get

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:list",
                                "bms:virtualNetworks:get"
                        ]
                }
        ]
}
```

## 场景五：修改自定义网络名称<a name="section16181644101513"></a>

修改自定义网络名称对应授权项为：bms:virtualNetworks:update

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:list",
                                "bms:virtualNetworks:get",
                                "bms:virtualSubnets:create",
                                "bms:virtualNetworks:update"
                        ]
                }
        ]
}
```

## 场景六：删除自定义网络<a name="section17784216165"></a>

删除自定义网络对应授权项为：bms:virtualNetworks:delete

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:list",
                                "bms:virtualNetworks:get",
                                "bms:virtualNetworks:delete"
                        ]
                }
        ]
}
```

## 场景七：添加自定义子网<a name="section101641881175"></a>

添加自定义子网对应授权项为：bms:virtualSubnets:create

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:list",
                                "bms:virtualNetworks:get",
                                "bms:virtualSubnets:list",
                                "bms:virtualSubnets:create"
                        ]
                }
        ]
}
```

## 场景八：查询自定义子网列表<a name="section217083518176"></a>

查询自定义子网列表对应授权项为：bms:virtualSubnets:list

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:list",
                                "bms:virtualNetworks:get",
                                "bms:virtualSubnets:list"
                        ]
                }
        ]
}
```

>![](public_sys-resources/icon-note.gif) **说明：** 
>该授权项仅用于自定义网络ACL关联自定义子网时使用。

## 场景九：删除自定义子网<a name="section38556312189"></a>

删除自定义子网对应授权项为：bms:virtualSubnets:delete

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:virtualNetworks:list",
                                "bms:virtualNetworks:get",
                                "bms:virtualSubnets:list",
                                "bms:virtualSubnets:delete"
                        ]
                }
        ]
}
```

## 场景十：创建自定义网络ACL<a name="section14481205618183"></a>

创建自定义网络ACL对应授权项为：bms:firewallGroups:create

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:firewallGroups:list",
                                "bms:firewallGroups:create"
                        ]
                }
        ]
}
```

## 场景十一：查询自定义网络ACL列表<a name="section1421022218197"></a>

查询自定义网络ACL列表对应授权项为：bms:firewallGroups:list

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:firewallGroups:list"
                        ]
                }
        ]
}
```

## 场景十二：查询自定义网络ACL详情<a name="section270013818194"></a>

查询自定义网络ACL详情对应授权项为：bms:firewallGroups:get

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:firewallGroups:list",
                                "bms:firewallGroups:get"
                        ]
                }
        ]
}
```

## 场景十三：修改自定义网络ACL<a name="section838216017203"></a>

该场景包括如下操作：修改名称、修改描述、添加ACL规则、修改ACL规则、删除ACL规则、开启/关闭ACL规则、向前/后插入规则、关联自定义子网（依赖bms:virtualSubnets:list授权项）。

修改自定义网络ACL对应授权项为：bms:firewallGroups:update

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:firewallGroups:list",
                                "bms:firewallGroups:get",
                                "bms:virtualSubnets:list",
                                "bms:firewallGroups:update"
                        ]
                }
        ]
}
```

## 场景十四：删除自定义网络ACL<a name="section2080173314224"></a>

删除自定义网络ACL对应授权项为：bms:firewallGroups:delete

完整的策略内容如下：

```
{
        "Version": "1.1",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "ecs:servers:list",
                                "bms:servers:list",
                                "vpc:vpcs:list",
                                "bms:firewallGroups:list",
                                "bms:firewallGroups:get",
                                "bms:firewallGroups:delete"
                        ]
                }
        ]
}
```

