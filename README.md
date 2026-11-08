# Digital IDE Efinity

用于分发 Digital IDE 配套 Efinity package 的发布仓库。Git 仓库仅保存本 README；Linux 与 Windows 压缩包通过 [GitHub Releases](https://github.com/Digital-EDA/digital-ide-efinity/releases) 提供，不放入 Git 历史。

## 下载

当前发布标签：[`20261109_014007`](https://github.com/Digital-EDA/digital-ide-efinity/releases/tag/20261109_014007)。标签对应打包时间标识，不代表 Efinity 软件版本号。

| 平台 / 来源 | 下载文件 | 大小（MiB） | 精确字节数 |
| --- | --- | ---: | ---: |
| Linux（ICer） | [efinity_package_linux_20261109_014007.zip](https://github.com/Digital-EDA/digital-ide-efinity/releases/download/20261109_014007/efinity_package_linux_20261109_014007.zip) | 310.8 | 325935861 |
| Windows | [efinity_package_windows_20261109_014007.zip](https://github.com/Digital-EDA/digital-ide-efinity/releases/download/20261109_014007/efinity_package_windows_20261109_014007.zip) | 316.4 | 331804964 |

请下载对应操作系统的 ZIP 附件。GitHub 自动生成的 **Source code (zip/tar.gz)** 只包含仓库 README，不包含上述 package。

## 解压与使用

1. 下载对应平台的 ZIP，并按下方 SHA-256 校验完整性。
2. 解压并保留目录层级；两个压缩包的顶层目录均为 `package/`。
3. 将 Linux 与 Windows 包分别解压到独立位置，不要合并或相互覆盖。
4. 按所用 Digital IDE 版本的 Efinity package 配置要求设置解压路径，并确认本机依赖、设备驱动及适用授权。

本次发布仅对原始归档进行 ZIP 完整性检查和 SHA-256 校验，不对具体主机、器件或板卡的运行兼容性作额外保证。仓库不重新授予包内第三方软件许可；使用和分发应遵守相应权利人的条款。

## SHA-256

```text
fe259667d343f03f40249a30d3488760d323e85490107a76a46714111adc1aa0  efinity_package_linux_20261109_014007.zip
a359af27f2ee7dcacc52ec856a429bf8a1ea6fef1f7f075618b42116b8c72d93  efinity_package_windows_20261109_014007.zip
```

Windows PowerShell：

```powershell
Get-FileHash .\efinity_package_windows_20261109_014007.zip -Algorithm SHA256
```

Linux：

```sh
sha256sum efinity_package_linux_20261109_014007.zip
```

校验值不一致时不要使用该文件，应重新下载后再次检查。
