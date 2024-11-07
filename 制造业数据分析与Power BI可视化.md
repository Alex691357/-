# 制造业数据分析与Power BI可视化

## 确定数据源

  首先，本项目的目标是分析制造业的相关数据集，以利用 Power BI Desktop 进行可视化展示。在本项目中，我使用了来自 **Kaggle** 网站的公开数据集。Kaggle 是一个提供各种公开数据集的平台，涵盖了多个行业和应用场景。
  
### 数据集获取步骤
1. **搜索数据集**：
   - 在 Kaggle 网站上，通过搜索 **manufacturing** 等关键词。
   - ![image](https://github.com/user-attachments/assets/baf82345-ef65-4f6f-9642-1e057257b5cd)
   - 在筛选里选择**datasets**。
     
2. **确认数据集信息**：
   - 在选择数据集之前，查看数据集的描述和字段信息，以确保它符合项目需求。本数据集包含以下关键字段：
     - `product_id`：产品的唯一标识符。
     - `defect_type`：缺陷的类型。
     - `inspection_method`：用于检测缺陷的方法。
     - `repair_cost`：修理该缺陷的费用。
     - `date`：缺陷被检测到的日期。

3. **下载数据**：
   - 进入数据集页面后，选择所需的文件（如 CSV 文件），点击 **“Download”** 按钮下载到本地。
  ![image](https://github.com/user-attachments/assets/53a985b9-fe1c-4a5c-8e70-626575b710ce)

## 数据导入与清洗

在进行数据分析之前，首先需要将数据集导入到 Power BI 并进行初步清洗和准备，以确保数据适合分析。

### 1. 数据导入
将下载的 CSV 数据集导入到 Power BI Desktop 中，确保数据已正确加载并可用。

### 2. 数据清洗与准备
## 数据导入与清洗

在 Power BI 的 **Power Query Editor** 中进行数据清洗，本数据集包括 2024 年 1-6 月的数据，为了方便制表和分析，使用 DAX 生成一个名为 **month** 的列。

## 前置美术设计
本项目的前置美术工作包括：
1.寻找 **排版设计灵感**：
   - 前往 **Freepik** 网站，寻找报表排版灵感。
2. **获取背景图片**：
   - 在 Freepik 上下载符合报表主题的高质量背景图片。
3. **主题色提取**：
   - 利用 **Adobe Color** 工具从选定的设计模板中提取主题色。
   - 通过上传背景图片至 Adobe Color，分析并生成主色调及其配色方案，然后将这些色彩应用于 Power BI 报表的图表、文字和背景中。

## 可视化报表

在完成前期准备工作后，进入 Power BI 可视化报表的制作过程。

1. **导入背景图片**：
   - 将选定的背景图片导入到 Power BI 报表页面中，设置为页面背景，并调整透明度和对齐方式，使数据和图表在背景上清晰可见。

2. **应用主题色**：
   - 使用 Adobe Color 提取的主题色，将这些颜色应用到 Power BI 的视觉对象中，如图表、文字和卡片，确保整个报表的色彩风格统一、协调。
  
## 创建衡量值

在本项目中，利用DAX公式创建了多个衡量值来支持数据分析和可视化，具体如下：

1. **Average Repair Cost**：计算了平均修理成本，用于分析整体的修理费用水平。
2. **CriticalDefectCount**：统计了严重缺陷的数量，以便分析高风险产品的分布。
3. **HighestRepairCost** 和 **LowestRepairCost**：分别创建了衡量值来确定最高和最低修理成本，用于识别极值情况。
4. **Total Repair Cost - Critical/Minor/Moderate**：按缺陷严重程度计算的修理总成本，帮助区分不同严重等级的成本。
5. **Defect Count by Inspection Method/Location/Product/Type**：按检测方法、位置、产品和缺陷类型进行的缺陷数量统计，用于多维度分析缺陷分布。
6. **ProductWithMostDefects**：识别出缺陷最多的产品。
7. **Total Defects**：计算了总缺陷数量，用于展示数据的整体缺陷情况。
8. **Monthly Defects**：按月份统计缺陷数量，分析缺陷随时间的趋势。
9. **Minor/Moderate/Critical Defects Count**：统计了不同缺陷级别的数量，以便对比分析各级别缺陷的分布。

## 利用已有数据进行可视化创建

1. **折线图**：
   - 下图展示了 2024 年 1 月至 6 月的实际月度缺陷数量，并对未来 6 个月进行了预测。
   - ![image](https://github.com/user-attachments/assets/062a47b3-7798-40b3-985d-15099957b759)
  
2. **切片器**：
   - 下图展示了用于数据筛选的三个切片器，分别为 **Month（月份）**、**Severity（严重程度）** 和 **Inspection Method（检测方法）**。
     ![image](https://github.com/user-attachments/assets/e788afa4-8fab-453e-bf49-24566084f05f)

3. **卡片视图**：
   - 下图展示了三个卡片视图，分别显示了 **Average Repair Cost（平均修理成本）**、**Lowest Repair Cost（最低修理成本）** 和 **Highest Repair Cost（最高修理成本）**。
   - ![image](https://github.com/user-attachments/assets/0b8c4939-27a6-4b62-be1a-ea6dbb97866f)
     
4. **条形图：Inspection Method（按 Defect Type）**：
   - ![image](https://github.com/user-attachments/assets/32cd5a98-82d2-4aae-b7f8-f5132936d704)

5. **柱状图 2：Defect Count by Severity**：
   - ![image](https://github.com/user-attachments/assets/94256c75-59c6-435e-93bf-a38bbe16460e)




    


  
   

