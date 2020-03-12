# fujao-time 编辑部档案
### Markdown 格式
- [句子合集](./master.html)
- [符语本家合集](./fujaoese.html)

### JSON 格式 （便于自动操作）
JSON 接口分为 `ver.json` 和 `master.json`。  
- `ver.json` 存储版本信息和对应的 `master.json` 的 hash 值。
- `master.json` 则存储该版本中 __所有的__ 句子，也包含版本号。

推荐的调用方法是将 `master.json` 存储在本地，更新时定期请求 `ver.json` 后与本地的 `master.json` 比对版本号。
若远端版本号大于本地版本号，则拉取远端的 `master.json` 覆盖本地文件，并且可以通过 hash 校验来验证（可选）。

~~为什么不用api？因为我穷~~
