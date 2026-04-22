# TopoClaw 第三方构建发布

用于发布 TopoClaw 的非官方预编译安装包。

## 声明

- 此目录由独立第三方维护。
- 这里的安装包不是 TopoClaw 官方发布版本。
- 与官方维护者无隶属关系，也不代表官方背书。

## 包含文件

- `TopoClaw-2.1.0.apk`（移动端/Android 安装包）
- `TopoClaw-2.1.0.exe`（桌面端/Windows 安装程序）
- `SHA256SUMS.txt`（用于完整性校验的哈希列表）

## 下载

请从 Release 资源中下载安装包文件：

- `TopoClaw-2.1.0.apk`
- `TopoClaw-2.1.0.exe`

## 校验（可选但推荐）

校验不是必须步骤，但建议执行以确认文件完整性。

1. 下载 `SHA256SUMS.txt`。
2. 在本地计算 SHA-256。
3. 将本地结果与发布的校验值比对。

### Windows（PowerShell）校验

```powershell
Get-FileHash ".\TopoClaw-2.1.0.exe" -Algorithm SHA256
Get-FileHash ".\TopoClaw-2.1.0.apk" -Algorithm SHA256
```

### macOS/Linux 校验

```bash
sha256sum TopoClaw-2.1.0.exe
sha256sum TopoClaw-2.1.0.apk
```

## 为什么要提供校验值

校验值不会阻止别人下载，它的作用是帮助用户确认：

- 文件完整（未损坏），以及
- 文件在发布后未被篡改。

