# Modelsim键盘快捷键和鼠标操作

使用Modelsim查看波形，大多数的操作是键盘和鼠标配合，通过熟悉快捷键操作可以帮助提操作效率。

内容来自Modelsim的官方指导手册，在GUI界面中可以这样查询：

`Help -> SE Documentation - InfoHub（HTML Brower Required）`，如下图所示：

![image-20210320103914229](https://gitee.com/sharewow/pic_repo/raw/master/img/image-20210320103914229.png)

也可以通过安装目录进行查询，这里路径以安装在`D:盘`为例：

```bash
D:\modeltech64_10.6e\docs\htmldocs
```

## 键盘快捷键和鼠标操作

可以使用各种键盘和鼠标操作来操作用户界面。

- 特定于窗口的键盘快捷键
- 用户定义的键盘快捷键
- 主窗口和源窗口的鼠标和键盘快捷键
- GUI Windows中的键盘快捷键列表
- 列表窗口键盘快捷键
- ==Wave窗口鼠标和键盘快捷键==

前面几个快捷键的操作，做了解即可，笔者当前没有对用户定义键盘快捷键进行配置。使用频率最高的依然是最后一个==Wave窗口鼠标和键盘快捷键==。如果前面的内容不看，不影响直接跳转到那一节。

以下内容使用google翻译，加上人工校对，如有问题以原版英文准。

## 特定于窗口的键盘快捷键

可以通过在键盘上输入`Ctrl + /`来打开许多ModelSim窗口的常用（预定义）和用户定义的键盘排序窗口的动态列表。

例如，图1显示了为“源”窗口提供的键盘快捷键列表。

图1.源窗口的键盘快捷键

![img](https://gitee.com/sharewow/pic_repo/raw/master/img/source_shortcuts.gif)

通过单击列表底部的`查看所有快捷方式(View All Shortcuts)`，可以找到所有键盘快捷方式的完整列表（包括预定义的和用户定义的）。有关如何创建自定义快捷键的更多信息，请参考用户定义的键盘快捷键。

## 用户自定义的键盘快捷键

除了预定义的键盘快捷键之外，您还可以使用`键盘快捷键`对话框创建自己的快捷键或修改预定义的键盘快捷键。

快捷方式可以是特定于窗口的（仅当窗口处于活动状态时可用），也可以是全局的（可从工具中的任何位置使用）。您可以为任何ModelSim窗口创建键盘快捷键。

一旦定义了快捷方式，它将在所有后续调用中可用。该架构的动态特性使键盘快捷键可用于任何基于ModelSim GUI的Mentor Graphics产品。

###　键盘快捷方式对话框

键盘快捷方式对话框列出了所有现有的键盘快捷方式。此对话框区分用户定义的快捷方式和ModelSim模拟器预定义的快捷方式。
图2显示了`键盘快捷键`对话框的示例，您可以通过从主菜单中选择以下内容来显示该对话框：

`Windows>键盘快捷方式...`

图2.键盘快捷方式对话框

![img](https://gitee.com/sharewow/pic_repo/raw/master/img/kbd_shortcut_all-1616208510209.gif)


键盘快捷方式对话框使您可以：

- 添加一个新的用户定义的键盘快捷方式。有关更多信息，请参考创建键盘快捷键。
- 修改现有的键盘快捷键。可以修改任何快捷方式，包括预定义的快捷方式。
- 删除快捷方式。
- 从以前保存的`bindings.do`文件导入快捷方式。您也可以使用`do`命令重新加载键盘快捷方式文件。
- 将所有用户定义的键盘快捷方式导出到`bindings.do`文件。通过选择“键盘快捷方式”对话框中的“导入”按钮或在命令行上输入`do bindings.do`，可以重新加载文件中保存的键盘快捷键。

### 创建键盘快捷键

可以创建自己的全局快捷方式或仅适用于特定窗口的快捷方式。

#### 程序

1. 如果要创建特定于窗口的快捷方式，则必须在模拟运行期间的某个时间打开该窗口。

2. 通过选择“**窗口”>“键盘快捷键**”，打开“**添加键盘快捷键”**对话框。

3. 单击**添加**按钮以打开添加键盘快捷方式对话框。

   *图3.添加键盘快捷方式对话框*

   ![img](https://gitee.com/sharewow/pic_repo/raw/master/img/kbd_shortcut_add.gif)

   

4. 选择快捷方式类型，全局或窗口。如果要创建特定于窗口的快捷方式，请单击窗口按钮以打开“**选择窗口类型”**对话框。该对话框显示当前模拟过程中打开的每个窗口。如果没有找到所需的窗口，请关闭两个对话框，通过在命令行上输入**视图**<window>或从**View**菜单中选择该窗口来打开所需的窗口。选择“全局”或特定窗口会在“**快捷键操作”**字段和右侧的动态填充字段中更改可用的选项。

5. 在**快捷键**字段中输入组合**键**。或选择“**更改输入模式”**按钮以输入组合键。

6. 选择快捷方式将执行的操作类型。

   - 弹出菜单或下拉菜单—打开“**菜单项”**对话框，其中包含全局或步骤4中指定的窗口可用的所有弹出菜单和下拉菜单项的层次结构列表。
   - 工具栏按钮-打开“工具栏按钮”对话框，其中列出了全局或步骤4中指定的窗口可用的所有工具栏按钮操作的层次结构列表。
   - 常规Tcl脚本—选择此选项将在右侧打开Tcl脚本字段。您可以输入任何Tcl脚本或命令行序列。
   - 内部窗口命令-此选项仅适用于特定于窗口的命令。请参考步骤4。打开右侧的“窗口动作”对话框，其中包含所有窗口特定命令的列表。

## 主窗口和源窗口的鼠标和键盘快捷键

以下鼠标操作和特殊的按键可用于`main`窗口的输入区域中编辑命令。

它们也可以用于编辑在`源`窗口和所有“**记事本”**窗口中显示的文件（在ModelSim中输入notepad命令以打开“记事本”编辑器）。

表1. 鼠标快捷方式

| Mouse-UNIX和Windows                      | 结果                                     |
| ---------------------------------------- | ---------------------------------------- |
| 点击鼠标左键                             | 重新定位光标                             |
| 单击并拖动鼠标左键                       | 选择一个地区                             |
| 按住Shift键并单击鼠标左键                | 扩展选择                                 |
| 双击鼠标左键                             | 选择一个词                               |
| 双击并拖动鼠标左键                       | 选择一组词                               |
| 按住Ctrl键并单击鼠标左键                 | 移动插入光标而不更改选择                 |
| 在先前的ModelSim或VSIM提示上单击鼠标左键 | 将先前的命令字符串复制并粘贴到当前提示中 |
| 点击鼠标中键                             | 将选择粘贴到剪贴板                       |
| 单击并拖动鼠标中键                       | 滚动窗口                                 |

表2.键盘快捷键

| KEY-UNIX和Windows                                      | 结果                                                         |
| ------------------------------------------------------ | ------------------------------------------------------------ |
| 左箭头、右箭头                                         | 向左或向右移动光标一个字符                                   |
| Ctrl +向左键、Ctrl +右箭头                             | 向左或向右移动光标一个词                                     |
| Shift +任何箭头                                        | 扩展文本选择                                                 |
| Ctrl + Shift +左箭头、Ctrl + Shift +右箭头             | 用一个词扩展文本选择                                         |
| 向上箭头、向下箭头                                     | 笔录窗口：滚动浏览命令历史记录源窗口：将光标上移或下移一行   |
| Ctrl +向上箭头、Ctrl +向下箭头                         | 笔录窗口：将光标移至第一行或最后一行源代码窗口：将光标上移或下移一个段落 |
| Alt + /                                                | 打开用于输入命令的弹出命令提示符。                           |
| Ctrl +主页                                             | 将光标移到文本的开头                                         |
| Ctrl +结束                                             | 将光标移到文本的末尾                                         |
| 退格键Ctrl + h（仅UNIX）                               | 删除左侧的字符                                               |
| 删除Ctrl + d（仅UNIX）                                 | 删除右边的字符                                               |
| Esc（仅Windows）                                       | 取消                                                         |
| Alt键                                                  | 激活或停用菜单栏模式                                         |
| Alt-F4                                                 | 关闭活动窗口                                                 |
| Home、Ctrl + a                                         | 将光标移到行首                                               |
| Ctrl + Shift + a                                       | 选择活动窗口的所有内容                                       |
| Ctrl + b                                               | 向左移动光标                                                 |
| Ctrl + d                                               | 删除右边的字符                                               |
| End、Ctrl + e                                          | 将光标移到行尾                                               |
| Ctrl + f（UNIX）、向右箭头（Windows）                  | 将光标向右移动一个字符                                       |
| Ctrl + k                                               | 删除到行尾                                                   |
| Ctrl + n                                               | 将光标向下移动一行（仅在Windows下为“源”窗口）                |
| Ctrl + o（仅UNIX）                                     | 在光标处插入换行符                                           |
| Ctrl + p                                               | 将光标向上移动一行（仅在Windows下为“源”窗口）                |
| Ctrl + s（UNIX）、Ctrl + f键（Windows）                | 找                                                           |
| Ctrl + T                                               | 颠倒光标两侧的两个字符的顺序                                 |
| Ctrl + u                                               | 删除行                                                       |
| 向下翻页、Ctrl + v（仅UNIX）                           | 将光标向下移动一屏                                           |
| Ctrl + x                                               | 削减选择                                                     |
| Ctrl + s、Ctrl + x（仅UNIX）                           | 救                                                           |
| Ctrl + v                                               | 粘贴选择                                                     |
| Ctrl + a（仅Windows）                                  | 选择小部件的全部内容                                         |
| Ctrl + \                                               | 清除小部件中的所有选择                                       |
| Ctrl +-（UNIX）、Ctrl + /（UNIX）、Ctrl + z（Windows） | 撤消“源代码”窗口中的先前编辑                                 |
| 元+ <（仅UNIX）                                        | 将光标移到文件的开头                                         |
| 元+>（仅UNIX）                                         | 将光标移到文件末尾                                           |
| 向上翻页、Meta + v（仅UNIX）                           | 将光标向上移动一屏                                           |
| Ctrl + c                                               | 复制选择                                                     |
| F3                                                     | 在“源”窗口中执行“查找下一个”操作。                           |
| F4、Shift + F4                                         | 将焦点切换到主窗口中的下一个窗格将焦点切换到主窗口中的上一个窗格 |
| F5、Shift + F5                                         | 在扩展和还原窗格的大小之间切换以适合整个主窗口切换开/关窗格标题。 |
| F8                                                     | 搜索与键入的字符匹配的最新命令（仅主窗口）                   |
| F9                                                     | 运行模拟                                                     |
| F10                                                    | 继续模拟                                                     |
| F11（仅Windows）                                       | 一小步                                                       |
| F12（仅Windows）                                       | 跨步                                                         |

主窗口仅允许在提示后插入或粘贴；因此，将字符串复制到命令行时无需设置光标。

 ## GUI Windows中的键盘快捷列表

您可以通过输入Ctrl-Shift-？来打开大多数窗口的键盘快捷键的动态列表（预先定义和用户定义）。

*图1.原理图窗口键盘快捷键*

![img](https://gitee.com/sharewow/pic_repo/raw/master/img/schematic_keyboard_shortcuts.gif)

您可以创建用户定义的键盘快捷方式并更改预定的快捷方式。有关更多信息，请参考[用户定义的键盘快捷键](Contain_UserDefinedKeyboardShortcuts_id45c046f4.html#id45c046f4-273a-429d-93f4-bd90950996f9__Contain_UserDefinedKeyboardShortcuts_id45c046f4.xml#id45c046f4-273a-429d-93f4-bd90950996f9)。

 ## 列表窗口键盘快捷键

当鼠标光标位于“列表”窗口中时，使用以下键将导致指示的操作：

表3.列表窗口键盘快捷键

| KEY-UNIX和Windows                       | 行动                                                 |
| --------------------------------------- | ---------------------------------------------------- |
| 左箭头                                  | 向左滚动列表（选择并突出显示当前所选项目左侧的项目） |
| 右箭头                                  | 向右滚动列表（选择并突出显示当前所选项目右侧的项目） |
| 向上箭头                                | 向上滚动列表                                         |
| 向下箭头                                | 向下滚动列表                                         |
| 向上翻页、Ctrl +向上箭头                | 逐页向上滚动列表                                     |
| 向下翻页、Ctrl +向下箭头                | 按页面向下滚动列表                                   |
| 标签                                    | 向前（向下）搜索所选信号的下一个过渡                 |
| Shift + Tab                             | 向后（向上）搜索所选信号的上一个过渡                 |
| Shift +向左键、Shift +右箭头            | 向左/向右扩展选择                                    |
| Ctrl + f键（Windows）、Ctrl + s（UNIX） | 打开“查找”对话框以在列表显示中查找指定的项目标签     |

## Wave窗口鼠标和键盘快捷键

在Wave窗口中可以使用以下鼠标操作和击键。

表4. Wave窗口鼠标快捷键

| 鼠标动作1                                                    | 结果                                                       |
| ------------------------------------------------------------ | ---------------------------------------------------------- |
| Ctrl +单击鼠标左键并拖动![img](https://gitee.com/sharewow/pic_repo/raw/master/img/a_shortcuts1a.png) | 放大区域（zoom in）                                        |
| Ctrl +单击鼠标左键并拖动![img](https://gitee.com/sharewow/pic_repo/raw/master/img/a_shortcuts2a.png) | 缩小（zoom out）                                           |
| Ctrl +单击鼠标左键并拖动![img](https://gitee.com/sharewow/pic_repo/raw/master/img/a_shortcuts3a.png) | 缩放适合                                                   |
| 单击鼠标左键并拖动                                           | 移动最近的光标                                             |
| Ctrl +在滚动条箭头上单击鼠标左键                             | 将窗口滚动到顶部或底部（垂直滚动）或向左或向右（水平滚动） |
| 单击滚动条中的鼠标中键（仅适用于UNIX）                       | 将窗口滚动到点击位置                                       |
| Shift +鼠标中键滚动                                          | 滚动窗口                                                   |

**Note：** 如果选择“**波形”>“鼠标模式”>“缩放模式”**，则无需按`Ctrl`键。

| 按键                                  | 行动                                                         |
| ------------------------------------- | ------------------------------------------------------------ |
| s                                     | 使当前活动的光标可见并居中                                   |
| i、Shift +i、+                        | 放大（鼠标指针必须在光标或波形窗格上方）                     |
| o、Shift + o、-                       | 缩小（鼠标指针必须在光标或波形窗格上方）                     |
| f、Shift + f                          | 全屏放大（鼠标指针必须在光标或波形窗格上方）                 |
| L、Shift + L                          | 最后放大（鼠标指针必须在光标或波形窗格上方）                 |
| r、Shift + r                          | 变焦范围（鼠标指针必须在光标或波形窗格上方）                 |
| m                                     | 将所有打开的Wave窗口缩放到活动窗口的缩放范围。               |
| 向上箭头、向下箭头                    | 当鼠标指针移至“波形”窗格上方时，将整个窗口向上或向下滚动一行当鼠标指针位于路径名或值窗格上方时，向上或向下滚动突出显示一行 |
| 左箭头                                | 向左滚动路径名，值或波形窗格                                 |
| 右箭头                                | 向右滚动路径名，值或波形窗格                                 |
| 向上翻页                              | 将波形窗格向上滚动一页                                       |
| 向下翻页                              | 将波形窗格向下滚动一页                                       |
| 标签                                  | 向前搜索（向右）到所选信号的下一个过渡-找到下一个边沿        |
| Shift + Tab                           | 向后（向左）搜索选定信号上的上一个过渡-查找上一个边          |
| Ctrl + G                              | 自动为名称为Group <n>的区域的选定信号创建一个组。如果对已存在“ Group <n>”的信号使用此快捷方式，则将它们放置在该区域的组中，而不是创建一个新的组。 |
| Ctrl + F（Windows）、Ctrl + S（UNIX） | 打开查找对话框；在路径名窗格中的指定字段中搜索文本字符串     |
| Ctrl +向左键、Ctrl +右箭头            | 左右滚动页面的路径名，值或波                                 |

## 写在后面

当然不需要一次性用脑子记下来这么多操作，用到的时候想到咋用的，多用几次自然就习惯了。

2021-03-20.

