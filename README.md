# Digital IDE Efinity

用于分发 Digital IDE 配套 Efinity package 的发布仓库。Git 仓库保存本 README；Linux 与 Windows 压缩包通过 [GitHub Releases](https://github.com/Digital-EDA/digital-ide-efinity/releases) 提供，不放入 Git 历史。

## 下载

当前发布标签：[`20261117_151317`](https://github.com/Digital-EDA/digital-ide-efinity/releases/tag/20261117_151317)。标签使用本次更新包的时间标识，不代表 Efinity 软件版本号。

| 平台 | 下载文件 | 大小（MiB） | 精确字节数 |
| --- | --- | ---: | ---: |
| Linux | [efinity_package_linux.zip](https://github.com/Digital-EDA/digital-ide-efinity/releases/download/20261117_151317/efinity_package_linux.zip) | 310.9 | 325976785 |
| Windows | [efinity_package_win.zip](https://github.com/Digital-EDA/digital-ide-efinity/releases/download/20261117_151317/efinity_package_win.zip) | 321.0 | 336639774 |

[下载 SHA256SUMS.txt](https://github.com/Digital-EDA/digital-ide-efinity/releases/download/20261117_151317/SHA256SUMS.txt)。GitHub 自动生成的 **Source code (zip/tar.gz)** 只包含仓库内容，不包含 Efinity package。

## 解压与使用

1. 下载对应操作系统的 ZIP，并按下方 SHA-256 校验完整性。
2. **Linux**：压缩包顶层为 `package/`；将解压后的 `package` 目录配置为 Efinity package 路径。
3. **Windows**：压缩包顶层直接包含 `bin/`、`lib/`、`arch/`、`res/`，没有外层 `package/`。请先创建独立目标目录（例如 `D:\APP\Efinity\package\package`），将 ZIP 内容解压到该目录，并将该目录配置为 Efinity package 路径。
4. 保留目录结构，将两个平台的包解压到独立位置；不要混合平台文件。package 根目录应直接包含 `bin/`、`lib/`、`arch/` 和 `res/`。
5. 在 Digital IDE 设置 `digital-ide.prj.efinix.package.path`；独立命令/MCP 也可通过 `DIGITAL_IDE_EFINIX_PACKAGE` 指定同一目录。

两个更新包的 XSD 均位于 `res/schema`，包括 `lpf.xsd`、`peri_util.xsd`、`enf_proj.xsd` 和 `p.xsd`。

本次发布验证了这两个原始 ZIP 的全部条目 CRC 完整性、目录层级和 SHA-256；不据此承诺所有器件或板卡的运行兼容性。仓库不重新授予包内第三方软件许可；使用和分发应遵守相应权利人的条款。

## SHA-256

```text
3c245bb8599df11e980ad86b42ddf4059dc27e94ff53e741c68b37cfddf5aba1  efinity_package_linux.zip
5fdc9a664d310e4eb80bbefb5046ffa9e580df9dd9eade14ec9b15b817508426  efinity_package_win.zip
```

Windows PowerShell：

```powershell
Get-FileHash .\efinity_package_win.zip -Algorithm SHA256
```

Linux（将校验文件与已下载的 ZIP 放在同一目录）：

```sh
sha256sum --check --ignore-missing SHA256SUMS.txt
```

校验值不一致时不要使用该文件，应重新下载后再次检查。

## 历史版本

- [20261109_014007](https://github.com/Digital-EDA/digital-ide-efinity/releases/tag/20261109_014007)
