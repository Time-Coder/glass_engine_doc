欢迎来到 Glass Engine 的文档
========================================

**Glass Engine** 是一个相当易用的 Python 3D 实时渲染引擎，完全免费开源。使用 **Glass Engine** 你可以轻松地在你的 Python 界面程序中嵌入可交互的 3D 画面。你可以从以下网址访问到项目代码和 PyPI 索引：

- `Github 项目主页 <https://github.com/Time-Coder/Glass-Engine>`_
- `Gitee 项目主页 <https://gitee.com/time-coder/Glass-Engine>`_
- `PyPI 索引 <https://pypi.org/project/glass-engine>`_

.. figure:: index/images/glass_engine_logo411.png
   :align: center
   :width: 250px

首先，使用如下命令即可完成对 **Glass Engine** 的安装：

::

    pip install glass-engine --upgrade

如果你是中国区用户，则可以使用如下命令加速其安装：

::

    pip install glass-engine --upgrade -i https://pypi.tuna.tsinghua.edu.cn/simple

接下来，让我们通过一个简单例子来直观感受一下 **Glass Engine** 的使用过程：

.. highlight:: python3

::

    from glass_engine import *
    from glass_engine.Geometries import * # 导入所有的基本几何体

    scene, camera, light, floor = SceneRoam() # 创建基本场景

    sphere = Sphere() # 创建一个球体模型
    sphere.position.z = 1 # 设置球体位置
    scene.add(sphere) # 将球体添加到场景中

    camera.screen.show() # 相机显示屏显示渲染结果

上述代码首先使用 ``SceneRoam`` 创建出一个基本场景，包括了相机、光源、地板，然后往场景中添加了一个球体模型，最后将相机观察到的视口显示出来。

可以看出，使用 **Glass Engine** 创建 3D 场景无需自定义任何类和任何函数，仅通过对象创建、方法调用的顺序程序结构就可完成场景的构建和显示，由此体现出 **Glass Engine** 高度的易用性，这也是 **Glass Engine** 相比于其他同类 3D 引擎的优势所在。

运行上述程序，你将得到图 1 所示结果：

.. figure:: index/images/start.png
   :alt: 简单场景
   :align: center
   :width: 400px

   图 1. 第一个简单场景

你可以通过鼠标右键拖动以旋转视角，还可通过键盘按键 :kbd:`W` :kbd:`A` :kbd:`S` :kbd:`D` :kbd:`E` :kbd:`C` 来在场景中漫游：

- :kbd:`A` 向左移动，:kbd:`D` 向右移动
- :kbd:`W` 向前移动，:kbd:`S` 向后移动
- :kbd:`E` 向上移动，:kbd:`C` 向下移动

并可通过鼠标滚轮来缩放场景。

怎么样，是不是很简单、直观、易用？如果你感兴趣的话，就让我们开始接下来的 3D 渲染之旅吧！

.. toctree::
   :maxdepth: 1
   :caption: 目录:

   introduce/introduce
   installation/installation
   getting_start/getting_start
   scene_graph/scene_graph
   transform/transform
   background/background
   geometries/geometries
   model/model
   color_renderhint/color_renderhint
   material/material
   lights/lights
   camera/camera
   fog/fog
   post_process_effects/post_process_effects
   manipulators/manipulators
   renderers/renderers
   animation/animation
   problems/problems
