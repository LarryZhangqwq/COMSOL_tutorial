# The Modeling Workflow

The modeling workflow consists of the following steps:

- Setting up the model environment
- Building the geometry
- Specifying material properties
- Defining physics boundary conditions
- Creating the mesh
- Running the simulation
- Postprocessing the results

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

22。59
