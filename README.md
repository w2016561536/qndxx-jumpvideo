# qndxx-jumpvideo
# 青年大学习跳过视频python脚本
使用方法：<br>
1. 仅限安卓用户，ios用户请锁屏后拖动进度条。
2. 安装QPython 3 翻译器（QPython 3L/H皆可，以后可能会有更多），打开，授予存储的读写权限（因为需要修改微信的缓存数据）。
3. 打开编辑器选项，右上角有个打开文件，打开此脚本。
4. 默认内部存储根目录为`/storage/Emulated/0/`,若存在多用户（多密码多空间或者炼妖壶诸如此类），请修改`yourstorage`参数至微信在实际空间内的内部存储根目录。
5. 运行脚本，回到微信。
6. 进入青年大学习界面，在开始学习界面（不是个人信息确认界面，那里不需要等）等待 **缓存完成** ，点击开始学习。
> ## 如何判断“缓存完成”?
> 注意通知栏的网速显示，在“开始学习”界面时会尽全力下载视频。所以在缓存的时候网速会飙升至1M/s甚至更高。  
> 当缓存完成时网络会闲置，通知栏网速也会降至1K/s或者更低。
7. 视频被自动跳过。截图走人。
8. 有时候以为网络环境过差，微信没有及时缓存，播放成了原视频，返回键回到个人信息确认界面重新进入即可。
  
  
  
> ## 补充说明原理：
> - 在等待的这段时间，微信会把青年大学习的视频缓存到上面说的那个文件夹内。
> - 程序每隔3秒检测一次文件夹，如果有视频，就把它换成一个非常短的空白视频，这样点击开始学习后就会直接显示“学习完成”（因为“视频”已经放完了）。
