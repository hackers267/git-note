# 使用 SSH 代理管理本机的多个密钥

在使用 Git 进行版本控制时，我们通常需要使用 SSH 密钥进行身份验证。如果您在同一台计算机上管理多个 Git 存储库，并使用不同的 SSH 密钥对这些存储库进行身份验证，那么您可以使用 SSH 代理来管理多个密钥。

## 如何查看 key 是否添加到了 ssh 代理中

您可以使用以下命令来查看已经添加到 SSH 代理中的密钥列表：
```bash
ssh-add -l
```
如果您想查看指定的 SSH 密钥是否已添加到 SSH 代理中，可以使用以下命令：
```bash
ssh-add -L | grep <ssh-key-fingerprint>
```
其中，<ssh-key-fingerprint> 是您要查看的 SSH 密钥的指纹值。

## 如何使用 SSH 代理管理多个密钥

如果您需要在不同的存储库中使用不同的 SSH 密钥，则可以为每个存储库配置不同的 SSH 密钥。以下是使用 SSH 代理管理多个密钥的步骤：

将要使用的所有 SSH 密钥添加到 SSH 代理中，可以使用以下命令：
```bash
ssh-add ~/.ssh/key1
ssh-add ~/.ssh/key2
```
其中，~/.ssh/key1 和 ~/.ssh/key2 是您要添加的 SSH 密钥文件的路径。

将 SSH 密钥的公钥文件添加到您的 Git 存储库的 SSH 密钥列表中。

在您的 Git 存储库的配置文件中指定要使用的 SSH 密钥。例如，使用以下命令将存储库的 URL 更改为使用 SSH 协议：
```bash
git remote set-url origin git@github.com:username/repo.git
```
其中，username 是您的 GitHub 用户名，repo 是您要使用的存储库的名称。

现在，您可以使用 Git 命令进行身份验证，Git 将使用指定的 SSH 密钥进行身份验证。

> 注意：如果您要管理多个 SSH 密钥，您需要确保每个密钥的公钥已添加到您要访问的每个 Git 存储库的 SSH 密钥列表中。这样，当您使用 Git 进行身份验证时，Git 将能够正确找到密钥。
