# 重装弹性云服务器操作系统（未安装Cloud-init）<a name="ZH-CN_TOPIC_0077841398"></a>

## 功能介绍<a name="section61372619"></a>

重装弹性云服务器的操作系统。

该接口支持未安装Cloud-init或Cloudbase-init的镜像。

## 接口约束<a name="section2842257210401"></a>

-   关机状态或者重装操作系统失败的弹性云服务器，才能执行重装操作。
-   不包含系统盘的弹性云服务器不能执行重装操作。
-   执行重装操作系统任务时，请勿并行执行其他任务，否则可能会引起重装操作系统失败。
-   该接口支持未安装Cloud-init或Cloudbase-init的镜像。

## URI<a name="section15482662"></a>

POST /v1/\{project\_id\}/cloudservers/\{server\_id\}/reinstallos

参数说明请参见[表1](#table55945983)。

**表 1**  参数说明

<a name="table55945983"></a>
<table><thead align="left"><tr id="row11302482"><th class="cellrowborder" valign="top" width="24.462446244624463%" id="mcps1.2.4.1.1"><p id="p43085863"><a name="p43085863"></a><a name="p43085863"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.272427242724273%" id="mcps1.2.4.1.2"><p id="p294000"><a name="p294000"></a><a name="p294000"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="51.26512651265126%" id="mcps1.2.4.1.3"><p id="p23814038"><a name="p23814038"></a><a name="p23814038"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49888896"><td class="cellrowborder" valign="top" width="24.462446244624463%" headers="mcps1.2.4.1.1 "><p id="p14468758"><a name="p14468758"></a><a name="p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.272427242724273%" headers="mcps1.2.4.1.2 "><p id="p31118786"><a name="p31118786"></a><a name="p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.26512651265126%" headers="mcps1.2.4.1.3 "><p id="p145635146499"><a name="p145635146499"></a><a name="p145635146499"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row613736410235"><td class="cellrowborder" valign="top" width="24.462446244624463%" headers="mcps1.2.4.1.1 "><p id="p2736446410235"><a name="p2736446410235"></a><a name="p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.272427242724273%" headers="mcps1.2.4.1.2 "><p id="p192907210235"><a name="p192907210235"></a><a name="p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.26512651265126%" headers="mcps1.2.4.1.3 "><p id="p2203711610235"><a name="p2203711610235"></a><a name="p2203711610235"></a>弹性云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section5126234"></a>

请求参数如[表2](#table2840889)所示。

**表 2**  请求参数

<a name="table2840889"></a>
<table><thead align="left"><tr id="row19854472"><th class="cellrowborder" valign="top" width="21.800000000000004%" id="mcps1.2.5.1.1"><p id="p5212090120624"><a name="p5212090120624"></a><a name="p5212090120624"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.720000000000002%" id="mcps1.2.5.1.2"><p id="p5568008920626"><a name="p5568008920626"></a><a name="p5568008920626"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.620000000000005%" id="mcps1.2.5.1.3"><p id="p4189246820628"><a name="p4189246820628"></a><a name="p4189246820628"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.86000000000001%" id="mcps1.2.5.1.4"><p id="p2137802720629"><a name="p2137802720629"></a><a name="p2137802720629"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6277626"><td class="cellrowborder" valign="top" width="21.800000000000004%" headers="mcps1.2.5.1.1 "><p id="p38725660"><a name="p38725660"></a><a name="p38725660"></a>os-reinstall</p>
</td>
<td class="cellrowborder" valign="top" width="13.720000000000002%" headers="mcps1.2.5.1.2 "><p id="p49770771"><a name="p49770771"></a><a name="p49770771"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.620000000000005%" headers="mcps1.2.5.1.3 "><p id="p4900679"><a name="p4900679"></a><a name="p4900679"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="42.86000000000001%" headers="mcps1.2.5.1.4 "><p id="p61410719"><a name="p61410719"></a><a name="p61410719"></a>重装弹性云服务器。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  os-reinstall字段数据结构说明

<a name="table32200631"></a>
<table><thead align="left"><tr id="row47660253"><th class="cellrowborder" valign="top" width="21.62216221622162%" id="mcps1.2.5.1.1"><p id="p12719134223610"><a name="p12719134223610"></a><a name="p12719134223610"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.72137213721372%" id="mcps1.2.5.1.2"><p id="p171964243615"><a name="p171964243615"></a><a name="p171964243615"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.61216121612161%" id="mcps1.2.5.1.3"><p id="p11719144217362"><a name="p11719144217362"></a><a name="p11719144217362"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.04430443044304%" id="mcps1.2.5.1.4"><p id="p97194429363"><a name="p97194429363"></a><a name="p97194429363"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row65851064"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p32335967"><a name="p32335967"></a><a name="p32335967"></a>adminpass</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p1967662"><a name="p1967662"></a><a name="p1967662"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p25162958"><a name="p25162958"></a><a name="p25162958"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p16847167112050"><a name="p16847167112050"></a><a name="p16847167112050"></a>云服务器管理员帐户的初始登录密码。</p>
<p id="p8742832102714"><a name="p8742832102714"></a><a name="p8742832102714"></a>其中，Windows管理员帐户的用户名为Administrator。</p>
<p id="p11576631102714"><a name="p11576631102714"></a><a name="p11576631102714"></a>建议密码复杂度如下：</p>
<a name="ul37080817102714"></a><a name="ul37080817102714"></a><ul id="ul37080817102714"><li>长度为8-26位。</li><li>密码至少必须包含大写字母、小写字母、数字和特殊字符（!@$%^-_=+[{}]:,./?~#*）中的三种。</li></ul>
<div class="note" id="note65349643112129"><a name="note65349643112129"></a><a name="note65349643112129"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul8134516175112"></a><a name="ul8134516175112"></a><ul id="ul8134516175112"><li>对于Windows弹性云服务器，密码不能包含用户名或用户名的逆序，不能包含用户名中超过两个连续字符的部分。</li><li>adminpass和keyname不能同时为空。</li></ul>
</div></div>
</td>
</tr>
<tr id="row45934497"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p29706771"><a name="p29706771"></a><a name="p29706771"></a>keyname</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p57438237"><a name="p57438237"></a><a name="p57438237"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p21985640"><a name="p21985640"></a><a name="p21985640"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p36006428"><a name="p36006428"></a><a name="p36006428"></a>密钥名称。</p>
</td>
</tr>
<tr id="row2345411710289"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p2073531110289"><a name="p2073531110289"></a><a name="p2073531110289"></a>userid</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p183865010289"><a name="p183865010289"></a><a name="p183865010289"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p1471297410289"><a name="p1471297410289"></a><a name="p1471297410289"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p5090020910289"><a name="p5090020910289"></a><a name="p5090020910289"></a>用户ID。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section46136113"></a>

请参考[响应（任务类）](响应（任务类）.md)。

## 请求示例<a name="section15863105410364"></a>

```
POST https://{endpoint}/v1/{project_id}/cloudservers/{server_id}/reinstallos
```

```
{
    "os-reinstall": {
        "keyname": "KeyPair-350b", 
        "userid": "7e25b1da389f4697a79df3a0e5bd494e"
    }
}
```

## 响应示例<a name="section1760151015465"></a>

无

## 返回值<a name="section27037160"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码说明](错误码说明.md)。

