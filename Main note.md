# Main note

## 1. 基础操作

目录：

* 基本操作示例
* 几何建模和CAD导入
* 网格剖分
* 研究类型及求解器简介
* 结果及后处理
* 常用函数

### 1.1 基本操作示例

![截屏2022-06-29 上午9.45.16](Image_for_main_note/截屏2022-06-29 上午9.45.16.png)

#### 1.1.1 选择物理场界面

某某物理接口：在物理场选择中的某一个选项

建议一个个的加接口，方面后面查错。

#### 1.1.2 选择研究界面

具体模型具体分析

#### 1.1.3 建模界面

##### 模型开发器：参数

在COMSOL中，所有的单位都需要用[]括起来

##### 模型开发器：几何

在此处（或在工具栏）可以导入外部模型

点击设置中的“全部构建”显示所有的模型

所有之前设置的变量都会在登记在模型开发器中的“参数”中

##### 模型开发器：材料

右键单击，“从库中添加材料” ----> “内置材料” ----> 选择好后右键想添加的材料

如果库中没有想要的材料：右键单击“材料” ---> "空材料" ---> 自己设置属性参数

##### 模型开发器：组件1

右键此接口可以添加物理场

设置完后要和其他物理场进行耦合，在“多物理场”右键添加后来添加的物理场，然后选择适用的模型区域（一般是单击选择整个模型）

##### 模型开发器：某个接口（如“电流”）

已经存在的下拉列表是默认的条件，可以通过右键接口处添加其他条件（图标全填满的是域条件，半填满的是边界条件）

添加某个条件（如“接地”，边界条件），添加后点击模型选择接地的地方

在某点添加某个电压（选择“电势”，边界条件）

在未选择的模型的某一个part默认使用带“D”的接口默认条件，**要确认其他部分在默认条件下是否合理**，如果不合理，需要添加合理的条件去替代他

##### 模型开发器：网格

使用此选项对模型进行剖分

##### 模型开发器：研究

使用此选项对模型进行计算

显示变形和变形的的量：https://www.bilibili.com/video/BV1XE411P7hk?spm_id_from=333.337.search-card.all.click&vd_source=4eae4971dfe22b320ea4706b4ddcb436（第36分钟）

#### 1.1.4 App开发界面

##### app开发器：表单

右键新建表单，设置app的输入输出；通过“图形”添加其他输出的东西；通过“按钮”添加按钮。单击完成

##### 主界面

拖动模块改变其位置
