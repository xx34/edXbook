****************
创建一个 HTML 组件
****************

    .. image:: Images/C07_01.png

HTML 组件是最基本的组件类型，可用於建造以文字为主的课程。
诸如文字、清单、联结、图片等资讯到单元中。 
例如，您可以在问题组件中使用这些组件来增加解释文字，您也可使用 HTML 组件来汇入 LaTeX 原始码到您的课程。

HTML 组件编辑器有两种显示模式: **视觉检视** 以及 **HTML 检视**
「视觉检视」提供“所见即所得” (WYSIWYG) 编辑器用以编辑已预先格式化版本的文字。
「HTML 检视」让您可以直接编辑 HTML 原始码。

.. note::

  当 HTML 原始码被储存时，Studio 将在渲染前先行处理结果。 
  在「视觉检视」及「HTML 检视」之间切换以确您创建的组件看起来与您预期的一样。

.. raw:: latex
  
      \newpage %

创建一个基本 HTML 组件
********************

**创建一个基本、空白的HTML组件**

1. 在新增新组件下，点击 **HTML** 接着点击 **空白** ，会出现下方的空白组件。

.. image:: Images/C07_02.png

2. 在空白组件中，点击 **编辑** 开启 HTML 编辑器。

.. image:: Images/C07_03.png

3. 输入您要的资讯，接着点击 **储存** 。

.. note::

  若您想要加入到其它页面或图片的连结或或是要直接编辑 HTML，请切换到 HTML 分页。

.. raw:: latex
  
      \newpage %

**创建一个包含样式的基本 HTML 组件**

1. 在 **新增组件** 下方点击 **HTML** 接着点击 **公告** ，出现下列画面。

.. image:: Images/C07_04.png

2. 点击 **编辑** 。

  在「视觉检视」里开启文字编辑器。 用您要发表的文字取代样式里的文字。

.. note::

  若您想要加入到其它页面或图片的连结或或是要直接编辑 HTML，请切换到 HTML 分页。

.. image:: Images/C07_05.png

3. 点击 **储存** 。

.. raw:: latex
  
    \newpage %

创建连结
*******

连结到讲义或图片
==========================

要连结到一个文件、图片或您上传到 **档案及上传页面** 的其他档案：

1. 创建一个空白的 HTML 组件，切换到 HTML 检视。

2. 在 HTML 对话框，创建连到您的档案的连结。

要创建连到文件的连结，请输入以下句法， **URL OF FILE** 是您上传档案到 **档案及上传** 页面的步骤5记下的 URL， **LINK TEXT** 是使用者所看到可以按下的文字连结要显示的文字。 ::

	<p><a href="[URL OF FILE]">[LINK TEXT]</a></p>

例如，要创建连结连到 “About” 页面的 HTML 样式的文件，其 URL 是
/c4x/edX/edX101/asset/AboutPage_Template.txt, 
则请输入以下的原始码： ::

  <p><a href="/c4x/edX/edX101/asset/AboutPage_Template.txt">HTML Template for
  <the "About" page</a></p>

要创建连到您已上传的图片的连结，请输入以下句法， **URL OF FILE** 是您上传档案到 **档案及上传** 页面的步骤5记下的 URL， **LINK TEXT** 是使用者所看到可以按下的文字连结要显示的文字。 ::

  <p><img src="[URL OF FILE]"/></p>

例如，当您要建立一个连结连到 CourseImage.jpg，您记下的 URL 为
/c4x/edX/edX101/asset/CourseImage.jpg
则请输入以下的原始码： ::

	<p><img src="/c4x/edX/edX101/asset/CourseImage.jpg"></p>

当您使用此原始码，将会出现下方图片中范例。

.. image:: Images/image078.png
  :width: 800

3. 点击 **储存** ，您的档案或图片将出现在组件中。


.. raw:: latex
  
  \newpage %
  

连结到课程单元
============

要引导学生到您课程中的特定位置，您必须要增加一个HTML连结到特定单元，请参考下列步骤：

1. 确定您课程的相对目录。

a. 在课程设定分页，点击在基本资讯下方的蓝色您的课程 URL 连结。

.. image:: Images/image079.png
  :width: 800

您课程的注册页会打开。

b. 从页面上方浏览器的网址列复制 URL

c. 复制在主要网址之後，“about”之前的 URL (包含最後面的 "/")，如下所举例： ::

	/courses/[organization]/[course_number]/[course_name]/

以 edX101: How to Create an edX Course from edX, 其完整的 URL 如下。 ::

	https://edge.edx.org/courses/edX/edX101/How_to_create_an_edX_course/about

其相对目录如下。 ::

	/courses/edX/edX101/How_to_create_an_edX_course/

2. 确定目标单元的位置 ID。 当您创建单元时，Studio 会为每个单元产生位置 ID。 
位置 ID 使用以下的句法。::

	 i4x://<organization>/<course_number>/vertical/<url_name_of_unit>

.. note::

  要找到位置 ID，在 Studio 中开启欲连结单元页面，接着注意浏览器中的网址列中的 URL。 
  位置 ID 为结束编辑後的URL，请见以下范例。

.. image:: Images/image081.png  


3. 打开您要连结的单元。

4. 在新增组件下方，点击 HTML，接着点击空白。画面上将出现一个新的空白组件。

.. image:: Images/image083.png
  :width: 800

5. 点击 **编辑** 。

6. 在开启的 HTML 编辑器中，点击 HTML 分页.

7. 接着到 number 1 输入下列原始码，用您於前述步骤中取得资讯取代课程相对目录位置，单元的位置 ID 以及连结文字。::

  <a href = "[[relative course directory]]/jump_to/[[location id of <unit]]">[link text]</a>

例如， 一个连结到 edx101 的 “Creating an HTML Component” 的单元类似於以下 ::

  <a href = "courses/edX/edX101/How_to_Create_an_edX_Course/jump_to/i4x://edX/ed
  <X101/vertical/8713e94afd074e40991dcb675d1030b5">Creating an HTML
  <Component</a>
 

.. raw:: latex
  
  \newpage %

从 LaTeX 汇入
************

您可以由汇入 LaTeX 原始码来创建一个 HTML 组件。

.. note::

  此功能还在开发当中。

1. 在 **新增单元** 下方，点击 **HTML** ，接着点击 **E-text Written in LaTeX.** 

.. image:: Images/C07_01.png
  :width: 800

2. 在出现的组件中点击编辑。

.. image:: Images/image083.png
  :width: 800

3. 组件编辑器会开启。在编辑器的左上角，点击黄色的 **Edit High Level Source** 文字。

.. image:: Images/image085.png
  :width: 800

4. 在开启的 **High Level Source Editing** 画面中，以您的 LaTeX 原始码取代范例程式码。

.. image:: Images/image087.png
  :width: 800

5. 点击 **Save and compile to edX XML** 以转换 LaTeX 原始码到 edX XML 程式码。

.. note::

  Studio 使用第三方 LaTeX 处理器来转换 LaTeX 程式码到 XML，LaTeX 处理器必须是在启动中的状态才能使用。

6. 点击 **储存** ，检查您新建的组件是否看起来跟您预想的一样。
