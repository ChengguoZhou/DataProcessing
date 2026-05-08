# DataProcessing

Python 数据处理与数据分析学习项目，内容覆盖 NumPy、Pandas、Matplotlib、Seaborn 以及一个完整的房地产市场分析综合案例。项目以 Jupyter Notebook 为主要载体，适合边运行代码边理解数据分析流程。

## 项目内容

项目按学习顺序拆分为多个模块：

| 目录 | 内容 |
| --- | --- |
| `01_numpy` | NumPy 基础、数组创建、索引切片、数组运算、常用统计函数 |
| `02_pandas_series` | Pandas Series 的创建、索引、切片、缺失值处理和常用操作 |
| `03_pandas_dataframe` | DataFrame 创建、筛选、排序、增删改查、类型转换 |
| `04_数据分析` | 数据读取、清洗、转换、统计分析、分组聚合等基础分析流程 |
| `05_matplotlib` | Matplotlib 绘图基础，包含折线图、柱状图、散点图、子图和图表样式设置 |
| `06_seaborn` | Seaborn 统计图表，包含分布图、箱线图、热力图、分类图等 |
| `07_房地产市场分析` | 综合案例：读取二手房数据，完成清洗、特征构造、分层分析、相关性分析和可视化 |
| `utils` | 项目公共常量和辅助代码 |

其中 `07_房地产市场分析/综合案例.ipynb` 是完整项目案例，包含：

- CSV 数据读取与字段检查
- 缺失值、重复值处理
- 面积、总价、单价、年份等字段清洗和类型转换
- 区域、楼层、户型、楼龄、直辖市标记等特征构造
- 价格分层、城市维度、户型维度、朝向维度分析
- 相关性分析与热力图
- Seaborn/Matplotlib 图表展示

## 适合学习人群

本项目适合：

- Python 基础入门后，想系统学习数据分析的学习者
- 正在学习 NumPy、Pandas、Matplotlib、Seaborn 的同学
- 想通过真实 CSV 数据练习数据清洗和可视化的人
- 需要准备数据分析课程作业、课程设计或入门作品集的人

建议具备以下基础：

- 会运行 Python 脚本或 Jupyter Notebook
- 理解变量、列表、字典、函数等 Python 基础语法
- 对表格数据、CSV 文件、统计指标有基本概念

## 主要技术

- Python 3.9+
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook / JupyterLab
- CSV 数据处理
- 数据清洗、特征工程、分组聚合、相关性分析、数据可视化

## 安装与运行

### 1. 克隆或打开项目

```bash
git clone <your-repo-url>
cd DataProcessing
```

如果已经在本地有项目，直接进入项目根目录即可。

### 2. 创建虚拟环境

Windows PowerShell：

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

macOS / Linux：

```bash
python -m venv .venv
source .venv/bin/activate
```

### 3. 安装依赖

```bash
python -m pip install --upgrade pip
python -m pip install numpy pandas matplotlib seaborn jupyter ipykernel
```

如果使用 Anaconda，也可以安装到当前 conda 环境：

```bash
conda install numpy pandas matplotlib seaborn jupyter ipykernel
```

### 4. 注册 Jupyter 内核

```bash
python -m ipykernel install --user --name data-processing --display-name "Python (DataProcessing)"
```

### 5. 启动 Jupyter

```bash
jupyter notebook
```

打开对应目录下的 `.ipynb` 文件，并选择内核：

```text
Python (DataProcessing)
```

推荐从基础模块依次学习，也可以直接运行综合案例：

```text
07_房地产市场分析/综合案例.ipynb
```

## 验证综合案例能否运行

可以在项目根目录执行：

```bash
jupyter nbconvert --to notebook --execute "07_房地产市场分析/综合案例.ipynb" --output "综合案例.executed.ipynb"
```

如果命令执行完成且没有报错，说明 notebook 可以从头到尾运行。

## 常见问题

### 1. pandas 和 numpy 版本不兼容

如果看到类似错误：

```text
this version of pandas is incompatible with numpy
```

通常是同一个 Python 环境中混装了不同来源的包。建议在同一个虚拟环境中重新安装：

```bash
python -m pip install --upgrade numpy pandas
```

或使用 conda 环境统一安装依赖。

### 2. notebook 中 import seaborn 报错

说明当前 Jupyter 内核对应的 Python 环境没有安装 Seaborn。先确认 notebook 右上角选择的内核，再在对应环境安装：

```bash
python -m pip install seaborn
```

### 3. 找不到 utils 模块

请从项目根目录启动 Jupyter，或确保 notebook 中已经把项目根目录加入 `sys.path`。综合案例 notebook 已包含路径初始化代码。

## 学习建议

推荐学习顺序：

1. `01_numpy`
2. `02_pandas_series`
3. `03_pandas_dataframe`
4. `04_数据分析`
5. `05_matplotlib`
6. `06_seaborn`
7. `07_房地产市场分析/综合案例.ipynb`

学习时建议每个 notebook 都按顺序运行，并尝试修改筛选条件、聚合指标和图表参数，加深对数据分析流程的理解。

## 参考

项目内容参考 Python 数据分析相关课程和练习材料整理，代码与案例用于学习和练习数据处理、统计分析及数据可视化。
