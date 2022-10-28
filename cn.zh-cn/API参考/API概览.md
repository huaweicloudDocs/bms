# API概览<a name="bms_api_0200"></a>

## 接口介绍<a name="section1852025323614"></a>

裸金属服务器所提供的接口分为BMS接口与OpenStack原生接口。

通过配合使用BMS服务提供的接口和OpenStack原生接口，您可以完整地使用裸金属服务器的所有功能。例如创建裸金属服务器实例，可以使用OpenStack原生接口，也可以使用BMS接口进行创建。

**表 1**  接口说明

|类型|子类型|说明|
|--|--|--|
|BMS接口|查询API版本信息|查询裸金属服务器服务当前所用的API版本。|
|生命周期管理|可以实现包周期裸金属服务器的创建、裸金属服务器详情查询等操作。|
|状态管理|裸金属服务器修改名称、重装系统、启动、重启、关闭等功能。|
|规格管理|用于查询裸金属服务器的规格详情和规格扩展信息，比如规格ID、规格名称、CPU核数、启动源。|
|网卡管理|可以查询裸金属服务器网卡信息，比如网卡的IP地址、MAC地址。|
|云硬盘管理|裸金属服务器云硬盘挂载、卸载，以及挂载的磁盘信息查询。|
|元数据管理|裸金属服务器元数据包含了裸金属服务器在云平台的基本信息，例如服务器ID、主机名、网络信息等。您可以更新裸金属服务器的元数据。|
|租户配额管理|查询某租户名下，所有资源的配额信息，包括已使用配额。|
|密码管理|查询是否支持一键重置密码，如果支持，您可以对裸金属服务器重置密码。还包括Windows裸金属服务器的密码获取与清除。|
|查询Job状态|对于创建裸金属服务器、挂卸卷等异步API，命令下发后，会返回“job_id”，通过“job_id”可以查询任务的执行状态。|
|OpenStack原生接口（v2.1版本）|生命周期管理|查询类接口，包括查询裸金属服务器详情、查询裸金属服务器列表、查询裸金属服务器详情信息列表。|
|状态管理|状态管理接口，包括对裸金属服务器的启动、重启、关闭等接口。|
|元数据管理|裸金属服务器元数据包含了裸金属服务器在云平台的基本信息，例如服务器ID、主机名、网络信息等。您可以查询、更新、删除裸金属服务器的元数据。|
|IP信息查询|查询裸金属服务器的私有IP地址信息，包括IP地址版本（IPv4或者IPv6）和具体的IP地址。|
|裸金属服务器规格查询|查询裸金属服务器规格信息列表：查询系统中的所有规格，或者指定过滤条件检索需要的规格。查询裸金属服务器规格详情：根据裸金属服务器的规格ID，查询规格的详细信息，比如规格名称、CPU核数、内存大小等。查询裸金属服务器规格extra_specs参数的详情：“extra_specs”参数用于描述裸金属服务器规格的键值对，如果您想确认某个规格是否支持快速发放，可以调用该接口进行查询。|
|裸金属服务器网卡查询|您可以查询裸金属服务器的所有网卡；或者根据网卡ID，查询某一个网卡的详细信息，比如网卡的IP地址、MAC地址。|
|云硬盘管理|您可以查询裸金属服务器所挂载的云硬盘信息；或者根据磁盘ID，查询裸金属服务器挂载的某个云硬盘信息，比如挂载目录。|
|SSH密钥管理|查询SSH密钥信息列表、详情，创建、删除SSH密钥等功能。|
|一维标签管理|裸金属服务器一维标签的增删改查。|


>![](public_sys-resources/icon-note.gif) **说明：** 
>-   使用BMS提供的接口时，您需要使用BMS服务自身的Endpoint。
>-   使用OpenStack原生接口时，您需要使用ECS服务注册的Endpoint。
>-   当前版本调用OpenStack接口不支持HTTP长连接。

## BMS接口使用限制<a name="section1016613793716"></a>

**表 2**  BMS接口使用限制

|类型|API|URI|使用限制|
|--|--|--|--|
|查询API版本信息|查询API版本信息列表|GET /|每分钟2000次|
|查询指定API版本信息|GET /{api_version}|每分钟2000次|
|生命周期管理|创建裸金属服务器|POST /v1/{project_id}/baremetalservers|每分钟50次|
|查询裸金属服务器详情|GET /v1/{project_id}/baremetalservers/detail|每分钟500次|
|查询裸金属服务器详情列表|GET /v1/{project_id}/baremetalservers/{server_id}|每分钟1000次|
|状态管理|修改裸金属服务器名称|PUT /v1/{project_id}/baremetalservers/{server_id}|每分钟100次|
|重装裸金属服务器操作系统|POST /v1/{project_id}/baremetalservers/{server_id}/reinstallos|每分钟50次|
|启动裸金属服务器|POST /v1/{project_id}/baremetalservers/action|每分钟50次|
|重启裸金属服务器|POST /v1/{project_id}/baremetalservers/action|每分钟50次|
|关闭裸金属服务器|POST /v1/{project_id}/baremetalservers/action|每分钟50次|
|规格管理|查询规格详情和规格扩展信息列表|GET /v1/{project_id}/baremetalservers/flavors|每分钟500次|
|网卡管理|查询裸金属服务器网卡信息|GET /v1/{project_id}/baremetalservers/{server_id}/os-interface|每分钟500次|
|云硬盘管理|裸金属服务器挂载云硬盘|POST /v1/{project_id}/baremetalservers/{server_id}/attachvolume|每分钟100次|
|裸金属服务器卸载云硬盘|DELETE /v1/{project_id}/baremetalservers/{server_id}/detachvolume/{attachment_id}|每分钟100次|
|查询裸金属服务器挂载的磁盘信息|GET /v1/{project_id}/baremetalservers/{server_id}/os-volume_attachments|每分钟500次|
|元数据管理|更新裸金属服务器元数据|POST /v1/{project_id}/baremetalservers/{server_id}/metadata|每分钟100次|
|租户配额管理|查询租户配额|GET /v1/{project_id}/baremetalservers/limits|每分钟500次|
|密码管理|查询是否支持一键重置密码|GET /v1/{project_id}/baremetalservers/{server_id}/os-resetpwd-flag|每分钟500次|
|一键重置裸金属服务器密码|PUT /v1/{project_id}/baremetalservers/{server_id}/os-reset-password|每分钟50次|
|Windows裸金属服务器获取密码|GET /v1/{project_id}/baremetalservers/{server_id}/os-server-password|每分钟50次|
|Windows裸金属服务器清除密码|DELETE /v1/{project_id}/baremetalservers/{server_id}/os-server-password|每分钟50次|
|Job管理|查询Job状态|GET /v1/{project_id}/jobs/{jobId}|每分钟2000次|


