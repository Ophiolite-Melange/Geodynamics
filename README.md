# Python与地球动力学学习记录

<div align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![Status](https://img.shields.io/badge/Status-Learning-green.svg)
![Start Date](https://img.shields.io/badge/Start-2026.02.06-orange.svg)

**从零开始的Python学习与地球动力学数值模拟转型之路**

[学习规划](./Python学习与地球动力学转型规划.md) • [GitHub指南](./GitHub完全上手指南.md) • [每周总结](#每周学习总结)

</div>

---

## 📖 项目简介

这是我作为中国科学院大学构造地质学直博二年级学生，从2026年2月6日开始的Python编程学习和地球动力学数值模拟方向转型的完整记录。

### 学习背景
- **专业**：构造地质学（大地构造方向）
- **目标**：掌握Python编程，能够复现文献中的地球动力学数值模型
- **时间规划**：2026年2月 - 7月（5个月集中学习）
- **每日投入**：2-4小时编程学习

### 核心目标
1. ✅ **3-4周内**掌握Python基础语法和科学计算库（NumPy, Matplotlib, Pandas）
2. ✅ **2个月内**能够阅读并运行地球动力学源代码
3. ✅ **4个月内**能够复现文献中的数值模拟图件
4. ✅ **5个月内**完成一个独立的小型数值模拟项目

---

## 🗂️ 仓库结构

```
Python-Geodynamics-Learning/
│
├── README.md                                # 本文件
├── Schedule.md                              # 完整学习规划
├── Daily notebooks.md                        # 学习笔记模板
│
├── Week1-基础语法/                            # 第1周：Python基础
│   ├── Day1-环境搭建/
│   │   ├── day1_hello.py
│   │   └── notes.md
│   ├── Day2-数据类型/
│   ├── ...
│   └── weekly_summary.md
│
├── Week2-科学计算入门/                        # 第2周：NumPy & Matplotlib
│   └── ...
│
├── Week3-数据处理/                            # 第3周：Pandas & 可视化
│   └── ...
│
├── Week4-代码复现/                            # 第4周：阅读与复现
│   └── ...
│
├── Projects/                                 # 综合项目
│   ├── 01-地质样品管理系统/
│   ├── 02-地温梯度可视化/
│   └── 03-简单俯冲带模型/
│
└── Resources/                                # 学习资源
    ├── datasets/                            # 数据集
    ├── papers/                              # 相关文献
    └── references.md                        # 参考资料汇总
```

---

## 📅 学习进度

### 第一阶段：Python基础（2.6 - 3.3，4周）

| 周次 | 时间 | 主题 | 状态 | 完成度 |
|------|------|------|------|--------|
| Week 1 | 2.6-2.10 | Python基础语法 | 🔄 进行中 | ![](https://progress-bar.dev/20/) |
| Week 2 | 2.11-2.17 | NumPy & Matplotlib | ⏳ 待开始 | ![](https://progress-bar.dev/0/) |
| Week 3 | 2.18-2.24 | Pandas & 数据可视化 | ⏳ 待开始 | ![](https://progress-bar.dev/0/) |
| Week 4 | 2.25-3.3 | 代码阅读与复现 | ⏳ 待开始 | ![](https://progress-bar.dev/0/) |

### 第二阶段：深入学习（3月 - 7月）

| 月份 | 重点内容 | 状态 |
|------|----------|------|
| 3月 | 巩固基础 + SciPy + 有限差分法 | ⏳ 待开始 |
| 4月 | 数值方法 + Underworld入门 | ⏳ 待开始 |
| 5月 | 数学基础 + 代码能力提升 | ⏳ 待开始 |
| 6月 | 文献阅读 + 独立项目 | ⏳ 待开始 |

---

## 🏆 学习成果展示

### Week 1
- [x] 完成Python环境搭建（Anaconda + VS Code）
- [x] 第一个Python程序：地壳厚度计算
- [ ] 地质样品管理系统（Day 5）

#### 代码示例
```python
# 地温梯度计算
def calculate_geothermal_gradient(depth1, temp1, depth2, temp2):
    gradient = ((temp2 - temp1) / (depth2 - depth1)) * 1000
    return gradient
```

#### 图表展示
（这里放你绘制的图，如地温梯度曲线）

---

## 📝 每周学习总结

### 📌 Week 1 总结（2.6-2.10）
**主题**：Python基础语法

**完成内容**：
- ✅ 安装Anaconda和VS Code
- ✅ 学习变量、数据类型、列表、字典
- ✅ 掌握if-else、for循环
- ✅ 学会定义函数和读写文件
- ✅ 完成3个地质相关的练习

**关键收获**：
1. Python语法比想象中简洁，缩进很重要
2. 列表和字典非常适合存储地质数据
3. 函数可以让代码更模块化和可重用

**遇到的困难**：
- 初期对缩进不习惯，导致几次IndentationError
- 文件读写时编码问题（通过`encoding='utf-8'`解决）

**下周计划**：
- 开始学习NumPy数组操作
- 用Matplotlib绘制第一张地质图表

[查看详细总结](./Week1/weekly_summary.md)

---

## 🔗 重要资源链接

### 学习材料
- [Python官方教程](https://docs.python.org/zh-cn/3/tutorial/)
- [NumPy教程](https://numpy.org/doc/stable/user/quickstart.html)
- [Matplotlib图库](https://matplotlib.org/stable/gallery/index.html)
- [地球动力学模拟入门](https://github.com/underworldcode/underworld2)

### 参考文献
- Gerya, T. (2019). *Introduction to Numerical Geodynamic Modelling*
- 李忠海等. 地球动力学数值模拟相关论文（见Resources/papers/）

### 课程组资源
- 李忠海课题组GitHub（待添加）
- 课题组内部分享材料（待整理）

---

## 💬 联系与交流

- **GitHub Issues**：欢迎提问、讨论或提供建议
- **邮箱**：[你的邮箱]（可选填写）

如果你也在学习Python用于地质学/地球物理研究，欢迎一起交流！

---

## 📊 统计信息

- **开始日期**：2026年2月6日
- **总学习天数**：`X` 天（自动统计）
- **代码提交次数**：`Y` 次（查看[Commits](../../commits/main)）
- **完成练习数**：`Z` 个

---

## 🙏 致谢

感谢：
- Claude，ChatGPT，Gemini，Grok，Manus，Deepseek，Kimi，豆包等等，提供学习规划和答疑
- GitHub社区，提供丰富的开源资源

---

## 📜 License

本仓库代码采用 [MIT License](./LICENSE)，欢迎学习和使用。

---

<div align="center">

**"编程改变地质学研究的方式"**

*最后更新：2026年2月5日*

</div>
