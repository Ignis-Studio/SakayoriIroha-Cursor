进入“系统设置”->“颜色与主题”->“光标”并点击“从文件安装”，然后选择`SakayoriIroha-Cursor.tar.gz`文件，再点击应用即可。
如果发现光标大小不正确（大部分情况下都会如此），请执行如下指令（GUI 是无效的）来强行调整 KDE 内部的光标设置大小：
```
kwriteconfig6 --file kcminputrc --group Mouse --key cursorSize 128 # 使用 KDE 写入配置 kcminputrc，使得鼠标配置组下的 cursorSize 值设定为 128
echo "Xcursor.size: 128" > ~/.Xresources && xrdb -merge ~/.Xresources # 针对 XWayland 的兼容
```
执行完毕后，请您完全登出当前会话并重新登录以应用设置。
