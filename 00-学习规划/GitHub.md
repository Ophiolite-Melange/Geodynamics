# GitHub每日实战操作指南
## 适合初学者的完整工作流程（Git Bash + 网页双模式）

**你的仓库位置**：`D:\Repositories\GeodynamicsLearning\Geodynamics`  
**日期**：2026年2月6日更新

---

## 📁 第一步：建立清晰的文件夹结构

### 方案A：在本地（Windows文件资源管理器）创建文件夹

这是**最简单**的方法，适合初学者！

**操作步骤：**

1. **打开你的仓库文件夹**
   - 在文件资源管理器中打开 `D:\Repositories\GeodynamicsLearning\Geodynamics`
   - 你应该能看到 `.git`、`README.md`、`LICENSE` 等文件

2. **手动创建文件夹结构**
   - 在仓库文件夹中右键 → 新建 → 文件夹
   - 按照以下结构创建：

```
Geodynamics/                          ← 你的仓库根目录
│
├── .git/                             ← Git配置文件夹（已存在，不要动）
├── .gitignore                        ← 已存在
├── LICENSE                           ← 已存在
├── README.md                         ← 已存在
│
├── 00-学习规划/                       ← 新建这个文件夹
│   ├── Python学习与地球动力学转型规划.md
│   ├── GitHub完全上手指南.md
│   ├── 第一周任务清单.md
│   ├── 每日学习笔记模板.md
│   └── README模板.md
│
├── Week1-基础语法/                    ← 新建这个文件夹
│   ├── Day1-环境搭建/                 ← 新建子文件夹
│   ├── Day2-数据类型/
│   ├── Day3-函数模块/
│   ├── Day4-文件操作/
│   ├── Day5-综合项目/
│   └── weekly_summary.md             ← 周总结文件
│
├── Week2-科学计算/                    ← 新建这个文件夹
│   └── （第二周时再创建内容）
│
├── Projects/                         ← 新建这个文件夹
│   └── （存放综合项目）
│
└── Resources/                        ← 新建这个文件夹
    ├── datasets/                     ← 存放数据集
    └── references.md                 ← 参考资料链接
```

3. **快速创建所有文件夹的方法**：
   - 打开Git Bash，切换到仓库目录：
   ```bash
   cd /d/Repositories/GeodynamicsLearning/Geodynamics
   ```
   
   - 执行以下命令一次性创建所有文件夹：
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

4. **复制学习文档到文件夹**：
   - 把我之前给你的5份文档（.md文件）复制到 `00-学习规划/` 文件夹中

---

## 🎯 第二步：理解两种提交方式的使用场景

### 🖥️ Git Bash方式 - 适合场景：
- ✅ 每天学习结束后提交代码（**推荐日常使用**）
- ✅ 批量上传多个文件
- ✅ 提交Python代码文件
- ✅ 本地已经编辑好文件，要推送到GitHub

### 🌐 网页方式 - 适合场景：
- ✅ 快速编辑README或文档
- ✅ 在其他电脑上（如实验室电脑）临时修改
- ✅ 创建新文件夹和文件
- ✅ 简单的文字修改（不适合大量代码）

**建议**：
- **80%的时间用Git Bash**（本地编写代码 → Git推送）
- **20%的时间用网页**（快速修改文档、查看历史）

---

## 📝 每日工作流程 - 方式一：Git Bash（主要方式）

### 场景：每天学习结束后上传代码

**完整步骤（每天重复）：**

#### Step 1: 在本地编写代码

1. 今天是2月6日（Day1），你在学习环境搭建
2. 打开 `D:\Repositories\GeodynamicsLearning\Geodynamics\Week1-基础语法\Day1-环境搭建`
3. 在VS Code中创建 `day1_hello.py`，写代码
4. 创建 `notes.md`，记录学习笔记

#### Step 2: 打开Git Bash

- 方法1：在文件夹空白处右键 → "Git Bash Here"
- 方法2：打开Git Bash，用cd命令切换目录：
  ```bash
  cd /d/Repositories/GeodynamicsLearning/Geodynamics
  ```

#### Step 3: 查看修改状态

```bash
# 查看哪些文件被修改或新增
git status
```

**你会看到类似输出**：
```
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Week1-基础语法/Day1-环境搭建/day1_hello.py
        Week1-基础语法/Day1-环境搭建/notes.md

nothing added to commit but untracked files present (use "git add" to track)
```

**解读**：
- `Untracked files`：新创建的文件，Git还没追踪
- 红色文件名：未添加到暂存区

#### Step 4: 添加文件到暂存区

**方法A：添加特定文件**（推荐，更精确）
```bash
git add "Week1-基础语法/Day1-环境搭建/day1_hello.py"
git add "Week1-基础语法/Day1-环境搭建/notes.md"
```

**方法B：添加所有修改**（简单，但要小心）
```bash
git add .
```
⚠️ 注意：`.` 表示当前目录下所有文件，使用前确保没有不想上传的文件

#### Step 5: 再次查看状态（可选但推荐）

```bash
git status
```

**现在你会看到**：
```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Week1-基础语法/Day1-环境搭建/day1_hello.py
        new file:   Week1-基础语法/Day1-环境搭建/notes.md
```

**解读**：
- `Changes to be committed`：准备提交的文件
- 绿色文件名：已添加到暂存区

#### Step 6: 提交更改

```bash
git commit -m "Day1: 完成Python环境搭建和第一个程序"
```

**提交说明规范**：
- 简短描述（一行话，50字以内）
- 用动词开头：完成、添加、修复、更新
- 中文或英文都可以

**更多示例**：
```bash
git commit -m "Day1: 环境搭建完成"
git commit -m "Day2: 学习列表和循环，完成地温梯度计算"
git commit -m "Week1: 第一周总结"
git commit -m "修复day2代码中的缩进错误"
git commit -m "添加学习规划文档"
```

#### Step 7: 推送到GitHub

```bash
git push origin main
```

**如果提示错误**：
- 如果显示 `fatal: 'origin' does not appear to be a git repository`，说明还没关联远程仓库
- 解决方法见下面的"首次设置"部分

#### Step 8: 验证上传成功

1. 打开浏览器
2. 访问 https://github.com/你的用户名/仓库名
3. 刷新页面
4. 查看文件是否出现

---

## 🌐 每日工作流程 - 方式二：GitHub网页（辅助方式）

### 场景A：在网页上创建新文件

**步骤：**

1. **登录GitHub**，进入你的仓库
   - 地址：https://github.com/你的用户名/Geodynamics

2. **导航到目标文件夹**
   - 点击 `Week1-基础语法`
   - 点击 `Day1-环境搭建`

3. **创建新文件**
   - 点击右上角 "Add file" → "Create new file"

4. **输入文件名和内容**
   - 在 "Name your file..." 处输入：`day1_hello.py`
   - 在下面的编辑框输入代码：
   ```python
   # Day1: 第一个Python程序
   print("Hello, Geodynamics!")
   ```

5. **提交文件**
   - 滚动到页面底部
   - 在 "Commit new file" 处：
     - 第一个框：写提交说明，如 "添加Day1的第一个Python程序"
     - 第二个框（可选）：写详细描述
   - 点击绿色按钮 "Commit new file"

### 场景B：在网页上编辑已有文件

**步骤：**

1. **找到要编辑的文件**
   - 在仓库中点击文件，如 `README.md`

2. **点击编辑按钮**
   - 文件内容右上角有一个铅笔图标 ✏️，点击它

3. **编辑内容**
   - 直接在网页编辑器中修改文字

4. **提交更改**
   - 滚动到底部
   - 在 "Commit changes" 处写说明，如 "更新README，添加学习进度"
   - 点击 "Commit changes"

### 场景C：在网页上创建文件夹

⚠️ **重要**：GitHub网页不能直接创建空文件夹，必须在文件夹中创建文件

**步骤：**

1. 在仓库主页点击 "Add file" → "Create new file"

2. 在文件名框输入：`Week1-基础语法/Day1-环境搭建/placeholder.txt`
   - 输入第一个 `/` 后，GitHub会自动识别为文件夹
   - 继续输入下一级文件夹名和文件名

3. 在编辑框输入一些内容（如 "临时文件"）

4. 提交文件

5. 之后可以删除 `placeholder.txt`，文件夹会保留（只要里面有其他文件）

### 场景D：在网页上上传文件

**步骤：**

1. 导航到目标文件夹，如 `Week1-基础语法/Day1-环境搭建`

2. 点击 "Add file" → "Upload files"

3. **拖拽文件**到页面中间的虚线框
   - 或点击 "choose your files" 选择文件

4. 写提交说明，点击 "Commit changes"

---

## 🔄 Git Bash vs 网页 - 具体对比

| 操作 | Git Bash命令 | 网页操作 | 推荐 |
|------|-------------|---------|------|
| 创建文件夹 | `mkdir Week1-基础语法` | 无法直接创建（需创建文件） | Git Bash |
| 创建代码文件 | VS Code编写 + `git add` | "Create new file" | Git Bash |
| 上传多个文件 | `git add .` + `git commit` | "Upload files"（限100MB） | Git Bash |
| 编辑README | VS Code + Git推送 | 点击✏️直接编辑 | 网页（更快） |
| 查看历史 | `git log` | 点击"Commits" | 网页（更直观） |
| 批量提交 | `git add . && git commit` | 需逐个文件 | Git Bash |

---

## 🎬 完整示例：第一天（Day1）的操作流程

### 情景：今天是2月6日，你要完成第一天的学习

**时间：晚上20:00-21:00**

#### 本地操作（在Windows）

1. **创建今天的文件夹**：
   - 打开 `D:\Repositories\GeodynamicsLearning\Geodynamics\Week1-基础语法\Day1-环境搭建`

2. **编写代码**：
   - 在VS Code创建 `day1_hello.py`，写入：
   ```python
   # Day1: 第一个Python程序
   print("Hello, Geodynamics!")
   
   moho_depth = 35
   crustal_thickness = moho_depth - 0.5
   print(f"地壳厚度: {crustal_thickness} km")
   ```

3. **写学习笔记**：
   - 创建 `notes.md`，记录今天学到的内容

#### Git Bash操作

4. **打开Git Bash**：
   - 在仓库根目录 `D:\Repositories\GeodynamicsLearning\Geodynamics` 右键 → "Git Bash Here"

5. **查看状态**：
   ```bash
   git status
   ```

6. **添加文件**：
   ```bash
   git add "Week1-基础语法/Day1-环境搭建/day1_hello.py"
   git add "Week1-基础语法/Day1-环境搭建/notes.md"
   
   # 或者一次性添加所有
   git add .
   ```

7. **提交**：
   ```bash
   git commit -m "Day1: 完成Python环境搭建和第一个程序"
   ```

8. **推送**：
   ```bash
   git push origin main
   ```

#### 验证（在浏览器）

9. **打开GitHub**：
   - 访问 https://github.com/你的用户名/Geodynamics
   - 点击 `Week1-基础语法` → `Day1-环境搭建`
   - 检查 `day1_hello.py` 和 `notes.md` 是否出现

10. **查看提交历史**：
    - 在仓库主页点击 "X commits"（X是提交次数）
    - 应该能看到最新的提交 "Day1: 完成Python环境搭建和第一个程序"

**恭喜！你完成了第一天的完整Git工作流！** 🎉

---

## 🔧 首次设置：关联远程仓库

如果你是第一次在本地使用这个仓库，需要关联GitHub远程仓库。

### 检查是否已关联

```bash
git remote -v
```

**如果显示**：
```
origin  git@github.com:你的用户名/Geodynamics.git (fetch)
origin  git@github.com:你的用户名/Geodynamics.git (push)
```
说明已关联，跳过此步骤。

**如果显示为空**，执行以下步骤：

### 关联远程仓库

1. **获取仓库SSH地址**：
   - 打开GitHub仓库页面
   - 点击绿色 "Code" 按钮
   - 选择 "SSH" 标签
   - 复制地址（类似 `git@github.com:username/Geodynamics.git`）

2. **在Git Bash中执行**：
   ```bash
   git remote add origin git@github.com:你的用户名/Geodynamics.git
   ```

3. **验证**：
   ```bash
   git remote -v
   ```

4. **第一次推送**：
   ```bash
   git push -u origin main
   ```
   - `-u` 参数：设置上游分支，之后只需 `git push` 即可

---

## 📋 每日Git Bash操作速查表

```bash
# 1. 切换到仓库目录（如果不在的话）
cd /d/Repositories/GeodynamicsLearning/Geodynamics

# 2. 查看状态（随时可用）
git status

# 3. 添加文件到暂存区
git add "文件路径"          # 添加单个文件
git add .                  # 添加所有修改

# 4. 提交更改
git commit -m "提交说明"

# 5. 推送到GitHub
git push origin main

# 6. 查看提交历史
git log                    # 详细历史
git log --oneline          # 简洁历史

# 7. 拉取远程更新（如果在多台电脑工作）
git pull origin main

# 8. 撤销操作（慎用）
git checkout -- "文件路径"  # 撤销对文件的修改（未add）
git reset HEAD "文件路径"   # 取消暂存（已add未commit）
```

---

## 🎯 每周日晚上：周总结提交流程

### 操作步骤

1. **创建周总结文件**：
   - 在 `Week1-基础语法/` 下创建 `weekly_summary.md`
   - 内容包括：本周学习内容、完成练习、困难、下周计划

2. **提交周总结**：
   ```bash
   git add "Week1-基础语法/weekly_summary.md"
   git commit -m "Week1总结：完成Python基础语法学习"
   git push origin main
   ```

---

## ⚠️ 常见问题与解决

### 问题1：push时提示 "rejected"

**错误信息**：
```
! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'git@github.com:...'
```

**原因**：远程仓库有你本地没有的更新（如在网页上编辑了文件）

**解决**：
```bash
# 先拉取远程更新
git pull origin main

# 如果有冲突，会提示你手动解决
# 解决后：
git add .
git commit -m "解决合并冲突"

# 再推送
git push origin main
```

### 问题2：commit后想修改说明

**情况**：刚刚commit，但提交说明写错了

**解决**（仅限未push）：
```bash
git commit --amend -m "正确的提交说明"
```

### 问题3：不小心add了不该add的文件

**情况**：`git add .` 后发现添加了临时文件

**解决**：
```bash
# 取消暂存特定文件
git reset HEAD "不想提交的文件.txt"

# 取消所有暂存
git reset HEAD
```

### 问题4：忘记在哪个分支

**检查当前分支**：
```bash
git branch
```

**应该显示**：
```
* main
```
（`*` 表示当前分支）

### 问题5：中文文件名显示乱码

**解决**：
```bash
git config --global core.quotepath false
```

---

## 📊 Git工作区域理解

```
工作区（Working Directory）
  ↓ git add
暂存区（Staging Area）
  ↓ git commit
本地仓库（Local Repository）
  ↓ git push
远程仓库（Remote Repository，即GitHub）
```

**理解**：
- **工作区**：你的文件夹，VS Code编辑的地方
- **暂存区**：`git add` 后文件进入这里，准备提交
- **本地仓库**：`git commit` 后更改保存在本地
- **远程仓库**：`git push` 后上传到GitHub

---

## 🎓 渐进式学习建议

### Week 1（当前周）
- ✅ 掌握基本流程：`add → commit → push`
- ✅ 每天至少commit一次
- ✅ 80%用Git Bash，20%用网页（快速修改README）

### Week 2
- ✅ 学习查看历史：`git log`
- ✅ 学习撤销操作：`git checkout`
- ✅ 理解 `.gitignore` 文件

### Week 3
- ✅ 学习分支操作（可选）
- ✅ 在GitHub上与他人讨论（Issues）

---

## 🚀 高效技巧

### 技巧1：Git Bash快捷键

- `Ctrl + L`：清屏
- `Tab`：自动补全文件名/命令
- `↑` / `↓`：查看历史命令
- `Ctrl + C`：取消当前命令

### 技巧2：快速切换目录

在 `.bashrc` 或 `.bash_profile` 中添加别名：
```bash
alias geo='cd /d/Repositories/GeodynamicsLearning/Geodynamics'
```
之后只需输入 `geo` 就能切换到仓库目录。

### 技巧3：批量提交的简化命令

```bash
# 一行命令完成 add + commit + push
git add . && git commit -m "Day2: 学习数据类型" && git push origin main
```

⚠️ 仅在确定所有文件都要提交时使用。

---

## 📝 每日检查清单（打印出来贴在电脑旁）

**每天学习结束前（21:00）**：
- [ ] 1. 打开Git Bash，切换到仓库目录
- [ ] 2. `git status` 查看修改
- [ ] 3. `git add .` 添加所有文件
- [ ] 4. `git commit -m "DayX: 今天学习内容"` 提交
- [ ] 5. `git push origin main` 推送
- [ ] 6. 打开GitHub网页验证上传成功
- [ ] 7. 在笔记本记录今天的小结

---

## 🎯 第一周实战时间表

| 日期 | Git操作重点 | 预计用时 |
|------|-----------|---------|
| 2月6日 | 首次推送，熟悉流程 | 30分钟 |
| 2月7日 | 重复昨天流程，加深记忆 | 15分钟 |
| 2月8日 | 尝试在网页上编辑README | 15分钟 |
| 2月9日 | 练习查看历史（`git log`） | 15分钟 |
| 2月10日 | 提交周总结，完整回顾 | 20分钟 |

**目标**：一周后，Git操作成为肌肉记忆，不再需要查文档。

---

## 🔚 总结

**两种方式的黄金法则**：
1. **日常学习代码**：VS Code编写 → Git Bash推送 ⭐⭐⭐⭐⭐
2. **快速修改文档**：GitHub网页直接编辑 ⭐⭐⭐

**核心三步**：
```
本地编写 → Git提交 → 验证成功
```

**坚持七天**，Git就会成为你的日常习惯！

---

**编写：Claude**  
**日期：2026年2月6日**  
**版本：v2.0 - 实战增强版**

*有任何问题，随时在GitHub Issues提问！*
