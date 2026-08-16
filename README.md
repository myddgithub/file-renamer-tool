# 文件批量重命名工具

一个单文件 HTML 工具：选文件夹后，可用 **Excel 对照** 或 **命名规则** 批量改名，预览后再应用，支持回滚。

所有操作都在本地浏览器完成，文件不会上传到任何服务器。

在线打开（Chrome / Edge）：  
https://myddgithub.github.io/file-renamer-tool/

或下载 [`file-renamer-tool.html`](./file-renamer-tool.html)，用 Chrome / Edge 打开。

## 怎么用

1. 用 **Chrome 或 Edge** 打开上面的页面，或打开下载的 HTML。
2. 选择（或拖入）要改名的文件夹，允许读写。
3. 可选：拖入 Excel / CSV，指定「原名列」「新名列」。
4. 可选：勾选规则（前缀、后缀、日期、简繁、替换、序号等）。
5. 看预览，确认后点「应用重命名」。

Excel 对照结果会再套用已勾选的规则。  
`新名 = 表格新名 +（可选 _附加信息）+ 原扩展名`，同一主名的 `.wav` / `.mp4` / `.TextGrid` 会一起改。

## 回滚

每次改名会在该文件夹写入 `.rename_history.json`。  
关掉浏览器后再打开本工具、选回同一文件夹，仍可「撤销上一次」或「全部回滚」。

## 说明

- 真正写回磁盘需要 Chrome / Edge（File System Access API）。
- 读 Excel、简繁转换会从 CDN 加载脚本，这两项首次使用需要能访问网络。
- 规则预设存在本机浏览器里，不会跟着 HTML 文件走。

## 许可

MIT。可自由下载、使用、修改。
