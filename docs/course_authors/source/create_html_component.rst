****************
创建一个 HTML 组件
****************

    .. image:: Images/C07_01.png

HTML 组件是最基本的组件类型，可用于创建以文字为主的课程。
例如文字、清单、链接、图片等内容到单元中。 
例如，您可以在问题组件中使用这些组件来增加解释文字，您也可使用 HTML 组件来插入 LaTeX 源代码到您的课程。

HTML 编辑器有两种显示模式: **可视化** 以及 **代码**
选择“可视化”时，您只需输入内容，编辑器将生成相应的 HTML 代码。
选择“代码”时，您可以直接编辑 HTML 代码。
若要更改显示模式，请点击 HTML 编辑器右上角的 **设置** ，改变 **编辑器** 选项为您想要的模式。

.. note::

  当 HTML 源代码被保存时，Studio 将在渲染前先行处理结果。
  如果您改变了显示模式设置，则该设置将在您保存并重新打开 HTML 编辑器才生效。
  在“可视化”模式下的 HTML 编辑器的工具栏最右侧有 **HTML** 按钮，点击该按钮可以弹出 **HTML 源代码** 编辑界面，通过这种方式您可以便捷的在“可视化”及“代码”之间切换以确您创建的组件看起来与您预期的一样。

.. raw:: latex
  
      \newpage %

创建一个基本 HTML 组件
********************

**创建一个基本的文字HTML组件**

1. 在 **添加新组件** 下，点击 **HTML** 接着点击 **文字** ，会出现下方的文字组件。

.. image:: Images/C07_02.png

2. 在文字组件中，点击 **编辑** 开启 HTML 编辑器。

.. image:: Images/C07_03.png

3. 输入您想要的文本，接着点击 **保存** 。

.. note::

  若您想要加入其它页面或图片的链接或是要直接编辑 HTML，请点击工具栏最右侧的 **HTML** 。

.. raw:: latex
  
      \newpage %

**创建一个包含样式的基本 HTML 组件**

1. 在 **添加新组件** 下方点击 **HTML** 接着点击 **Announcement** ，出现下列画面。

.. image:: Images/C07_04.png

2. 点击 **编辑** 。

  在弹出的 HTML 编辑器中，用您要发表的内容取代模板里的文字。

.. note::

  若您想要加入其它页面或图片的链接或是要直接编辑 HTML，请点击工具栏最右侧的 **HTML** 。

.. image:: Images/C07_05.png

3. 点击 **保存** 。

.. raw:: latex
  
    \newpage %

创建链接
*******

链接到讲义或图片
==========================

要链接到一个文件、图片或您上传到 **文件&上传** 页面的其他文件：

1. 创建一个模板为“Raw HTML”的 HTML 组件，点击编辑。

2. 在“代码”模式的 HTML 编辑器里，创建连到您的文件的链接。

要创建连到文件的链接，请按照以下句法输入， **URL OF FILE** 是您上传文件到 **文件&上传** 页面的第5个步骤中记下的 URL， **LINK TEXT** 是使用者所看到的可以点击的文字链接要显示的文字。 ::

	<p><a href="[URL OF FILE]">[LINK TEXT]</a></p>

例如，要创建链接连到 “About” 页面的 HTML 样式的文件，其 URL 是
/c4x/edX/edX101/asset/AboutPage_Template.txt, 
则请输入以下的源代码： ::

  <p><a href="/c4x/edX/edX101/asset/AboutPage_Template.txt">HTML Template for
  <the "About" page</a></p>

要创建连到您已上传的图片的链接，请按照以下句法输入， **URL OF FILE** 是您上传文件到 **文件&上传** 页面的第5个步骤中记下的 URL， **LINK TEXT** 是使用者所看到可以按下的文字链接要显示的文字。 ::

  <p><img src="[URL OF FILE]"/></p>

例如，当您要建立一个链接连到 CourseImage.jpg，您记下的 URL 为
/c4x/edX/edX101/asset/CourseImage.jpg
则请输入以下的源代码： ::

	<p><img src="/c4x/edX/edX101/asset/CourseImage.jpg"></p>

当您使用此源代码，将会出现下方图片中范例。

.. image:: Images/image078.png
  :width: 800

3. 点击 **保存** ，您的文件或图片将出现在组件中。


.. raw:: latex
  
  \newpage %
  

链接到课程单元
============

要引导学生到您课程中的特定位置，您必须要增加一个HTML链接到特定单元，请参考下列步骤：

1. 确定您课程的相对目录。

a. 在课程设定页面，点击基本资讯下方的您的课程的 URL 链接。

.. image:: Images/image079.png
  :width: 800

您课程的注册页会被打开。

b. 从页面上方浏览器的地址栏复制 URL

c. 复制域名之后“about”之前的 URL (包含最后面的 "/")，如下所示： ::

	/courses/[organization]/[course_number]/[course_name]/

以 edX101: How to Create an edX Course from edX 为例, 其完整的 URL 如下。 ::

	https://edge.edx.org/courses/edX/edX101/How_to_create_an_edX_course/about

其相对目录如下。 ::

	/courses/edX/edX101/How_to_create_an_edX_course/

2. 确定目标单元的位置 ID。当您创建单元时，Studio 会为每个单元生成位置 ID。 
位置 ID 使用以下的句法。::

	 i4x://<organization>/<course_number>/vertical/<url_name_of_unit>

.. note::

  要找到位置 ID，在 Studio 中打开要链接到的单元页面，在页面右侧 **单元位置** 区域有该单元的位置 ID 。
  或者通过URL分离位置 ID ，注意浏览器地址栏中的 URL 。 
  位置 ID 为结束编辑后的URL，请见以下范例。

.. image:: Images/image081.png  


3. 打开您要添加链接的单元。

4. 在 **添加新组件** 下方，点击 HTML ，接着点击 **Raw HTML** ，将出现一个新的组件。

.. image:: Images/image083.png
  :width: 800

5. 点击 **编辑** 。

7. 在弹出的 HTML 编辑器中，用您在之前几步中获取的课程相对目录位置，单元的位置 ID 以及链接文字，按照以下句法输入源代码。::

  <a href = "[[relative course directory]]/jump_to/[[location id of <unit]]">[link text]</a>

例如，一个链接到 edx101 的 “Creating an HTML Component” 单元的源代码应该是 ::

  <a href = "courses/edX/edX101/How_to_Create_an_edX_Course/jump_to/i4x://edX/ed
  <X101/vertical/8713e94afd074e40991dcb675d1030b5">Creating an HTML
  <Component</a>
 

.. raw:: latex
  
  \newpage %

从 LaTeX 插入
************

您可以通过插入 LaTeX 源代码来创建一个 HTML 组件。

.. note::

  此功能还在开发当中。

1. 在 **添加新组件** 下方，点击 **HTML** ，接着点击 **E-text Written in LaTeX.** 

.. image:: Images/C07_01.png
  :width: 800

2. 在出现的组件中点击 **编辑** 。

.. image:: Images/image083.png
  :width: 800

3. 在弹出的组件编辑器的左上角，点击黄色的 **Edit High Level Source** 文字。

.. image:: Images/image085.png
  :width: 800

4. 在开启的 **High Level Source Editing** 画面中，以您的 LaTeX 源代码取代模板代码。

.. image:: Images/image087.png
  :width: 800

5. 点击 **Save and compile to edX XML** 以转换 LaTeX 源代码到 edX XML 代码。

.. note::

  Studio 使用第三方 LaTeX 处理器来转换 LaTeX 代码到 XML，LaTeX 处理器必须是在启动中的状态才能使用。

6. 点击 **保存** ，检查您新建的组件是否看起来跟您预想的一样。
