### 科研通签到脚本

每日北京时间7点40,21点40，两个时间点自动签到

### 注册登录GitHub

自行百度

### Fork项目到自己的Github

打开[Github](https://github.com/chenlunTian/ablesciSign)  项目地址: https://github.com/chenlunTian/ablesciSign

#### 点击 Fork 

![image-20240926213440393](./img/image-20240926213440393.png)

![image-20240926213618153](./img/image-20240926213618153.png)

#### 在自己Fork的项目中启用Actions

![image-20240926213708640](./img/image-20240926213708640.png)

![image-20240926213738452](./img/image-20240926213738452.png)

![image-20240926213818221](./img/image-20240926213818221.png)

#### 配置环境变量

![image-20240926213843274](./img/image-20240926213843274.png)

![image-20240926213937401](./img/image-20240926213937401.png)

##### 添加科研通cookie和推送服务secrets(以息知为例)

![image-20240926214237002](./img/image-20240926214237002.png)

同样的方式添加息知**secrets**

最终结果如下图。

![image-20240926214421277](./img/image-20240926214421277.png)

> 注：必须是 
>
> ​	ABLESCICOOKIE 
>
> ​	XZKEY

#### 运行Actions

点击 **Actions** -> **ablesci-checkin** ->  **Run workflow** ->  **Run workflow** ,即可运行。

运行成功则如下图所示。

![image-20240926214721811](./img/image-20240926214721811.png)

> 注：运行失败时，则显示红色。此时请检查错误日志。

#### 运行成功时，息知推送提醒

![息知](./img/xizhi.jpg)

> 注：如未收到 息知提醒 请检查 息知secrets是否填写正确 及 是否关注 息知公众号

### 登录科研通获取cookie

登录网站，打开调试模式，快捷键<kbd>F12</kbd>，依次选择 

<kbd>网络</kbd> -> <kbd>保留日志</kbd> -> <kbd>刷新界面 </kbd>-> 点击<kbd> https://www.ablesci.com/</kbd> -> 复制 <kbd>cookie</kbd> 

![image-20240926212008725](./img/image-20240926212008725.png)

### 获取推送secrets

打开[息知](https://xz.qqoq.net/#/index) 网站首页: https://xz.qqoq.net/#/index

```bash
https://xizhi.qqoq.net/{key}.send?title=标题&content=内容
```

> 其中**key**即需要获取的**secrets**

扫码登录 

![image-20240926215346889](./img/image-20240926215346889.png)