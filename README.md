[中文](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

# Actions-OpenWrt

[![LICENSE](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square&label=LICENSE)](https://github.com/P3TERX/Actions-OpenWrt/blob/master/LICENSE)


A template for building OpenWrt with GitHub Actions

## My default config
项目release的固件除openwrt默认包含的组件外还含有以下内容：ipv6-helper、luci-app-filetransfer、BORE CPU Scheduler、SmartDNS、OPENCLASH（内置mihomo smart alpha内核）、~~DiskMan~~、TurboACC（支持firewall4）、BBR3补丁、taskplan（任务计划）、~~my-script（一个启动脚本，为了切换qdisc算法）~~、luci-app-temp-status（温度）、luci-theme-argon（主题）、重启插件、关机插件。

~~当前rax3000m固件使用来自https://github.com/chasey-dev/immortalwrt-mt798x-rebase 的源码，使用闭源驱动，支持MTK硬件NAT和硬件加速。~~
用回immortalwrt了，闭源驱动不知道为什么游戏延迟比开源驱动高一倍，而且这个分支的源码不支持开高功率，5G只能开到22db,immortalwrt可以开到24db。

**turboacc仅开启BBR算法可用，请勿打开其中的硬件加速选项，mtk硬件加速已经默认开启，与turboacc中的硬件加速以及防火墙中的路由/NAT 卸载功能冲突，打开会无限重启。**

## Usage

编译固件岂是如此不便之物？

编译脚本已重构焕新，抛弃原本的分开的三个自定义脚本，将大部分编译前准备流程合入一个脚本中，只需上传你的.config，

并按自己的想法修改对应机型（仅支持rax3000m和x86)的脚本（指本分支config目录下的SETUP_rax3000m.sh和SETUP_x86.sh）。

脚本各部分均有有中文注释，小学生也能轻松看懂。

目录：

 |->本项目

	|->.github ---->放置action运行脚本。

	|->config ----->放置所有需要的文件。

		|->files ---->放置你要添加的文件。
	
		|->rax3000m-->放置rax3000m的.config文件。
	
		|->x86 ------>放置x86的.config文件。
	

## Credits

- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub Actions](https://github.com/features/actions)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [Mikubill/transfer](https://github.com/Mikubill/transfer)
- [softprops/action-gh-release](https://github.com/softprops/action-gh-release)
- [Mattraks/delete-workflow-runs](https://github.com/Mattraks/delete-workflow-runs)
- [dev-drprasad/delete-older-releases](https://github.com/dev-drprasad/delete-older-releases)
- [peter-evans/repository-dispatch](https://github.com/peter-evans/repository-dispatch)

## License

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © [**P3TERX**](https://p3terx.com)
