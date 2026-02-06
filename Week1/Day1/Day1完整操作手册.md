# Day1（2月6日）完整操作手册
## 从零开始的Git实战 - 包含每一个点击和命令

**目标**：今晚21:00前完成第一次Git提交  
**预计时间**：1小时（包括学习和操作）

---

## 📋 今晚要做的事（按顺序）

### ✅ 任务清单
- [ ] 任务1：创建文件夹结构（15分钟）
- [ ] 任务2：复制学习文档（5分钟）
- [ ] 任务3：创建Day1代码文件（10分钟）
- [ ] 任务4：第一次Git提交（15分钟）
- [ ] 任务5：验证GitHub上传成功（5分钟）
- [ ] 任务6：写今日总结（10分钟）

---

## 📁 任务1：创建文件夹结构（15分钟）

### 步骤1.1：打开仓库文件夹

1. 按 `Win + E` 打开文件资源管理器
2. 在地址栏输入：`D:\Repositories\GeodynamicsLearning\Geodynamics`
3. 按回车

**你应该看到**：
- `.git` 文件夹（可能是隐藏的）
- `.gitignore` 文件
- `LICENSE` 文件
- `README.md` 文件

### 步骤1.2：用Git Bash创建所有文件夹

1. 在当前文件夹空白处右键 → 选择 "**Git Bash Here**"
   
2. 在弹出的黑色窗口（Git Bash）中，**复制粘贴**以下命令并按回车：

```bash
mkdir -p "00-学习规划"
mkdir -p "Week1-基础语法/Day1-环境搭建"
mkdir -p "Week1-基础语法/Day2-数据类型"
mkdir -p "Week1-基础语法/Day3-函数模块"
mkdir -p "Week1-基础语法/Day4-文件操作"
mkdir -p "Week1-基础语法/Day5-综合项目"
mkdir -p "Week2-科学计算"
mkdir -p "Projects"
mkdir -p "Resources/datasets"
```

3. 按回车后，看到新的命令提示符（如 `username@DESKTOP-XXX MINGW64 ...`），说明执行成功

4. 验证：在文件资源管理器中刷新（按F5），应该能看到新建的文件夹

**截图时刻**：用手机拍一张文件夹结构的照片，记录你的第一步！📸

---

## 📄 任务2：复制学习文档（5分钟）

### 步骤2.1：找到之前下载的文档

1. 打开你保存那5份Markdown文档的位置（如"下载"文件夹）
2. 找到以下文件：
   - `Python学习与地球动力学转型规划.md`
   - `GitHub完全上手指南.md`
   - `GitHub每日实战操作指南-新版.md`
   - `第一周任务清单.md`
   - `每日学习笔记模板.md`
   - `README模板.md`

### 步骤2.2：复制到仓库

1. 全选这6个文件（Ctrl + A）
2. 复制（Ctrl + C）
3. 打开 `D:\Repositories\GeodynamicsLearning\Geodynamics\00-学习规划`
4. 粘贴（Ctrl + V）

**验证**：`00-学习规划` 文件夹中应该有6个.md文件

---

## 💻 任务3：创建Day1代码文件（10分钟）

### 步骤3.1：打开VS Code

1. 打开VS Code
2. 点击左上角 "文件" → "打开文件夹"
3. 选择 `D:\Repositories\GeodynamicsLearning\Geodynamics`
4. 点击"选择文件夹"

**你应该看到**：左侧文件资源管理器显示仓库的所有文件夹

### 步骤3.2：创建第一个Python文件

1. 在左侧文件树中，展开 `Week1-基础语法` → `Day1-环境搭建`
2. 右键点击 `Day1-环境搭建` → "新建文件"
3. 输入文件名：`day1_hello.py`
4. 按回车

### 步骤3.3：编写代码

在 `day1_hello.py` 中输入以下代码：

```python
# day1_hello.py - 我的第一个Python程序
# 日期：2026年2月6日
# 作者：[你的名字]

print("Hello, Geodynamics!")
print("这是我的Python学习之旅的开始")

# 计算地壳厚度
moho_depth = 35  # 莫霍面深度（公里）
surface_elevation = 0.5  # 地表高程（公里）
crustal_thickness = moho_depth - surface_elevation

print(f"\n地壳厚度计算：")
print(f"莫霍面深度：{moho_depth} km")
print(f"地表高程：{surface_elevation} km")
print(f"地壳厚度：{crustal_thickness} km")

# 练习：计算不同地点的地壳厚度
locations = ["青藏高原", "华北平原", "四川盆地"]
moho_depths = [70, 35, 42]

print(f"\n不同地点的地壳厚度：")
for i in range(len(locations)):
    thickness = moho_depths[i] - 0.5
    print(f"{locations[i]}：{thickness} km")
```

5. 按 `Ctrl + S` 保存文件

### 步骤3.4：运行代码（验证）

1. 在VS Code中，右键点击代码编辑器 → "在终端中运行Python文件"
2. 或者按 `Ctrl + F5` 直接运行

**你应该看到输出**：
```
Hello, Geodynamics!
这是我的Python学习之旅的开始

地壳厚度计算：
莫霍面深度：35 km
地表高程：0.5 km
地壳厚度：34.5 km

不同地点的地壳厚度：
青藏高原：69.5 km
华北平原：34.5 km
四川盆地：41.5 km
```

**恭喜！你的第一个Python程序成功运行！** 🎉

### 步骤3.5：创建学习笔记

1. 在 `Day1-环境搭建` 文件夹右键 → "新建文件"
2. 输入文件名：`notes.md`
3. 复制以下模板并填写：

```markdown
# Day1 学习笔记

**日期**：2026年2月6日  
**学习时长**：晚上20:00-21:00 = 1小时  
**主题**：Python环境搭建 + 第一个程序

---

## 📚 今日学习内容

### 完成的任务
1. ✅ 安装Anaconda（已完成/今天完成）
2. ✅ 安装VS Code + Python扩展
3. ✅ 创建GitHub仓库并建立文件夹结构
4. ✅ 编写第一个Python程序
5. ✅ 学习Git基本操作

### 核心概念
1. **变量**：存储数据的容器，如 `moho_depth = 35`
2. **print()函数**：输出文本到屏幕
3. **f-string**：格式化字符串，如 `f"厚度：{thickness} km"`
4. **列表**：存储多个数据，如 `locations = ["青藏高原", "华北平原"]`
5. **for循环**：重复执行代码

---

## 💻 今日代码练习

完成了 `day1_hello.py`，包括：
- 简单的print输出
- 变量赋值和计算
- 使用列表和循环计算多个地点的地壳厚度

**运行结果**：成功输出3个地点的地壳厚度 ✅

---

## 🎯 关键收获

1. Python的语法比想象中简单，不需要声明变量类型
2. 缩进很重要，for循环里的代码必须缩进
3. VS Code的代码提示很好用，会自动补全

---

## ❓ 遇到的问题

### 问题1：第一次运行代码时找不到Python
**解决**：在VS Code中选择了Anaconda的Python解释器（Ctrl+Shift+P → "Python: Select Interpreter"）

### 问题2：不知道如何在VS Code中运行代码
**解决**：右键 → "在终端中运行Python文件"

---

## 📝 明天计划

1. 学习列表（list）和字典（dict）
2. 学习for循环和if-else
3. 完成地温梯度计算练习

---

**学习状态**：😊 顺利  
**精力状态**：⚡ 充沛  
**信心指数**：★★★★☆ (4/5)
```

4. 按 `Ctrl + S` 保存

---

## 🔄 任务4：第一次Git提交（15分钟）⭐ 最重要！

### 步骤4.1：打开Git Bash

**方法1（推荐）**：
- 在仓库文件夹 `D:\Repositories\GeodynamicsLearning\Geodynamics` 空白处右键
- 选择 "**Git Bash Here**"

**方法2**：
- 打开开始菜单，搜索 "Git Bash"
- 打开后输入：`cd /d/Repositories/GeodynamicsLearning/Geodynamics`

### 步骤4.2：查看仓库状态

在Git Bash中输入：
```bash
git status
```

**你会看到类似输出**（红色文字）：
```
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        00-学习规划/
        Week1-基础语法/
        Week2-科学计算/
        Projects/
        Resources/

nothing added to commit but untracked files present (use "git add" to track)
```

**解读**：
- `Untracked files`：Git发现了新文件，但还没有追踪
- 红色表示未添加到暂存区

### 步骤4.3：添加所有文件到暂存区

输入命令：
```bash
git add .
```

**注意**：
- `add` 后面有一个空格，然后是一个英文句号 `.`
- `.` 表示当前目录下的所有文件

**按回车后**，等待几秒（如果文件多可能需要5-10秒）

### 步骤4.4：再次查看状态（验证）

```bash
git status
```

**现在你会看到**（绿色文字）：
```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   00-学习规划/GitHub完全上手指南.md
        new file:   00-学习规划/Python学习与地球动力学转型规划.md
        ... (更多文件)
        new file:   Week1-基础语法/Day1-环境搭建/day1_hello.py
        new file:   Week1-基础语法/Day1-环境搭建/notes.md
```

**解读**：
- `Changes to be committed`：准备提交的文件
- 绿色表示已添加到暂存区，随时可以commit

### 步骤4.5：提交更改

输入命令：
```bash
git commit -m "Day1: 完成仓库结构搭建、学习文档上传和第一个Python程序"
```

**按回车后**，你会看到类似输出：
```
[main xxxxxxx] Day1: 完成仓库结构搭建、学习文档上传和第一个Python程序
 X files changed, XXX insertions(+)
 create mode 100644 Week1-基础语法/Day1-环境搭建/day1_hello.py
 create mode 100644 Week1-基础语法/Day1-环境搭建/notes.md
 ...
```

**解读**：
- `X files changed`：有X个文件被修改
- `XXX insertions(+)`：添加了XXX行代码
- 每个 `create mode` 表示创建了一个新文件

### 步骤4.6：推送到GitHub

输入命令：
```bash
git push origin main
```

**第一次推送可能会提示**：
```
The authenticity of host 'github.com (xxx.xxx.xxx.xxx)' can't be established.
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```

**输入 `yes` 并按回车**

**然后会看到类似输出**：
```
Enumerating objects: XX, done.
Counting objects: 100% (XX/XX), done.
Delta compression using up to 8 threads
Compressing objects: 100% (XX/XX), done.
Writing objects: 100% (XX/XX), XXX KiB | XXX MiB/s, done.
Total XX (delta X), reused 0 (delta 0), pack-reused 0
To github.com:你的用户名/Geodynamics.git
   xxxxxxx..yyyyyyy  main -> main
```

**看到 `main -> main` 说明推送成功！** ✅

---

## ✅ 任务5：验证GitHub上传成功（5分钟）

### 步骤5.1：打开GitHub仓库

1. 打开浏览器（Chrome/Edge/Firefox）
2. 访问 https://github.com
3. 登录你的账号
4. 点击右上角头像旁边的下拉菜单
5. 选择 "Your repositories"
6. 点击 `Geodynamics` 仓库

### 步骤5.2：检查文件

**你应该看到**：
- `00-学习规划` 文件夹
- `Week1-基础语法` 文件夹
- `Week2-科学计算` 文件夹
- `Projects` 文件夹
- `Resources` 文件夹
- 原有的 `README.md`、`LICENSE`、`.gitignore`

### 步骤5.3：深入检查代码文件

1. 点击 `Week1-基础语法`
2. 点击 `Day1-环境搭建`
3. 你应该能看到：
   - `day1_hello.py`
   - `notes.md`
4. 点击 `day1_hello.py`，查看代码是否完整

**如果能看到代码，说明上传成功！** 🎉

### 步骤5.4：查看提交历史

1. 返回仓库主页
2. 查找页面上的 "**X commits**" （X是数字，如 "2 commits"）
3. 点击它
4. 你应该能看到最新的提交：
   - 提交说明："Day1: 完成仓库结构搭建、学习文档上传和第一个Python程序"
   - 时间：刚才的时间
   - 作者：你的GitHub用户名

**截图时刻**：截图你的第一次提交记录，这是你的编程学习里程碑！📸

---

## 📝 任务6：写今日总结（10分钟）

在你的实体笔记本或电子文档中写下：

```
=== 2026年2月6日 Python学习第一天 ===

今天完成的事：
1. ✅ 创建了GitHub仓库的完整文件夹结构
2. ✅ 上传了所有学习规划文档
3. ✅ 编写并运行了第一个Python程序
4. ✅ 学会了Git的基本操作：add → commit → push
5. ✅ 成功推送到GitHub

学到的核心技能：
- Python基础：变量、print、列表、循环
- Git操作：git add, git commit, git push
- VS Code的使用

明天要做的事：
1. 学习列表和字典
2. 练习for循环和if-else
3. 完成地温梯度计算

今日感想：
[写下你的真实感受，如"第一次用Git有点紧张，但成功后很有成就感！"]

信心指数：★★★★☆
```

---

## 🎉 恭喜！你完成了Day1的所有任务！

### 今天的成就：
- ✅ 建立了完整的学习仓库结构
- ✅ 编写了第一个Python程序
- ✅ 掌握了Git的基本操作流程
- ✅ 在GitHub上留下了第一个代码提交

### 今晚的Git命令回顾：
```bash
git status      # 查看状态
git add .       # 添加所有文件
git commit -m "说明"  # 提交
git push origin main  # 推送到GitHub
```

### 明天（2月7日）的Git操作会更简单：
因为文件夹结构已经建好，明天只需要：
1. 在Day2文件夹中写代码
2. 四行命令：`git status` → `git add .` → `git commit` → `git push`
3. 10分钟搞定！

---

## 🌟 给自己的话

今天是你Python和Git学习的第一天，虽然有些命令可能还不熟悉，但你已经迈出了最重要的一步。记住：

> **"千里之行，始于足下"**

每一次commit都是进步，每一行代码都是成长。坚持下去，一个月后你会感谢今天努力的自己！

---

**明天见！记得在相同时间（晚上20:00-21:00）继续学习！** 💪

---

**编写：Claude**  
**专为Day1学习者设计**  
**日期：2026年2月6日**
