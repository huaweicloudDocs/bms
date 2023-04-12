# 创建用户并授权使用BMS<a name="bms_umn_0056"></a>

如果您需要对您所拥有的BMS资源进行精细的权限管理，您可以使用[统一身份认证服务](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)[统一身份认证服务](https://docs.otc.t-systems.com/usermanual/iam/iam_01_0026.html)[统一身份认证服务](https://docs.prod-cloud-ocb.orange-business.com/zh-cn/usermanual/iam/iam_01_0026.html)（Identity and Access Management，简称IAM），通过IAM，您可以：

-   根据企业的业务组织，在您的华为云帐号帐号中，给企业中不同职能部门的员工创建IAM用户，让员工拥有唯一安全凭证，并使用BMS资源。
-   根据企业用户的职能，设置不同的访问权限，以达到用户之间的权限隔离。
-   将BMS资源委托给更专业、高效的其他华为云帐号帐号或者云服务，这些帐号或者云服务可以根据权限进行代运维。

如果华为云帐号帐号已经能满足您的要求，不需要创建独立的IAM用户，您可以跳过本章节，不影响您使用BMS的其它功能。

本章节为您介绍对用户授权的方法，操作流程如[图  给用户授予BMS权限流程](#fig1837718415011)所示。

## 前提条件<a name="section16471332171420"></a>

给用户组授权之前，请您了解用户组可以添加的BMS权限，并结合实际需求进行选择，BMS支持的系统权限，请参见：[BMS权限管理](https://support.huaweicloud.com/productdesc-bms/bms_pd_0011.html)。若您需要对除BMS之外的其它服务授权，IAM支持服务的所有权限请参见[系统权限](https://support.huaweicloud.com/usermanual-permissions/iam_01_0001.html)[权限集](https://docs.otc.t-systems.com/permissions/index.html)[权限集](https://docs.prod-cloud-ocb.orange-business.com/zh-cn/permissions/index.html)。

## 示例流程<a name="section617655112114"></a>

**图 1**  给用户授予BMS权限流程<a name="fig1837718415011"></a>  
![](figures/给用户授予BMS权限流程.png "给用户授予BMS权限流程")

1.  <a name="li10176121316284"></a>[创建用户组并授权](https://support.huaweicloud.com/usermanual-iam/iam_03_0001.html)[创建用户组并授权](https://docs.otc.t-systems.com/usermanual/iam/iam_01_0030.html)[创建用户组并授权](https://docs.prod-cloud-ocb.orange-business.com/zh-cn/usermanual/iam/iam_01_0030.html)

    在IAM控制台创建用户组，并授予裸金属服务器只读权限“BMS ReadOnlyAccess”。

2.  [创建用户并加入用户组](https://support.huaweicloud.com/usermanual-iam/iam_02_0001.html)

    在IAM控制台创建用户，并将其加入[1](#li10176121316284)中创建的用户组。

3.  [用户登录](https://support.huaweicloud.com/usermanual-iam/iam_01_0552.html)[用户登录](https://docs.otc.t-systems.com/usermanual/iam/iam_01_0032.html)[用户登录](https://docs.prod-cloud-ocb.orange-business.com/zh-cn/usermanual/iam/iam_01_0032.html)并验证权限

    新创建的用户登录控制台，切换至授权区域，验证权限：

    -   在“服务列表”中选择“计算 \> 裸金属服务器”，进入BMS主界面，单击右上角“购买裸金属服务器”尝试购买裸金属服务器。若提示权限不足，表示“BMS ReadOnlyAccess”已生效。
    -   在“服务列表”中选择除裸金属服务器以外的任意一个服务，若提示权限不足，表示“BMS ReadOnlyAccess”已生效。


