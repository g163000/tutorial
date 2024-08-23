# tutorial

#### 一、 fork作者的代码仓库: [wzdnzd/aggregator](https://github.com/wzdnzd/aggregator)

#### 二、启用 Actions 和 Gist

1. 进入刚刚 fork 的仓库，点击 [Actions](https://github.com/g163000/aggregator/actions)，启用 Actions 和相关 workflow。一般启用 Collect 和 Refresh 即可
2. [创建 Gist](https://gist.github.com/) ，内容随便填，点击 Create secret git 保存后，会跳转到另一个页面
3. 将页面 URL 的结尾部分 `g163000/b855ad776xxxxxxxxx19b6cb4d17` 复制并保存(**稍后要用**)
4. 进入[token设置](https://github.com/settings/tokens?type=beta) 页面，选择 Personal access tokens -> Fine-grained tokens
5. 点击 Generate new token 按钮，创建 PAT。Token name 随便填，Expiration 过期时间选得久一点
6. 下拉页面找到 Permissions -> Account permissions， 展开下拉框，**授予 Gists 和 Git SSH keys 选项 `Read and Write` 权限**
7. 下拉到页面最底下，点击 Generate token，复制并保存刚刚生成的 token(**稍后要用**)
8. 进入到[仓库设置](https://github.com/g163000/aggregator/settings/secrets/actions) 页面，选择 Secrets 页签，点击 Repository secrets 右边的 New repository secret 按钮，添加环境变量
9. 变量名为 `GIST_LINK` 和 `GIST_PAT`，值分别为第3步和第7步保存的内容
10. 再次回到仓库的 [Actions](https://github.com/g163000/aggregator/actions) 页面，选中左边的 Collect，点击右边的 Run workflow 下拉框里的 Run workflow 按钮
11. 手动运行第10步的测试后，是否能够正常执行并成功推送到 Gist。如果在 [Gist](https://gist.github.com/g163000) 里发现有 clash.yaml 文件，表示项目运行成功。
12. 进入刚刚生成的 [clash.yaml](https://gist.github.com/g163000/8a97ae36f29284a630c38d7237edecc5) 文件，点击右上角的 Raw 按钮，进入另一个页面。
13. 复制上一步的页面URL，并去掉 `raw/` 和 `/clash.yaml` 中间的字符串。去掉的字符串就是版本id，每次修改都会变，去掉后的 URL 就是指向最后更新的版本

```
# 第10步生成的订阅连接，但是每次执行 Actions 里的 Collect 或 Refresh 都会变
https://gist.githubusercontent.com/g163000/8a97axxxxxxxxxxedecc5/raw/befccb0aa9c22c26e50bae65c15ab2896b8f6d0b/clash.yaml

# 去掉版本id的订阅连接，这个永远指向最新的订阅连接
https://gist.githubusercontent.com/g163000/8a97axxxxxxxxxxedecc5/raw/clash.yaml
```

#### 三、转换订阅链接

1. 进入 [订阅地址转换](https://sub.cfip.gay/) 网站，将第13步复制的去掉版本id的链接，粘贴进输入框
2. 如果使用的是 [Hiddify](https://github.com/hiddify/hiddify-next/releases) 代理软件，则生成类型选择 `Sing-Box`
3. 先点击 "生成订阅连接"，再点击 "生成短连接"，将生成的长连接或短连接复制代理软件里，即可使用。
