# 这是FreeCAD For Inventors随书例子的模型文件

我用中文界面的FreeCAD 0.17版重新做了一遍。

## [关于FreeCAD For Inventors这本书](https://forum.freecadweb.org/viewtopic.php?f=40&t=31900#p265446)
Oct 29, 2018 3:57 pm

### 关于作者

Brad Collette，在论坛上的名字是Sliptonic，他2010年就参加了FreeCAD项目，是CAM功能PATH工作台的主程。他在2013年就合著过第一本商业发行的FreeCAD图书《FreeCAD [How-to] Solid Modeling with the Power of Python》。

### 目标对象

面向广义上的工匠，不限于机械和建筑等特定行业，不限于工程师和设计师等特定职业。哪怕是中小学生，只要你有一个想法，需要三维模型，以便做后续的分析和输出，那就可以借用FreeCAD这个工具的帮助。

本书名称虽然有发明者，但是不讲发明的思考过程，只是给发明者介绍一个有用的工具箱。本书虽然教FreeCAD，但是并非实例套路，也不是大全指南，只介绍对发明者有用的功能，让他们先知其有，再自己深入探索。

总之，本书就像是给新厨师的粤系菜谱，“师父领进门，修行在个人”。

### 篇章结构

本书正文有十五章，分为三部分。附录部分另有四章。

第一部分是概念，介绍三维建模的基本概念和建模经验。三维工具长什么样，有没有表达式和引用，传统2D绘图怎么用，传统3D建模怎么用，属性建模怎么用？作者没有简单回答这些问题，而是基于经验教训，给出各种方法的适用对象，还有最佳实践的小技巧。即使是成熟工程师，如果不了解FreeCAD，读这一部分也会有所收获。

第二部分是技巧，通过复制经典发明来展示建模技巧。阿基米德螺线，爱迪生的灯泡，蝙蝠侠的飞盘，贝尔的金属探测仪，特斯拉的轮机，它们是经典的发明，但发明本身不是本书重点。在复制其模型的时候，发现和了解多种建模技巧，才是演示这些例子的目的。比如，用哪些参数生成螺线，怎样通过表达式调用表格数据，怎样导入照片描摹形状，如何处理有对称性的模型，怎样把部件之间的位置尺寸关联起来，怎样用一个草图驱动整个模型的主要尺寸？操练这一部分的例子，你会遇到挫折，也会豁然开朗，这就是熟练掌握CAD的过程，到最后你就有信心完成自己的模型了。

第三部分是应用，展示有了三维模型之后，在应用层面可以有什么作为。用于加工的话，可以出工程图，标注详细尺寸作为加工图纸；还可以生成指令或模型，给数控机床和3D打印机直接加工；用于分析和展示的话，可以做工程运算，用有限元方法做应变、受热、流体和电磁分析；也可以给材质贴纹理，打光后生成渲染图。另外，通过FreeCAD内置的Python控制台，还有无限的可能。

附录部分谈了两个独立方面。一个方面是实体模型和线框模型各自的利弊，为3D打印导出文件时要用线框模型。另一个方面谈如何向FreeCAD导入三维和二维文件，讲解几种主要公开标准格式的利弊。

第一部分的概念是基础，第二部分的技巧是行路，第三部分的应用是落脚。一个发明者与一个工具箱的磨合，就要走过这样的旅程。

## [《FreeCAD For Inventors》的引言](https://forum.freecadweb.org/viewtopic.php?f=40&t=31900#p265451)

Mon Oct 29, 2018 4:43 pm 

> 本书作者@sliptonic和发行人@jdupuy保留所有权。经他们同意，我把引言部分发表在这里。如果你们有兴趣，可以通过“[关于FreeCAD这本书](https://forum.freecadweb.org/viewtopic.php?f=8&t=30959#p256564)”的链接，去[Kobo](https://www.kobo.com/us/en/ebook/freecad-for-inventors)或[Amazon](https://www.amazon.com/dp/B07H9RV5X6/ref=cm_sw_r_cp_ep_dp_GNzNBb50V8HNH)买书，也欢迎私信我，帮我做翻译的校对工作。

### 为什么你要读这本书

我小的时候，那是上个世纪七十年代，我读到很多发明家的故事，阿基米德、爱迪生、贝尔、特斯拉，还有蝙蝠侠。我很想成为他们那个样子，特别是蝙蝠侠，我知道我只差一件东西，那就是一个发明。对我来说，成为发明家不是你做了什么东西，而是你**是**什么人——当你发明了什么东西之后你成为了什么人。它当然不能是蠢笨的，它只能是些好东西，很棒的东西。【这个“它”是指人做的事，还是发明之物？】

从那时起，我体会到怎样才算真正的发明者。成就一个发明家的，不是他的商务名片，他的专利，甚至不是他那些成功的发明。成就发明家的，是他们思考的方式，是他们看问题的视角，是他们探索新工具、新技术的途径。他们的好奇心无处不在。他们总是能看到新的可能性，然后问道：“如果我们把这个和那个放在一起，会怎样？”

过了很长时间我才意识到，有些人天生就用这样的方式思考，而有些人要刻意地学习这些方法并在实践中练习。这些提问的方式方法，并不是个人独特的性格特质，而是发明家们在他们的实践中习得的关键工具。就像在任何领域一样，发明家们有很多这样的工具，他们也不断搜集（常常是发明）新的工具。

软件，特别是CAD/CAM软件，是发明家们的另一种工具。不过，我发现很多发明者和其他用户一样，使用CAD时很费力。理想情况下，用发明者自然的姿势使用工具就好，但是现实中，他们往往要让自己的方法屈从于软件。

过去几年里，我幸运地成为了FreeCAD社区的一员。我既是用户也是贡献者。我亲眼目睹了用户们努力地理解这款迷人软件的理念和妙处。这本书就是我的一个尝试，让更多的人可以用起来FreeCAD。

我们需要更多的发明者，而他们需要更好的工具。对发明者们，无论是那些名下已经有很多专利的，还是那些还在念高中的，我认为FreeCAD都是他们的无价之宝【这里换成一个好成语？宝莲灯，金箍棒？】。


### 它不是什么

这本书不是替代官方文档的。FreeCAD的维基很完备，几乎关于每一个工具和工作台，那里都有详细的信息和例子。你要真是FreeCAD用户，就该把它的维基页面【这里给出地址】放在浏览器收藏夹。FreeCAD的论坛很热闹，它形成了一个社区，里面真是好心人云集。你该常去那里翻翻找找，读一读大家的讨论。如果你没有参与论坛，那就错失了一半的乐趣。

【小i】 如果你在FreeCAD的论坛上提问，一定要包含你的FreeCAD信息，它在排查问题时，非常有必要。打开Help->About菜单，你就能看到一个按钮，它方便你复制这个信息到剪贴板，然后你把它放到你的帖子里。

这本书也不是一本教程。纵贯全书，会有几个通用的例子，但是每个部分都应该是独立的。出于这个考虑，本书的内容并不是围绕着一个案例，通过逐渐展开的方式，来讲解越来越复杂的技能。这本书采用几个历史上伟大的发明，作为启发性的例子，来展示FreeCAD的概念和能力。

最后，这也不是一本关于发明过程的书。它也许不能帮你成为一名更好的发明者，不过如果你从那些历史上的设计身上学到了什么，好吧，那可不是我的功劳。

### 它是什么

大多数FreeCAD的新用户进来时，心里都是带着任务的。它通常是一个点子，而他们希望它不只是一个点子。不管怎样，他们知道或者被告知，他们需要一个CAD工具。用Google一查，看到了FreeCAD，受到名字的启示，他们点链接进去。在主页上，他们看到了逼真的设计，在论坛上，他们看到了活动的讨论，在Youtube上，他们看到了丰富的演示。急于开始，他们下载了FreeCAD应用，运行安装，打开程序。然后，现实骨感：CAD真难啊。

FreeCAD是一个很大的应用集合。它提供的工具，支持的技术，远远多于一本书所能涵盖的范围。并且，做事情还不止有一种方法。对一个简单的问题，我们的回答往往是：“那个，得看情况。”

另一方面，FreeCAD的用户来自各行各业。他们有发明者、建筑师、学生、程序员、机械师，和艺术家。他们有的人使用设计软件经验丰富，有的只是刚刚起步。为工程任务优化的工具和概念，对一名艺术家来说，就很难接受了。不少工具都有那么多的可选项，即使是要完成一个简单的任务，也够烦人的。

这本书不是写给所有人的。这里呈现核心概念的方式，是让发明者觉得利益相关。并且只有那些跟发明过程有关的工具和技术，才在这里讲。结果就是FreeCAD的很多精彩的部分，根本就没有被探索到。然而，有了基本的武装，读者深入探寻这款超棒的应用，将会走得更容易一些。

虽然这本书不会把新手变成FreeCAD专家，但是它将引导新用户达到一个合格的水平，从此往上，就可以自我教育和深入探索了。

### 本书结构

全书的篇章组织成了三部分

第一部分：概念

这部分是给那些新手准备的，他们完全没有接触过FreeCAD，也不了解实体建模。首先，总览一下FreeCAD这款应用和它的用户界面。然后，介绍一些贯穿FreeCAD的核心概念。我们还会考察几个工作台，用相对原始的例子来解释他们的用途。如果你是FreeCAD新手，这个概念板块会帮你逐渐加速。如果你已经用过一阵FreeCAD了，你也可以找到一些以前不知道的细节、忠告和小技巧。或者如果你喜欢，整个跳过这部分，直接阅读技术的篇章吧。

第二部分：技术

这一部分包含几个例子，用来教发明者们一些核心技巧，向他们的工具箱里添加另一种工具。这些例子涉及几个工作台，融合了多种技术。后面的例子会用到之前讨论过的技术，但是跳过那些细节。

第二部分的例子假设你已经基本熟悉FreeCAD了，所以省略了某些细节。

第三部分：应用

创建实体模型不容易，但是真正产生价值的地方，是你用它做什么事情。在第三部分，我们看四个产生有用输出的工作台：路径、有限元、技术图和渲染。我们还会考察Python控制台和输出窗口，看看即便是非程序员，也能怎样有效地使用它。

### 图标约定

纵贯全书，你都能见到一些特别的框子，记有额外的信息，给你参考：

* 【铅笔】给出附加信息和旁白信息
* 【书签】记录不该忽略的重要细节
* 【喇叭】提示潜在问题或可能错误
* 【小i】给出有用的功能、小技巧、有益提示
* 【警告】警示可能造成的混乱

