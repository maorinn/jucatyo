---
title: "关闭Win10强制更新终极大法，来自微软总部工程师"
date: 2019-10-05T00:46:26+08:00
draft: false
---

{{% admonition warning "Warning" %}}
由于需要修改注册表，请您提前将修改部分的注册表导出备份下。
{{% /admonition %}}

## 操作步骤


1. 在小娜中搜索`Regedit`，定位到[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate]

2. 创建字符串值，名称分别是 `WUServer` `WUStatusServer`,`UpdateServiceUrlAlternate` 数值为都为`127.0.0.1`

3. 然后定位到[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU]

4. 新建`dword`值 ,名称为`UseWUServer` 数值为`1`

   如果没有该路径,请您新建路径。完成后重启电脑。