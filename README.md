# Python学习与地球动力学转型完整规划

**学生信息**
- 姓名：直博二年级构造地质学学生
- 目标：掌握Python编程，转型地球动力学数值模拟方向
- 规划时间：2026年2月6日 - 2026年7月1日

---

## 一、核心问题解答

### 1.1 编译器选择：VS Code vs Anaconda

**推荐方案：Anaconda + VS Code 组合**

**原因：**
- **Anaconda**：不是编译器，而是Python发行版，包含conda包管理器和常用科学计算库（NumPy, Matplotlib, Pandas等），非常适合科学计算
- **VS Code**：轻量级代码编辑器，配合Python插件体验极佳

**安装步骤：**
1. 先安装Anaconda（包含Python 3.11或3.12版本）
2. 再安装VS Code
3. 在VS Code中安装Python扩展

**为什么不选Jupyter Notebook作为主力？**
- Jupyter适合交互式探索和可视化，但不利于养成良好的代码组织习惯
- 建议：70%时间用VS Code写.py文件，30%时间用Jupyter做数据探索

---

### 1.2 是否需要刷题？

**答案：不需要传统刷题，但需要针对性练习**

**理由：**
- 你的目标是**科学计算**而非软件开发或算法竞赛
- LeetCode式刷题对复现地质模型帮助有限
- 应该做**领域特定练习**：处理真实地质数据、绘制图件、阅读并运行他人代码

**替代方案（占用1周而非1-2周）：**
- 第2周专门做10-15个科学计算小练习
- 重点：NumPy数组操作、Matplotlib绘图、数据文件读写
- 练习材料：GitHub上的地质数据处理案例

---

### 1.3 第一个月（3.1-3.31）详细计划

**时间分配原则：**
- 专业学习（6-8h）：上课、读文献、写作
- 编程学习（2-4h）：集中学习+练习
- 健身运动（2h）：保持体能
- 总计：10-14小时/天

**每日时间表建议：**
```
08:30-10:30  编程学习（2h）- 精力最好时学新内容
10:30-12:00  专业学习（1.5h）
12:00-14:00  午餐+休息
14:00-18:00  专业学习（4h）- 深度工作
18:00-19:00  晚餐
19:00-20:00  健身/跑步（1h）
20:00-21:00  编程练习（1h）- 复习+实践
21:00-22:00  专业学习/阅读（1h）
22:00-23:00  放松+准备睡觉
```

**周末调整：**
- 周六：增加2小时编程深度学习（如阅读源代码）
- 周日：减少1小时编程，增加休息和反思时间

---

### 1.4 何时开始大量阅读地球动力学文献？

**分阶段策略：**

**第1个月（3月）：** 
- 不读专业文献，专注Python基础
- 只看1-2篇综述了解地球动力学大图景

**第2个月（4月）：**
- 开始每周精读1篇地球动力学数值模拟文章
- 重点关注Methods部分，尝试理解代码逻辑
- 推荐期刊：*Geochemistry, Geophysics, Geosystems (G³)*, *Tectonophysics*

**第3个月（5月）：**
- 每周精读2篇，开始尝试复现简单图件
- 联系李忠海老师课题组学生，请教具体问题

**第4个月（6月）：**
- 进入高强度文献阅读（每周3-4篇）
- 开始学习Underworld或其他数值模拟框架
- 尝试修改已有代码完成小项目

**优势分析：**
- ✅ 地质学背景：理解构造过程的物理意义
- ✅ 近距离资源：李忠海课题组的经验
- ✅ 时间投入：每天2-4小时足够（关键是持续性）
- ⚠️ 需要补充：线性代数、偏微分方程基础（可在5-6月补充）

---

## 二、第一周详细计划（2.6-2.10，共5天）

### 目标
掌握Python基础语法，能编写简单脚本，为后续科学计算打基础。

---

### Day 1（2月6日，周四）：环境搭建 + Python初体验

**上午（8:30-10:30）**
1. **安装Anaconda**（30min）
   - 下载地址：https://www.anaconda.com/download
   - 安装时勾选"Add to PATH"（尽管官方不推荐，但方便初学者）
   
2. **安装VS Code**（20min）
   - 下载地址：https://code.visualstudio.com
   - 安装Python扩展（在Extensions中搜索"Python"，安装Microsoft官方版本）

3. **第一个Python程序**（30min）
   - 创建文件夹 `D:\PythonLearning\Week1`
   - 在VS Code中新建 `day1_hello.py`
   - 写入并运行：
   ```python
   # day1_hello.py - 我的第一个Python程序
   # 语言：Python 3
   # 前置知识：无
   
   print("Hello, Geodynamics!")  # print()函数用于输出文本
   
   # 计算地壳厚度（简单示例）
   moho_depth = 35  # 单位：公里（km）
   surface_elevation = 0.5
   crustal_thickness = moho_depth - surface_elevation
   
   print(f"地壳厚度: {crustal_thickness} km")  # f-string用于格式化输出
   ```

4. **学习基础概念**（50min）
   - 观看视频教程：搜索"Python入门第一课"（B站或YouTube）
   - 重点理解：变量、数据类型（int, float, str）、注释

**晚上（20:00-21:00）**
- **练习**：修改上午的代码，计算5个不同地点的地壳厚度
- **记录**：在笔记本写下今天学到的3个关键概念

**学习资源：**
- 视频：B站搜索"Python基础 第1天"
- 文档：Python官方教程中文版（https://docs.python.org/zh-cn/3/tutorial/）

---

### Day 2（2月7日，周五）：数据类型与控制流

**上午（8:30-10:30）**
1. **学习内容**（90min）
   - 列表（list）、元组（tuple）、字典（dict）
   - if-elif-else条件语句
   - for循环和while循环

2. **代码练习**（30min）
   ```python
   # day2_data_structures.py
   # 语言：Python 3
   # 前置知识：变量、基本数据类型
   # 目标：学习列表和循环，为处理地质数据做准备
   
   # 列表：存储多个数据点
   sample_depths = [100, 250, 500, 750, 1000]  # 单位：米
   temperatures = [15, 28, 45, 62, 80]  # 单位：摄氏度
   
   # 使用循环处理数据
   print("深度(m)\t温度(°C)\t地温梯度(°C/km)")
   for i in range(len(sample_depths) - 1):
       depth_diff = sample_depths[i+1] - sample_depths[i]
       temp_diff = temperatures[i+1] - temperatures[i]
       gradient = (temp_diff / depth_diff) * 1000  # 转换为°C/km
       print(f"{sample_depths[i]}\t{temperatures[i]}\t\t{gradient:.2f}")
   
   # 字典：存储键值对数据
   sample_info = {
       "location": "四川盆地",
       "max_depth": 1000,
       "surface_temp": 15,
       "rock_type": "砂岩"
   }
   
   # 条件判断
   if sample_info["max_depth"] > 800:
       print("这是深部钻探样品")
   else:
       print("这是浅部钻探样品")
   ```

**晚上（20:00-21:00）**
- **练习**：创建一个字典存储5个地质样品的信息（位置、岩性、年龄）
- **练习**：用循环判断哪些样品的年龄超过100 Ma

**注意点：**
- 列表索引从0开始（`sample_depths[0]` 是第一个元素）
- 缩进很重要！Python用缩进表示代码块
- `range(5)` 生成0-4，不包括5

---

### Day 3（2月8日，周六）：函数与模块

**上午（8:30-10:30）**
1. **学习内容**（60min）
   - 函数定义和调用
   - 参数传递（位置参数、关键字参数）
   - 返回值

2. **代码练习**（60min）
   ```python
   # day3_functions.py
   # 语言：Python 3
   # 前置知识：变量、列表、循环
   # 目标：学会编写可重用的函数
   
   def calculate_geothermal_gradient(depth1, temp1, depth2, temp2):
       """
       计算地温梯度
       
       参数:
           depth1: 第一个测点深度（米）
           temp1: 第一个测点温度（摄氏度）
           depth2: 第二个测点深度（米）
           temp2: 第二个测点温度（摄氏度）
       
       返回:
           地温梯度（°C/km）
       """
       depth_diff = depth2 - depth1
       temp_diff = temp2 - temp1
       gradient = (temp_diff / depth_diff) * 1000
       return gradient
   
   # 调用函数
   gradient1 = calculate_geothermal_gradient(100, 15, 1000, 80)
   print(f"地温梯度: {gradient1:.2f} °C/km")
   
   # 定义计算地壳密度的函数
   def crustal_density(depth_km, surface_density=2.7):
       """
       根据深度估算地壳密度（简化线性模型）
       
       参数:
           depth_km: 深度（公里）
           surface_density: 地表密度（g/cm³），默认2.7
       
       返回:
           估算密度（g/cm³）
       """
       density_increase_rate = 0.01  # 每公里增加0.01 g/cm³
       density = surface_density + depth_km * density_increase_rate
       return density
   
   # 测试
   for depth in [0, 10, 20, 30]:
       rho = crustal_density(depth)
       print(f"深度 {depth} km: 密度 {rho:.2f} g/cm³")
   ```

**下午（14:00-16:00）额外2小时深度学习**
- **导入模块**：
  ```python
  # day3_modules.py
  import math
  
  # 计算圆形岩体的体积
  radius_km = 5
  depth_km = 2
  volume = math.pi * (radius_km ** 2) * depth_km
  print(f"岩体体积: {volume:.2f} km³")
  
  # 使用别名导入
  import math as m
  angle_degrees = 45
  angle_radians = m.radians(angle_degrees)
  print(f"{angle_degrees}° = {angle_radians:.4f} 弧度")
  ```

**晚上（20:00-21:00）**
- **练习**：编写函数计算两点间距离（需要用到 `math.sqrt`）
- **练习**：编写函数判断岩石类型（根据SiO₂含量：<45%超基性，45-52%基性，52-63%中性，>63%酸性）

---

### Day 4（2月9日，周日）：文件读写 + 错误处理

**上午（8:30-10:30）**
1. **学习内容**（60min）
   - 打开和关闭文件
   - 读取文件（read, readline, readlines）
   - 写入文件
   - with语句（推荐用法）

2. **代码练习**（60min）
   ```python
   # day4_file_io.py
   # 语言：Python 3
   # 前置知识：函数、循环
   # 目标：学会读写文本文件，为处理数据文件做准备
   
   # 创建测试数据文件
   sample_data = """Sample_ID,Latitude,Longitude,SiO2,Age_Ma
   S001,30.5,104.2,68.5,120
   S002,31.2,105.8,52.3,95
   S003,29.8,103.5,71.2,150
   """
   
   # 写入文件
   with open("samples.csv", "w", encoding="utf-8") as f:
       f.write(sample_data)
   
   print("文件已创建: samples.csv")
   
   # 读取文件并处理
   with open("samples.csv", "r", encoding="utf-8") as f:
       lines = f.readlines()
       
   # 跳过表头
   for line in lines[1:]:
       parts = line.strip().split(",")  # strip()去除空白，split()按逗号分割
       sample_id = parts[0]
       sio2 = float(parts[3])
       
       # 分类岩石
       if sio2 < 45:
           rock_type = "超基性岩"
       elif sio2 < 52:
           rock_type = "基性岩"
       elif sio2 < 63:
           rock_type = "中性岩"
       else:
           rock_type = "酸性岩"
       
       print(f"{sample_id}: SiO2={sio2}%, 类型={rock_type}")
   ```

3. **错误处理**（30min）
   ```python
   # day4_error_handling.py
   # 目标：学会处理可能出现的错误
   
   try:
       depth = float(input("请输入深度(km): "))
       if depth < 0:
           raise ValueError("深度不能为负数")
       density = crustal_density(depth)
       print(f"密度: {density:.2f} g/cm³")
   except ValueError as e:
       print(f"输入错误: {e}")
   except Exception as e:
       print(f"发生未知错误: {e}")
   ```

**晚上（20:00-21:00）**
- **练习**：读取samples.csv，计算所有样品的平均SiO₂含量
- **练习**：将符合条件的样品（年龄>100 Ma）写入新文件

**注意点：**
- 始终使用 `with open()` 而非 `f = open()`，前者自动关闭文件
- `encoding="utf-8"` 避免中文乱码
- CSV文件是最常见的数据格式，后续会用Pandas更方便地处理

---

### Day 5（2月10日，周一）：综合练习 + 第一周总结

**上午（8:30-10:30）**
**综合项目：地质样品数据管理系统**

```python
# day5_project.py
# 语言：Python 3
# 前置知识：前4天所有内容
# 目标：整合所学知识完成一个小项目

class GeologicalSample:
    """地质样品类"""
    
    def __init__(self, sample_id, location, rock_type, age_ma):
        self.sample_id = sample_id
        self.location = location
        self.rock_type = rock_type
        self.age_ma = age_ma
    
    def display_info(self):
        """显示样品信息"""
        print(f"样品编号: {self.sample_id}")
        print(f"采样位置: {self.location}")
        print(f"岩石类型: {self.rock_type}")
        print(f"年龄: {self.age_ma} Ma")
        print("-" * 40)

def load_samples_from_file(filename):
    """从文件加载样品数据"""
    samples = []
    try:
        with open(filename, "r", encoding="utf-8") as f:
            lines = f.readlines()[1:]  # 跳过表头
            for line in lines:
                parts = line.strip().split(",")
                sample = GeologicalSample(
                    sample_id=parts[0],
                    location=parts[1],
                    rock_type=parts[2],
                    age_ma=float(parts[3])
                )
                samples.append(sample)
    except FileNotFoundError:
        print(f"文件 {filename} 不存在")
    return samples

def filter_by_age(samples, min_age):
    """筛选指定年龄以上的样品"""
    return [s for s in samples if s.age_ma >= min_age]

def save_samples_to_file(samples, filename):
    """保存样品数据到文件"""
    with open(filename, "w", encoding="utf-8") as f:
        f.write("Sample_ID,Location,Rock_Type,Age_Ma\n")
        for sample in samples:
            f.write(f"{sample.sample_id},{sample.location},"
                   f"{sample.rock_type},{sample.age_ma}\n")
    print(f"已保存 {len(samples)} 个样品到 {filename}")

# 主程序
if __name__ == "__main__":
    # 创建测试数据
    test_data = """Sample_ID,Location,Rock_Type,Age_Ma
S001,青藏高原,花岗岩,120
S002,华北克拉通,玄武岩,180
S003,扬子板块,片麻岩,250
S004,塔里木盆地,砂岩,85
S005,天山造山带,闪长岩,300
"""
    with open("geological_samples.csv", "w", encoding="utf-8") as f:
        f.write(test_data)
    
    # 加载数据
    all_samples = load_samples_from_file("geological_samples.csv")
    print(f"加载了 {len(all_samples)} 个样品\n")
    
    # 显示所有样品
    for sample in all_samples:
        sample.display_info()
    
    # 筛选古老样品（>150 Ma）
    old_samples = filter_by_age(all_samples, 150)
    print(f"\n找到 {len(old_samples)} 个年龄>150 Ma的样品:")
    for sample in old_samples:
        print(f"  - {sample.sample_id}: {sample.age_ma} Ma")
    
    # 保存筛选结果
    save_samples_to_file(old_samples, "old_samples.csv")
```

**晚上（20:00-21:00）**
- **第一周总结**：
  1. 回顾5天学到的内容：变量、数据类型、控制流、函数、文件操作
  2. 列出3个最困惑的问题（下周解决）
  3. 写下1个Python能帮你解决的地质学问题

---

## 三、第一周知识清单

### 已掌握的核心概念
- ✅ 变量和数据类型（int, float, str, bool）
- ✅ 容器类型（list, tuple, dict）
- ✅ 控制流（if-else, for, while）
- ✅ 函数定义和调用
- ✅ 文件读写（txt, csv）
- ✅ 错误处理（try-except）
- ✅ 基础面向对象（class）

### 重要注意事项
1. **缩进**：Python用4个空格缩进（不要用Tab）
2. **命名规范**：变量用小写+下划线（`sample_depth`），类名用驼峰（`GeologicalSample`）
3. **注释**：用 `#` 单行注释，用 `"""..."""` 文档字符串
4. **调试**：多用 `print()` 查看变量值

---

## 四、第2-4周学习路线图

### 第2周（2.11-2.17）：科学计算入门
- **Day 6-7**：NumPy基础（数组创建、索引、运算）
- **Day 8-9**：Matplotlib绘图（折线图、散点图、等值线图）
- **Day 10**：综合练习（绘制地温梯度曲线）

**关键库安装**：
```bash
# 打开Anaconda Prompt执行
conda install numpy matplotlib pandas
```

### 第3周（2.18-2.24）：数据处理与可视化
- **Day 11-12**：Pandas入门（DataFrame操作、数据清洗）
- **Day 13-14**：地质数据可视化（玫瑰图、三角图、剖面图）
- **Day 15**：项目：处理真实地球化学数据集

### 第4周（2.25-3.3）：阅读与复现代码
- **Day 16-17**：学习阅读GitHub上的地质代码
- **Day 18-19**：复现第一篇文献的简单图件
- **Day 20**：总结与反思，准备进入3月正式学期

---

## 五、3月详细计划（3.1-3.31）

### 第1周（3.1-3.7）：巩固Python + 浅层文献阅读

**编程（每天2h上午 + 1h晚上）**
- 复习前4周内容，做5个综合练习
- 开始学习SciPy库（插值、拟合、优化）
- 练习：用Python拟合地震数据

**专业学习（每天6-8h）**
- 课程学习：按学校安排
- 阅读1篇地球动力学综述（如Gerya的教科书第1-2章）
- 目的：了解数值模拟的基本思想，不求深入理解

### 第2周（3.8-3.14）：开始接触数值方法

**编程（每天2h上午 + 1h晚上）**
- 学习有限差分方法（Finite Difference）基础
- 手写代码求解一维热传导方程
- 参考：[Nicolas Coltice的教程](https://github.com/ncolrice/geodynamics-tutorials)

**专业学习（每天6-8h）**
- 继续课程学习
- 开始每周精读1篇G³或JGR文章的Methods部分

### 第3周（3.15-3.21）：向李忠海课题组学习

**编程（每天2h上午 + 1h晚上）**
- 联系李忠海课题组学生，请教学习路径
- 获取课题组推荐的入门代码（可能是I2VIS或其他）
- 尝试运行第一个简单模型

**专业学习（每天6-8h）**
- 课程学习
- 阅读李忠海老师发表的1-2篇方法学文章

### 第4周（3.22-3.31）：第一个月总结

**编程（每天2h上午 + 1h晚上）**
- 完成一个小项目：用Python模拟简单的板块冷却过程
- 总结3月的编程学习笔记

**专业学习（每天6-8h）**
- 课程学习
- 撰写3月学习总结报告（中英文各1页）

---

## 六、4-6月宏观规划

### 4月：深入数值方法 + 开始Underworld
- 学习有限元方法（Finite Element Method）基础
- 安装并运行Underworld的示例代码
- 每周精读2篇数值模拟文章
- 尝试修改参数复现文献图件

### 5月：补充数学基础 + 代码能力提升
- 补充线性代数（特征值、矩阵分解）
- 补充偏微分方程基础（建议看Gilbert Strang的公开课）
- 每周精读2篇文章，尝试复现1张图
- 开始考虑自己的科研问题

### 6月：高强度文献 + 独立项目
- 每周精读3-4篇文章
- 完成一个独立的小模型（如简单的俯冲带热结构）
- 与导师讨论转向地球动力学的可能性
- 准备暑期参加相关workshop（如果有）

---

## 七、学习资源推荐

### Python基础
- **书籍**：《Python编程：从入门到实践》（Eric Matthes）
- **视频**：B站"Python零基础入门教程"（莫烦Python）
- **官方文档**：https://docs.python.org/zh-cn/3/

### 科学计算
- **NumPy教程**：https://numpy.org/doc/stable/user/quickstart.html
- **Matplotlib图库**：https://matplotlib.org/stable/gallery/index.html
- **SciPy Lecture Notes**：https://scipy-lectures.org/

### 地球动力学
- **教科书**：
  - Gerya, T. (2019). *Introduction to Numerical Geodynamic Modelling*
  - Turcotte & Schubert. *Geodynamics* (经典教材)
- **在线课程**：
  - MIT OpenCourseWare: Geodynamics
  - Coursera: Geophysics相关课程
- **代码仓库**：
  - [Underworld 官方教程](https://github.com/underworldcode/underworld2)
  - [Geodynamic Modelling Examples](https://github.com/geodynamics)

### GitHub学习
- **廖雪峰Git教程**：https://www.liaoxuefeng.com/wiki/896043488029600
- **GitHub官方指南**：https://docs.github.com/cn

---

## 八、评估与调整机制

### 每周评估（周日晚）
1. 完成了多少学习目标？（%）
2. 遇到的最大困难是什么？
3. 下周需要调整的地方

### 每月评估（月末）
1. 编程能力提升了多少？（自评1-10分）
2. 对地球动力学的理解深入了多少？
3. 是否需要调整学习节奏或内容？

### 灵活调整原则
- 如果编程进展快，提前进入数值方法学习
- 如果专业课压力大,减少编程时间到1.5h/天
- 如果身体疲劳，优先保证睡眠和运动

---

## 九、关键里程碑

| 时间节点 | 里程碑 |
|---------|--------|
| 2月底 | 掌握Python基础语法，能读懂简单代码 |
| 3月底 | 能用NumPy/Matplotlib处理和可视化数据 |
| 4月底 | 能运行Underworld示例，理解基本参数 |
| 5月底 | 能复现1篇文献的主要图件 |
| 6月底 | 能独立修改代码完成小项目 |

---

## 十、激励与心态

### 记住你的优势
1. **地质学背景**：你理解地质过程，这是做数值模拟的核心
2. **近距离资源**：李忠海课题组就在身边，这是巨大优势
3. **时间投入**：每天2-4小时持续4个月 = 240-480小时，足够入门

### 避免的陷阱
1. ❌ 完美主义：不要期望每行代码都完美，先运行起来
2. ❌ 过度刷题：不要陷入LeetCode，聚焦科学计算
3. ❌ 孤立学习：多向师兄师姐请教，GitHub上提问

### 持续动力
- **可视化进步**：每周截图你画的图，看到进步
- **小目标奖励**：每完成一个阶段，奖励自己（如买本书、看场电影）
- **找同伴**：和同样学编程的同学组队，互相监督

---

## 十一、FAQ

**Q1: 如果第一周进度慢怎么办？**
A: 延长到10天完成，关键是理解概念，不是赶进度。

**Q2: Matlab和Python都要学吗？**
A: 先学Python，Matlab语法相似，之后1周就能上手。

**Q3: 英文文档看不懂怎么办？**
A: 用翻译工具辅助，但要习惯英文，因为代码注释和文档多是英文。

**Q4: 代码报错怎么办？**
A: (1) 仔细读错误信息 (2) 复制错误到Google/Stack Overflow搜索 (3) 用GPT/Claude帮助调试

**Q5: 什么时候可以投简历到李忠海课题组？**
A: 建议5-6月，当你能复现1-2篇文章的图，并有自己的想法时。

---

**制定者：Claude**  
**日期：2026年2月5日**  
**版本：v1.0**

*这是一份活文档，请根据实际进展定期更新和调整。*
