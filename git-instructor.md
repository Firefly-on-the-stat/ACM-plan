- 创建$git$仓库

  ```
  git init
  ```

- 克隆仓库

  ```
  git clone <url>
  ```

- 添加文件到暂存区

  ```
  git add <file>
  ```

  ```
  git add .(add all files)
  ```

- 删除对文件的追踪

  ```
  git remove --cached <filename>
  ```

  ```
  git remove -r --cached <foldername>
  ```

- 版本回退

  ```
  git reset --hard <version>
  ```

  ```
  git reset --hard(clear your modification, and switch to the last vesion you commit)
  ```

- 提交文件

  ```
  git commit -m "messages"
  ```

- 查看文件状态

  ```
  git status
  ```

- 查看日志

  ```
  git log
  ```

  ```
  git reflog
  ```

  ```
  git-log(alias by me)
  ```

- 查看分支

  ```
  git branch
  ```

- 创建分支

  ```
  git branch <branchname>
  ```

- 切换分支

  ```
  git checkout <branchname>
  ```

  ```
  git checkout -b <branchname>(if <branchname> doesn't exist, git will create it)
  ```

- 在当前合并其他分支

  ```
  git merge <branchname>
  ```

​	合并可能出现冲突，最后需要手动修改

- 删除分支

  ```
  git branch -d <branchname>(do some checkout before deleting)
  ```

  ```
  git branch -D <branchname>(force to delete)
  ```


- 生成$SSH$秘钥

  ```
  ssh-keygen -t rsa
  ```

- 获取公钥

  ```
  cat ~/.ssh/id_rsa.pub
  ```

- 验证配置是否成功

  ```
  ssh -T git@github.com
  ```

  ```
  ssh -T git@gitee.com
  ```

- 添加远程仓库

  ```
  git remote add <Remotename> <SSH>
  ```

- 查看远程仓库

  ```
  git remote
  ```

- 远程仓库交互

  - 上传

    $\text{-f}$表示强制覆盖

    $\text{--set-upstream}$表示推送到远端的同时建立起和远端分支的联系，下次在对应分支里直接用$\text{git push}$就会直接更新

    ```
    git push [-f] [--set-upstream] <Remotename> <Localbranchname>[:<Remotebranchname>]
    ```

  - 删除

    ```
    git push <Remotename> -d <Remotebranchname>
    ```
    
  - 抓取

    将仓库里的更新抓取到本地但不进行自动合并

    ```
    git fetch <Remotename> <branchname>
    ```
  
  - 拉取

    将仓库里的更新抓取到本地并自动进行合并

     ```
     git pull <Remotename> <branchname>
     ```

  - 克隆
  
    ```
    git clone <url> <dir>
    ```
  
  