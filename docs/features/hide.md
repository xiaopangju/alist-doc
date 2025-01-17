---
sidebar_position: 4
---

# 隐藏


### 后台隐藏
后台api不会返回隐藏的数据
:::tip

请注意：v2.0.6及以后，管理员登录后隐藏功能失效。

:::

在后台元信息处添加记录，填写路径和路径中要隐藏的文件（夹）名即可，其中路径同[加密中的路径](./encrypt.md)

正确填写路径之后，填写hide字段，填写要隐藏的文件（夹）名称，以,分隔，比如要隐藏https://alist.nn.ci/本地存储 下的README.md和index.tsx文件，则填写:
- path: `/本地存储`
- hide: `README.md,index.tsx`

#### 图解
![list](https://store.heytapimage.com/cdo-portal/feedback/202203/03/f2c06e0f013f8ac2ff9420d93f15f2ea.png)
![hide](https://store.heytapimage.com/cdo-portal/feedback/202203/03/d87a1d6397318b0c4727000ed9dd5732.png)

即可。

### 前端隐藏
后台api会返回数据，只是前端不会去显示。

在后台的前端设置中填写`隐藏文件`这个设置，匹配正则表达式隐藏的文件，如果不懂的话不要乱填，错误的正则表达式会导致前端页面崩溃，每行一个，默认有一个隐藏所有目录下的`README.md`的示例表达式