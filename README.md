# Actions-OpenWrt for immortalwrt raspberryPi
Building OpenWrt with GitHub Actions

## 介绍
本项目源自于本人对于在树莓派4B上使用USB网卡（RTL8153）作为路由器，和部分特殊插件，以及ipv6的需求。
  
在我浏览了一圈后发现满足ipv6的固件不支持我的网卡，支持我网卡的固件不支持ipv6中继，再加上我之前一直使用的SuLingGG的固件已经停止更新了，因此启动了本项目。

## Tips

在我多尝试（包括我本地的服务器和Actions云端服务器）后，发现这个脚本原作者所使用的来自LEDE的分支对于树莓派以及部分插件的支持并不友好，会出现许多奇奇怪怪的编译错误，因此，如果你要修改源码仓库的话，请取保你自己有至少1次的成功编译并在你的机器上跑起来的经验，否则不建议随意修改。

当你首次编译时，请仅选择最基础的内容，例如网卡驱动，必要插件等，以提升成功几率。

在日常使用中，请尽量减少插件数量，确保只有必要的插件被安装，以提升运行稳定性。

在不增加编译项目的情况下，总编译时间大概是1小时40分钟

请尽量不要使用ssh来修改config文件，否则大概率被Github封控给打断

另外，如果你有任何问题，欢迎在issues栏目中提出，感谢您对本项目的支持，谢谢！

## 编译过程中启用ssh时的命令

进入ssh网页后使用control+c呼出命令栏。

输入cd openwrt && make menuconfig开始对.config文件做改动。

推出并保存后使用control+D断开网页ssh连接并使Actions编译继续。


## 本项目参考

- [immortalwrt-23.05](https://github.com/immortalwrt/immortalwrt/tree/openwrt-23.05)
- [openwrt-packages](https://github.com/kenzok8/openwrt-packages)
- [Actions-OpenWrt](https://github.com/P3TERX/Actions-OpenWrt)
- [GuLingGG-Rpi](https://github.com/SuLingGG/OpenWrt-Rpi)
- [原作者教程](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

## 原作者Credits

- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub Actions](https://github.com/features/actions)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Lean's OpenWrt](https://github.com/coolsnowwolf/lede)
- [tmate](https://github.com/tmate-io/tmate)
- [mxschmitt/action-tmate](https://github.com/mxschmitt/action-tmate)
- [csexton/debugger-action](https://github.com/csexton/debugger-action)
- [Cowtransfer](https://cowtransfer.com)
- [WeTransfer](https://wetransfer.com/)
- [Mikubill/transfer](https://github.com/Mikubill/transfer)
- [softprops/action-gh-release](https://github.com/softprops/action-gh-release)
- [ActionsRML/delete-workflow-runs](https://github.com/ActionsRML/delete-workflow-runs)
- [dev-drprasad/delete-older-releases](https://github.com/dev-drprasad/delete-older-releases)
- [peter-evans/repository-dispatch](https://github.com/peter-evans/repository-dispatch)

## 原作者License

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © [**P3TERX**](https://p3terx.com)
