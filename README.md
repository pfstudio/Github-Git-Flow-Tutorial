# Github-Git-Flow-Tutorial
Github/Git工作流简单教学

## Github Flow
对于持续开发部署来说，更适合使用的是Github Flow，因为Github Flow 只需要维护一条master分支，然后通过pull request的方式进行快速开发。这里先主要写一下Github Flow ，这个也是比较常用的团队开发方式。

## Demo演示
这个项目里的文件中存在一个很明显的错误。你需要对这个文件里的代码进行修改。提出修改的步骤是这样

1. 先把项目Fork到自己的github repositories

2. 然后在自己的电脑上执行
```
git clone 你自己fork下来的仓库地址
```

3. 在clone下来的目录下执行
```
git remote add upstream 仓库源地址
```
这里的命令是为了添加一个上游地址

4. 创建fix分支并将指针指到这个分支头
```
git checkout -b fix 
```

5. 然后修改错误代码

6. 向自己的fork仓库提交改动
```
git add .
git commit -m "修改add函数Bug"
git push origin master
```

7. 在github界面进入对应自己的仓库，点击pull request(注意PR的是自己的fix分支)，按照提示点击即可。之后等待自己的PR被源仓库所有者review and merge

这样就是一个完整github flow的过程

## 可能的坑
1. 代码与自己fork的仓库代码冲突，执行
```
git pull
```

2. PR的时候与源仓库的代码冲突，执行
```
git pull upstream master
```

