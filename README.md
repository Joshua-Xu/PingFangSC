# PingFang SC 独立字重版

本仓库提供按字重拆分的 PingFang SC TrueType 字体文件，主要用于改善 Windows 应用（尤其是 WPS Office）中的安装、字体选择和字重识别体验。

## 本次变更

- 将原仓库根目录下的旧版 `PingFang-*.ttf` 文件替换为 `PingFangSC-*.ttf`。
- 将字体统一放入 [`ttf`](./ttf) 目录，仓库结构更清晰。
- 采用 6 个独立字体文件，每个文件对应一个明确字重，不再依赖应用自动推断字重。
- 统一字体菜单名称为 `PingFang SC + 字重`，并保留对应的中文名称。
- 新增 [`PingFangSC-苹果命名独立字重说明.md`](./PingFangSC-苹果命名独立字重说明.md)，记录菜单名称和 Weight class。

## 字重列表

| 字体文件 | 英文菜单名称 | 中文菜单名称 | Weight class |
| --- | --- | --- | ---: |
| `PingFangSC-Ultralight.ttf` | PingFang SC Ultralight | 苹方-简 极细体 | 100 |
| `PingFangSC-Thin.ttf` | PingFang SC Thin | 苹方-简 纤细体 | 200 |
| `PingFangSC-Light.ttf` | PingFang SC Light | 苹方-简 细体 | 300 |
| `PingFangSC-Regular.ttf` | PingFang SC Regular | 苹方-简 常规体 | 400 |
| `PingFangSC-Medium.ttf` | PingFang SC Medium | 苹方-简 中黑体 | 500 |
| `PingFangSC-Semibold.ttf` | PingFang SC Semibold | 苹方-简 中粗体 | 600 |

## Windows 与 WPS Office 支持

WPS Office for Windows 使用 Windows 已安装的系统字体。这一版本把 6 个字重拆分为独立的 `.ttf` 文件，并为每个字重设置清晰的菜单名称，因此在 WPS 文字、WPS 演示和 WPS 表格中更容易直接选择所需字重，也能减少仅显示一个字体名、加粗映射错误或不同字重互相覆盖的问题。

### 安装方法

1. 关闭正在运行的 WPS Office。
2. 打开 [`ttf`](./ttf) 目录并选中全部 6 个 `.ttf` 文件。
3. 右键选择“安装”；需要供电脑上的所有账户使用时，可选择“为所有用户安装”（可能需要管理员权限）。
4. 重新启动 WPS Office，在字体列表中搜索 `PingFang SC` 或 `苹方-简`。
5. 建议直接选择带字重名称的字体，例如 `PingFang SC Medium`，不要只依赖 WPS 的“加粗”按钮模拟其他字重。

### 更新旧版本字体

如果 Windows 中已经安装过其他版本的 PingFang 字体，建议先关闭 WPS，在 Windows“字体”设置中卸载旧版本，再安装本仓库中的全部 6 个文件。安装后重新打开 WPS；若字体列表没有立即刷新，可注销并重新登录 Windows 或重启电脑。

### 文档兼容提示

- 接收文档的电脑也需要安装相同字体，否则 WPS 会使用替代字体，版式可能发生变化。
- 对外发送或跨设备编辑前，建议在 WPS 中导出 PDF，或使用 WPS 提供的字体嵌入/打包功能（具体功能取决于 WPS 版本和字体许可）。
- 旧文档如果引用的是 `PingFang-Regular` 等旧名称，更新后可能需要在 WPS 中使用“替换字体”，将其替换为对应的 `PingFang SC` 独立字重。

## 目录结构

```text
PingFangSC/
├─ README.md
├─ PingFangSC-苹果命名独立字重说明.md
└─ ttf/
   ├─ PingFangSC-Ultralight.ttf
   ├─ PingFangSC-Thin.ttf
   ├─ PingFangSC-Light.ttf
   ├─ PingFangSC-Regular.ttf
   ├─ PingFangSC-Medium.ttf
   └─ PingFangSC-Semibold.ttf
```

## 许可说明

字体的版权和许可仍归原权利人所有。本仓库的文件整理与命名调整不会改变原字体许可；使用、分发或用于商业项目之前，请自行确认已获得适用授权。
