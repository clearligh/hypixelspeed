# hypixelspeed
# 我的世界Hypixel加速IP

## 准备:
* 一台VPS  
* CentOS 7系统，宽带建议 5 Mbps。

## 安装Brook流量转发脚本
```
cd /
mkdir brook
cd brook
wget https://cdn.cakeskin.tk/brook.sh
bash brook.sh
```
![image](https://user-images.githubusercontent.com/98816824/200165486-7fb43ba2-2752-4477-8007-795522204ba0.png)

输入 1 安装 Brook,之后按回车

![image](https://user-images.githubusercontent.com/98816824/200165579-05fd4893-22a0-4519-9518-0ffc489424f1.png)

出现这个后重新输入``` bash brook.sh``` 注意一定要在brook文件夹下输入
输入```7```设置 Brook 端口转发 然后输入```1``` 添加端口转发

![image](https://user-images.githubusercontent.com/98816824/200165699-3155b5f6-9510-4aca-9fe8-63a56e9fecae.png)

然后本地监听端口填写 25565

![image](https://user-images.githubusercontent.com/98816824/200165739-0cf44d43-8898-4b21-bdda-336725b0707b.png)

## 获取转发ip

```Win+r``` 打开CMD 输入```ping mc.hypixel.net```
![image](https://user-images.githubusercontent.com/98816824/200165884-78a72b3f-8928-44f0-9b93-9f683a13b25f.png)
红框内的即为转发IP

将转发IP输入到VPS里即可
![image](https://user-images.githubusercontent.com/98816824/200165947-d20f7c49-00aa-4f0b-a4f6-6569fd4f02be.png)
被监听端口也填写 25565

输入```y```启用
![image](https://user-images.githubusercontent.com/98816824/200165968-b8672332-17d5-4846-817a-ffae89a5f6a7.png)

出现这个即配置成功
![image](https://user-images.githubusercontent.com/98816824/200166005-f2162f06-0115-4b82-b497-863bdbc65ae1.png)

##填写 本地Hosts

进入以下文件夹```C:\Windows\System32\drivers\etc\```找到``` hosts ```文件，右键以管理员身份打开，打开方式用记事本即可(具体方法可百度)

将以下代码粘贴进去，然后保存退出
```
xxx.xxx.xxx.xxx mc.hypixel.net
# 如果你想保持 mc.hypixel.net 原有的解析，只需要把 mc 换成任意字符串就行
# xxx.xxx.xxx.xxx 替换为你自己的服务器 IP 地址
```
