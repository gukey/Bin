# Actions-OpenWrt

注：本仓库纯属个人根据自己的设备配置使用，直接FORK本仓库是不能自动编译并发布release的，请看下面使用方法。

## 使用方法

前面的自动编译以及个性化定制等修改，全部来源于[P3TERX大佬](https://p3terx.com/archives/build-openwrt-with-github-actions.html)的教程。</br>
这里只说发布release的方法：</br>
 1、自动编译及自动发布你也可以使用本仓库模板，请点击上面的Use this template(使用此模板）来创建你自己的新仓库。</br>
 2、点击右上角你的头像-settings-Developer settings-Personal access tokens生成新的令牌，下面的选项全部选中，随便起名保存，同时复制令牌内容。</br>
 3、回到刚建的新仓库，settings-Secrets-Add a new secret(添加密匙），取名RELEASES_TOKEN,把刚才复制的令牌粘贴进去保存。</br>
 4、定时编译的时间、触发自动编译的方法修改都在上面P3TERX大佬的教程里有说明。 </br>
 5、最关键一步，因为我在里面加入了开始编译和编译成功的微信消息提醒，所以除以上步骤外，还要把serverchan（微信推送）</br>
 的令牌保存到secret里，取名ServerChan.和前面第三步的添加密匙方法一致，否则差了这一步，刚开始编译就因为微信推送</br>
 找不到令牌而宣告失败。或者取消微信推送，注释掉yml文件中开始编译和编译结束的代码（共四行代码）即可。</br>
 
## 致谢

-[P3TERX](https://github.com/P3TERX/Actions-OpenWrt)   
-[id77](https://github.com/id77/OpenWrt-K2P-firmware)
