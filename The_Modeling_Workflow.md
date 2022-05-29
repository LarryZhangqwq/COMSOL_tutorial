# The Modeling Workflow

The modeling workflow consists of the following steps:

- Setting up the model environment
- Building the geometry
- Specifying material properties
- Defining physics boundary conditions
- Creating the mesh
- Running the simulation
- Postprocessing the results
- Build an App

## Step 2: Building the geometry

* using "Geometry（几何）" ---> "Primitive（体素）" menu to build **or** using "import" **or** using "Home" menu（主屏幕） --->  "Geometry（几何）" ---> LiveLink
* 案例库：“File（文件）” menu ---> "Application Libraries(案例库)"
* 查看参数
  * 通过“Model Builder（模型开发器）” ---> Global Definitions ---> Parameters
* 修改参数
  * “Model Builder” ---> Component ---> Geometry x ---> Work plane x  ---> plane geometry

## Step 3: Specifying material properties(Create Definitions)

* The definitions workflow step is the most interchangeable in terms of order
  * Since definitions could be create any time( before hand or after solving a model )
  * Since their availability. 一些定义只有在其他的workflow完成之后才available

* 显式（Explicit）
  * 定义 --->  显式
  * 类似于给部件分组（根据不同的材料）
  * 选择“Explicit”之后鼠标单击选择要包含在内的材料
  * 显式设置“Setting”下的“颜色”选项可以更改颜色
  * 设置好后选择“Model Builder” ---> 定义 即可查看


## Step 4: Defining physics boundary conditions

* 选择“Material（材料）” Menu
* 选择“添加材料” ---> 选择需要添加的材料 ---> 添加到组件（Add to component）
* 单击“MB（模型开发器）”中的“材料” ---> 选择想要的材料 ---> 在Settings中的“Selection”中选择我们要把哪些部件设置为当前材料（使用的前提是在definition的步骤进行了显式分类）
* 加入的第一种材料默认将所有的部件设置为这种材料，需要添加其他材料并选择设置为新材料的部件即可替代原来的材料
* 向下滑动材料的setting ---> ”Material Contents（材料属性明细）“可以查看材料的所有属性
  * 标绿勾的是基于我们选择的物理场会用到的参数
  * 可以自己编辑数值
  * Stop提示会导致compute不能进行（在会用到的属性参数缺失时出现）
  * warning提示不会影响compute（在用不到的属性缺失时会出现）
* 对于某些材料可以通过展开他在MB中的菜单更改其参数

## Step 5: Defining physics boundary conditions 

* 选择MB材料选项之后的不同物理场进行定义
* 通过查看setting中的方程选项查看相关的物理公式
* 在MB中展开某一个物理场可以看到一些Default nodes
  * we only add the boundary conditions and constraints to our model when they are different from these default nodes
* 添加物理场：
  * 在MB中选取你想添加物理量的物理场
  * "Physics(物理场)" menu 
  * 在添加值的时候可以通过使用“[]”将想要用的符号填入其中
  * 可以回到Parameters 1中查看添加的物理场
  * 如果Parameters1中有相同的物理场大小和名称，则可以回到新建的物理场的setting中将大小设置为parameters1中有的物理场的名字(Case sensitive)
    * 使用Parameters1中的数据有俩好处：
      1. allows you to set up a parametric study later on or parametric optimization study later on if needed
      2. it becomes easy to call them when you package your finite element model into a simulation app

## Step 6: Creating the mesh

* "Mesh(网络)"Menu ---> Mesh 1 ---> “序列类型(meshing settings)”中选择”物理场控制网络“ ---> "setting"左上角的“Build all(全部构建)” 
* "Element size（单元大小）"可以设置网格的大小
  * 网格数量可以通过整个界面右下角的message中查看

## Step 7: Running the simulation

* 选择MB中的 “Study 1” ---> 在setting中更改设置 ---> setting左上角的“compute”

## Step 8: Postprocessing the results

* 选择“Result” Menu
* 在MB中选择“结果”中的某一个物理场的结果 ---> “Setting Expression（表达式）” ---> 通过更改表达式(单位) ---> 更改图中的显示
  * 其中表达式可以很花样，比如：“ cos（T*5）+ V ”
* 在“Result” Menu中可以选择“More Deririved Values(更多派生值)” 来获取更多数据

## Step 9: Build an App

* After finish the whole workflow, you can then package it into a simulation app. This is done by the Application Builder
* "Developer(开发工具)" Menu ---> “Application builder(APP开发器)” 
* 返回：左上角的"MB(模型开发器)"
* “New form” ---> 添加想要的数据和变量 --->ok
* “Test Application（测试app）” Menu 即可测试app

## 其他的功能

* APP案例库：(在APP界面)"File" Menu  ---> Application labaries
