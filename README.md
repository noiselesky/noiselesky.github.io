# aRvin.tips

## Bentley MicroStation CONNECT安装说明：

1、先安装ms10000030zh.exe ,注意如果勾选了Visualization Content组件，电脑就需要联网，因为有些组件需要联网下载才能安装成功，安装列表里的Visualization Content组件默认是勾选状态，如果不需要这个组件就取消勾选。

2、软件安装完后将MicroStation CONNECT Edition文件夹复制并粘贴到你电脑中:\Program Files\Bentley\目录下面，覆盖替换掉原始MicroStation CONNECT Edition文件夹。

3、再将Program Files文件夹复制并粘贴到你电脑的C盘根目录，覆盖替换掉原始Program Files文件夹。

(注意:如果你以前安装过其他包含CONNECTION client客户端的bentley产品，请先卸载以前安装的CONNECTION client客户端，安装ms10时会自动再安装正确对应ms10版本的CONNECTION client客户端软件，如果提示不能替换该文件就在我的电脑右下角找到CONNECTION客户端图标，右键先退出CONNECTION客户端软件在替换掉Program Files文件夹)。

注意:Program Files文件夹和MicroStation CONNECT Edition文件夹里的2个Bentley.liclib.dll不通用，不能乱混用，否则无法启动软件。

4、最后双击执行一次MicroStation注册表.reg文件就完成了。

如果你的杀毒软件意外将Bentley.liclib.dll和licensetool.exe误当病毒删除就在杀毒软件恢复区找回，并且添加到杀毒软件的信任列表，以防被误杀。

注: 此替换文件与以前网上流传的try it now!.exe激活以及其他版本不一样，用此替换文件
是永不过期的，即使以后运行LicenseTool.exe看到列表写着过期或禁用也不影响MS的正常使用。

ms10版本对显卡有一定的要求，如果是低端集成显卡运行ms10版本时会提示2dModeling.dll 
3dModeling.dll之类的错误，无法使用ms10版本的电脑请安装MicroStation v8i老版本。

## office 2016激活以及还原方法

Windows 7系统下备份方式：保存好“tokens.dat”文件（C:\ProgramData\Microsoft\OfficeSoftwareProtectionPlatform）。 

Windows 8系统下备份方式：打开C:\Windows\System32\spp\store文件夹（注意要显示隐藏文件），将“data.dat、tokens.dat、cache文件夹下的cache.dat”复制出来保存。 

Windows 8.1/10系统下备份方式：打开C:\Windows\System32\spp\store\2.0文件夹（注意要显示隐藏文件），将“data.dat、tokens.dat、cache文件夹下的cache.dat”复制出来保存。

备份激活后还原方法：同样随着系统的不同而不同

Windows7系统恢复方法：

1、以管理员身份运行“命令提示符”键入：net stop osppsvc
2、断网，使用备份的“tokens.dat”覆盖源文件。
3、以管理员身份运行“命令提示符”键入：net start osppsvc
4、打开Office程序，等待自动配置完毕，输入激活密钥即可成功激活。

Windows8/8.1/10系统下恢复方法：

1、以管理员身份运行“命令提示符”键入：net stop sppsvc
2、只需把备份的“3个文件”（data.dat、tokens.dat、 cache.dat）覆盖源文件即可成功激活。
3、以管理员身份运行“命令提示符”键入：net start sppsvc

恢复激活后检查激活是否可用：

按下WIN+R输入CMD 点击确定；

cscript.exe "C:\Program Files\Microsoft Office\Office16\OSPP.VBS" /dstatus

安装后卸载KEY的方法：
 
首先查询KEY：（参考验证是否已经完全激活）
 
cscript "C:\Program Files\Microsoft Office\Office16\ospp.vbs" /unpkey: KEY的后五位

