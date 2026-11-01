[中文](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

# Actions-OpenWrt

[![LICENSE](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square&label=LICENSE)](https://github.com/P3TERX/Actions-OpenWrt/blob/master/LICENSE)


A template for building OpenWrt with GitHub Actions

当前rax3000m固件使用来自 https://github.com/chasey-dev/immortalwrt-mt798x-rebase的 源码，使用闭源驱动，支持MTK硬件NAT和硬件加速。


## Usage


目录：

 |->项目

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
