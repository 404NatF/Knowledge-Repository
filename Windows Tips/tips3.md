### 文件格式头[^1]

| 文件类型 | 文件头标识（HEX）            | 开头   | 结尾    |
| -------- | ---------------------------- | ------ | ------- |
| PNG      | `89 50 4E 47 0D 0A 1A 0A`    | PNG    | IEND    |
| RAR      | `52 61 72 21`                | RAR    |         |
| JPG;JPEG | `FF D8 FF FE 00 4A 46 49 46` | JFIF   | `FF D9` |
| GIF      | `47 49 46 38 39 61`          | GIF89a | `3B`    |

### 使用 `certutil `工具校验文件

```
certutil -hashfile file MD5
certutil -hashfile file SHA1
certutil -hashfile file SHA256
```

### 查看磁盘信息

- `diskmgmt.msc`
- `diskpart`→`list disk`

### 测量命令的执行时间

- `cmd /v:on /c "echo !TIME! & echo hello  & echo !TIME!"`
- `powershell -Command "Measure-Command {echo hi}"`

### cmd窗口中英文切换

- 中文：`chcp 936`
- 英文：`chcp 437`

### 网络共享文件夹

- 创建：高级共享设置→启用网络发现→启用文件和打印机共享→[关闭密码保护共享]；文件右键共享
- 连接：`\\192.168.1.106`

### 查看路由表

`route -h`

`route print -4`

### 查看文件权限

`Icacls test.txt `

### 查看文件属性

`attrib test.txt`

### 筛选文件类型

`dir /?`

`dir /A:D`

### 分屏显示文件输出信息

`more filename`



---

[^1]: 格式不完全相同，但开始几个字节是固定值；例如 `GIF89a` 与 `GIF87a`

