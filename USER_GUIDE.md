

\---



\## 文件2：USER\_GUIDE.md



\*\*位置\*\*：`D:\\班级-elite\\elite20-starter\\USER\_GUIDE.md`



\*\*操作\*\*：

1\. 用记事本打开这个文件（如果不存在就新建）

2\. 复制下面灰色框里的全部内容

3\. 粘贴进去，保存



```markdown

\# 完整使用教程



\## 安装



\### 第一步：安装Git

\- 下载：https://git-scm.com/download/win

\- 安装：一路点下一步就行

\- 验证：打开PowerShell，输入 `git --version`，看到版本号就对了



\### 第二步：克隆本仓库

```powershell

git clone https://github.com/Ltt798599368923/elite20-starter.git

cd elite20-starter

git checkout my-work





使用方法

工具1：给笔记加日期

什么时候用：每天写工作日志、会议记录、学习笔记



怎么用：



powershell

cd D:\\班级-elite\\elite-workspace

echo "你的笔记内容" >> notes.txt

.\\add\_timestamp.bat

cat notes\_timestamped.txt

工具2：整理下载文件夹

什么时候用：下载文件夹太乱，想快速分类



怎么用：



powershell

cd D:\\班级-elite\\elite-workspace

.\\organize\_downloads.bat

运行后：



今天下载的文件 → 今日下载 文件夹



之前的文件 → 历史下载 文件夹



工具3：检查环境

什么时候用：换电脑了，或者工具不工作了



怎么用：



powershell

cd D:\\班级-elite\\elite20-starter

.\\check\_env.bat



常见问题

Q：提示「无法加载文件」

A：用管理员打开PowerShell，输入 Set-ExecutionPolicy RemoteSigned



Q：中文显示乱码

A：不影响使用。可以右键记事本打开文件，选「UTF-8编码」保存



Q：git push 失败

A：先 git pull 再 git push



修改路径

如果你把文件夹放在了别的位置，需要修改脚本里的路径：



用记事本打开 organize\_downloads.bat，修改这三行：



batch

set DOWNLOAD\_DIR=C:\\你的下载文件夹路径

set TODAY\_DIR=D:\\你的工作区路径\\今日下载

set OLD\_DIR=D:\\你的工作区路径\\历史下载



目录结构

text

D:\\班级-elite\\

├── elite20-starter/           # Git仓库（放代码）

│   ├── README.md

│   ├── USER\_GUIDE.md

│   ├── check\_env.bat

│   └── artifact\_kstar.bat

└── elite-workspace/           # 工作区（放数据）

&#x20;   ├── add\_timestamp.bat

&#x20;   ├── organize\_downloads.bat

&#x20;   ├── notes.txt

&#x20;   └── notes\_timestamped.txt

