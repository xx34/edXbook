.. raw:: latex
  
      \newpage %


================
附录 E: 问题类别
================

选项响应
========

选项响应允许学生从一群选项组合中，从下拉式选单中选出正确的答案。

选项响应类似选择题，有些概念上不同之处如下所列：

* 选择题使用的单选按钮比较适合学生在较长的叙述中选出答案。

* 选项响应使用的下拉式选单的格式，适合学生先思考一个可能的答案再从选单中寻找，而非纯粹认出这个答案。

* 选择题的格式较为明确清晰，所以更为适合用在较为复杂的问题以及答案的组合应用上，让学生能够适度地暂停思考可能的答案。

范例问题如下：

.. image:: ../Images/image287.png
    :width: 600  

**问题代码**

.. code-block:: xml

  <problem>

   <p>Option Response is most similar to __________.</p>

    <optionresponse>
     <optioninput
       options="('Multiple Choice','String Response',
                'Numerical Response','External Response',
                'Image Response')"
      correct="Multiple Choice"/>1
    </optionresponse>

   <solution>
     <div class="detailed-solution">
       <p>Explanation</p>
        <p>Like Option Response, Multiple Choice also allows students to select
       from a variety of pre-written responses.</p>
     </div>
    </solution>
  </problem>



**样板**

.. code-block:: xml

  <problem>

    <optionresponse>
     options="('A','B')"
      correct="A"/>
    </optionresponse>

    <solution>
      <div class="detailed-solution">
      </div>
    </solution>
  </problem> 



**XML 属性资讯**

<optionresponse>


  .. image:: ../Images/option_response1.png


<optioninput>

  .. image:: ../Images/optionresponse2.png


.. raw:: latex
  
      \newpage %


选择题 
======

选择题允许学生从一群选项组合中，以单选按钮清单的形式选出正确的答案。

一个选择题可以拥有超过一个以上的答案，端看您在 XML 中怎样描述并标记哪些选项是正确的。如果所有的选项都是错的，那麽这是一个错误格式的选择题。

选择题类似於选项响应，有些概念上不同之处如下所列：

* 选择题的单选按钮让学生容易从长叙述的选项中选出答案。

* 选项响应使用的下拉式选单的格式，适合学生先思考一个可能的答案再从选单中寻找，而非纯粹认出这个答案。

* 选择题的格式较为明确清晰，所以更为适合用在较为复杂的问题以及答案的组合应用上，让学生能够适度地暂停思考可能的答案。

范例问题如下：

.. image:: ../Images/image289.png
 :width: 600  

**问题代码** 

.. code-block:: xml

  <problem>
  <p><b>Example Problem</b></p>
  <p>How many correct responses can a Multiple Choice question have?</p>
      <multiplechoiceresponse>
     <choicegroup type="MultipleChoice">
        <choice correct="false" name="one">Only one</choice>
        <choice correct="false" name="zeroone">Only zero or one</choice>
        <choice correct="true" name="zeromore">Zero or more</choice>
        <choice correct="false" name="onemore">Only one or more</choice>
        <choice correct="false" name="noone">Nobody knows</choice>
        <choice correct="true" name="someone">Somebody might know :)</choice>
    </choicegroup>
    </multiplechoiceresponse>
  <solution>
        <div class="detailed-solution">
          <p>Explanation</p>
            <p>It depends on how many choices are marked as correct in the underlying XML.</p>                  
  <p>Note that if all choices are marked as incorrect, there is no
          correct response.</p>
        </div>
    </solution>
  </problem>


**样板** 

.. code-block:: xml

  <problem>

  <multiplechoiceresponse>
    <choicegroup type="MultipleChoice">
      <choice correct="false" name="a">A</choice>
      <choice correct="true" name="b">B</choice>
    </choicegroup>
  </multiplechoiceresponse>

  <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>


**XML 属性资讯**


<multiplechoiceresponse>

.. image:: ../Images/multipleresponse.png


<choicegroup>

  .. image:: ../Images/multipleresponse2.png


<choice>

  .. image:: ../Images/multipleresponse3.png


.. raw:: latex
  
      \newpage %


核取方块
========

核取方块允许学生从一群选项组合中，以核取方块清单的形式选出零或多个的答案。

备注：一个问题本身若使用核取方块来描述正确答案的组合，作答时所有被标记为 "true" 的选项都必须选择出来才会被判定为正确。

比较特别的是，“所有选项都被选起" 可以是一种正确的答案。但与选择题不同的地方在於，一定至少要有一个选项被选起，没有选项被选起是种错误的格式。

范例问题如下：

.. image:: ../Images/image290.png
 :width: 600  


**问题代码**

.. code-block:: xml

  <problem>
  <startouttext/>
    <p>How many correct responses can a Checkbox question have?</p>

  <choiceresponse>
  <checkboxgroup>
  <choice correct="false"><text>Zero</text></choice>
  <choice correct="true"><text>One</text></choice>
  <choice correct="false"><text>Two or more</text></choice>
  <choice correct="false"><text>Nobody knows</text></choice>
  <choice correct="true"><text>Somebody might know :)</text></choice>
  </checkboxgroup>
  </choiceresponse>
  </problem>


**样板**

.. code-block:: xml

  <problem>

  <choiceresponse>
  <checkboxgroup>
  <choice correct="false"><text>Zero</text></choice>
  <choice correct="true"><text>One</text></choice>
  </checkboxgroup>
  </choiceresponse>
  </problem>

.. raw:: latex
  
     \newpage %


字串响应
========

字串响应提供了一个输入方块，学生可以输入一行文字作为答案。

字串响应并不提供任何作答辅助，所以这也间接鼓励学生将其想法以各种形式，完成描述出来。

需要注意的是，由於学生的答案必须一字不差地符合答案的设定才能被判定为正确，因此这可能会在一些较为多元的答案格式 (例如日期) 上造成一些困扰。

范例问题如下：

.. image:: ../Images/image291.png
 :width: 600   

**问题代码**

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
    <p>What is the name of this unit? (What response type is this?)</p>
    <stringresponse answer="String Response" type="ci">
      <textline size="20"/>
    </stringresponse>
    <solution>
      <div class="detailed-solution">
        <p>Explanation</p>
        <p>The name of this unit is "String Response," written without the punctuation.</p>
        <p>Arbitrary capitalization is accepted.</p>
      </div>
    </solution>
  </problem>

**样板**

.. code-block:: xml

  <problem>
    <stringresponse answer="REPLACE_THIS" type="ci">
      <textline size="20"/>
    </stringresponse>
    <solution>
      <div class="detailed-solution">
      </div>
    </solution>
  </problem>

**XML 属性资讯**

<stringresponse>

  .. image:: ../Images/stringresponse.png

<textline>

  .. image:: ../Images/stringresponse2.png


.. raw:: latex
  
      \newpage %


数值响应
========

数值响应提供了一个输入方块，学生可以输入一个数字作为答案，不过数值的表示方式则必须遵守一定的规范。

答案本身只要落在容忍的范围内，就会被判定为正确。

预期的答案可以是个明确的数值，或是一段 Python 脚本计算的结果。

允许的输入答案形式包含了 ``<formulaequationinput />`` and ``<textline />`` 两种。
不过用 ``<textline math="1" />`` 格式描述的数学问题，可能会因为使用不同的分析器处理而有不同的结果，这会造成学生作答时的困难。
因此我们强烈建议只使用 ``<formulaequationinput />`` 这种格式，请见下面的范例问题。

范例问题如下：

.. image:: ../Images/image292.png
 :width: 600   


**问题代码**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>

  <p>What base is the decimal numeral system in?
      <numericalresponse answer="10">
          <formulaequationinput />
      </numericalresponse>
  </p>

    <p>What is the value of the standard gravity constant <i>g</i>, measured in m/s<sup>2</sup>? Give your answer to at least two decimal places.
    <numericalresponse answer="9.80665">
      <responseparam type="tolerance" default="0.01" />
      <formulaequationinput />
    </numericalresponse>
  </p>

  <!-- Use python script spacing. The following should not be indented! -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>
    
  <p>What is the distance in the plane between the points (pi, 0) and (0, e)? You can type math.
      <numericalresponse answer="$computed_response">
          <responseparam type="tolerance" default="0.0001" />
          <formulaequationinput />
      </numericalresponse>
  </p>
  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>The decimal numerical system is base ten.</p>
      <p>The standard gravity constant is defined to be precisely 9.80665 m/s<sup>2</sup>.
      This is 9.80 to two decimal places. Entering 9.8 also works.</p>
      <p>By the distance formula, the distance between two points in the plane is
         the square root of the sum of the squares of the differences of each coordinate.
        Even though an exact numerical value is checked in this case, the
        easiest way to enter this answer is to type
        <code>sqrt(pi^2+e^2)</code> into the editor. 
        Other answers like <code>sqrt((pi-0)^2+(0-e)^2)</code> also work.
      </p>
    </div>
  </solution>
  </problem>

**样板**

精确值

.. code-block:: xml

  <problem>

    <numericalresponse answer="10">
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>

十进制小数答案

.. code-block:: xml

  <problem>

    <numericalresponse answer="9.80665">
      <responseparam type="tolerance" default="0.01" />
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>

百分比答案

.. code-block:: xml

  <problem>

    <numericalresponse answer="100">
      <responseparam type="tolerance" default="10%" />
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>

利用脚本计算的答案

.. code-block:: xml

  <problem>

  <!-- Use python script spacing. The following should not be indented! -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>

    <numericalresponse answer="$computed_response">
      <responseparam type="tolerance" default="0.0001" />
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>


**XML 属性资讯**

<script>

  .. image:: ../Images/numericalresponse.png


``<numericalresponse>``

+------------+----------------------------------------------+-------------------------------+
| Attribute  |                 Description                  |              Notes            |
+============+==============================================+===============================+
| ``answer`` | A value to which student input must be       | Note that any numeric         |
|            | equivalent. Note that this expression can be | expression provided by the    |
|            | expressed in terms of a variable that is     | student will be automatically |
|            | computed in a script provided in the problem | simplified on the grader's    |
|            | by preceding the appropriate variable name   | backend.                      |
|            | with a dollar sign.                          |                               |
|            |                                              |                               |
|            | This answer will be evaluated similar to a   |                               |
|            | student's input. Thus '1/3' and 'sin(pi/5)'  |                               |
|            | are valid, as well as simpler expressions,   |                               |
|            | such as '0.3' and '42'                       |                               |
+------------+----------------------------------------------+-------------------------------+


+------------------------+--------------------------------------------+--------------------------------------+
|       Children         |                 Description                |                 Notes                |
+========================+============================================+======================================+
| ``responseparam``      | used to specify a tolerance on the accepted|                                      |
|                        | values of a number. See description below. |                                      |
+------------------------+--------------------------------------------+--------------------------------------+
|``formulaequationinput``| An input specifically for taking math      |                                      |
|                        | input from students. See below.            |                                      |
+------------------------+--------------------------------------------+--------------------------------------+
| ``textline``           | A format to take input from students, see  | Deprecated for NumericalResponse.    |
|                        | description below.                         | Use ``formulaequationinput`` instead.|
+------------------------+--------------------------------------------+--------------------------------------+


<responseparam>

  .. image:: ../Images/numericalresponse4.png

<formulaequationinput/>

========= ============================================= =====
Attribute                  Description                  Notes
========= ============================================= =====
size      (optional) defines the size (i.e. the width)
          of the input box displayed to students for
          typing their math expression.
========= ============================================= =====

<textline> (While <textline /> is supported, its use is extremely discouraged.
We urge usage of <formulaequationinput />. See the opening paragraphs of the
`Numerical Response`_ section for more information.)

  .. image:: ../Images/numericalresponse5.png


数学表达式语法
--------------

於数值响应当中，学生输入的内容可能比普通的数字还复杂。像是 ``sqrt(3)`` 甚至 ``1+e^(sin(pi/2)+2*i)`` 都是合法而且可以计算出答案的输入。

语法概要如下：

数字
~~~~

可接受的数字型态：

- 整数: '2520'
- 浮点数: '3.14'
- 小数: '.98'
- 科学记号: '1.2e-2' (=0.012)
- 更多的科学记号: '-4.4e+5' = '-4.4e5' (=-440,000)
- 附加 SI 後缀: '2.25k' (=2,250). The full list:

  ====== ========== ===============
  Suffix Stands for One of these is
  ====== ========== ===============
  %      percent    0.01 = 1e-2
  k      kilo       1000 = 1e3
  M      mega       1e6
  G      giga       1e9
  T      tera       1e12
  c      centi      0.01 = 1e-2
  m      milli      0.001 = 1e-3
  u      micro      1e-6
  n      nano       1e-9
  p      pico       1e-12
  ====== ========== ===============

目前支援的最大数字为正浮点数的上限值 (以 Python 语言能支援的定义)，也就是 1.7977e+308。
任何表示式中含有更大的数值是不支援的，因此最好避免这样的情况。


预设的常数
~~~~~~~~~~

简单而且常用的的数学及科学常数已经有定义，包含了：

- ``i`` and ``j`` as ``sqrt(-1)``
- ``e`` as Euler's number (2.718...)
- ``pi``
- ``k``: the Boltzmann constant (~1.38e-23 in Joules/Kelvin)
- ``c``: the speed of light in m/s (2.998e8)
- ``T``: the positive difference between 0K and 0°C (285.15)
- ``q``: the fundamental charge (~1.602e-19 Coloumbs)

运算元和函式
~~~~~~~~~~~~~~~~~~~~~~~

常见的四则运算 ``+ - * / ^`` 可以直接使用，另外支援了特别的 "并联电阻" 运算元 ``||``。
举例来说，``1 || 2`` 表示一个 1 欧姆跟一个 2 欧姆的电阻并联，因此计算结果为 2/3 欧姆。

目前系统暂时不支援 '3!' 这种形式的阶层计算，不过有个解决的方法：使用函式。您可以使用 ``fact(3)`` 或 ``factorial(3)`` 来呼叫函式做阶层计算。

预设支援的函式如下所示：

- 三角函数: sin, cos, tan, sec, csc, cot
- 反三角函数: arcsin, arccos, arctan, arcsec, arccsc, arccot
- 常用数学函式: sqrt, log10, log2, ln, exp, abs
- 阶层: ``fact(3)`` 或 ``factorial(3)`` 都是合法的，不过要注意的是只能使用整数作为输入，举例来说： ``fact(1.5)`` 就是个不合法的计算。
- 双曲线三角函数以及其反函数: sinh, cosh, tanh, sech, csch,
  coth, arcsinh, arccosh, arctanh, arcsech, arccsch, arccoth

.. raw:: latex
  
      \newpage %



方程式响应
============

方程式响应允许使用者输入一串文字当做数学表示式，评分程式会代入指定的参数去做计算，基於数值采样符号表达式判定答案正确与否。

方程式响应与数值响应共用相同的答案格式，包含了预设的变数和函式。
不同之处在於方程式响应在评分时可以指定未知的变数，学生的答案与教师的答案可以透过随机取样的方式进行比较，端看问题作者要怎样设计。

评分程式会根据学生答案的计算结果，比对本身记录的答案。程式本身可以允许一定程度的误差，超过误差范围会被判定为错误，误差范围内则判定为正确。

这种响应型态可以控制符号表示式，不过作者本身必须额外指出哪些变数可以允许加入，计算用的数值的范围也需设定，程式才能尝试进行运算并检测答案正确与否。

系统支援使用希腊字母，当您需要使用希腊字母的时候，您可以输入下列文字，对应的希腊字母将会被自动代入：

  ``alpha beta gamma delta epsilon varepsilon zeta eta theta vartheta iota
  kappa lambda mu nu xi pi rho sigma tau upsilon phi varphi chi psi omega``

Note: ``epsilon`` is the lunate version, whereas ``varepsilon`` looks like a
backward 3.

范例问题如下：

.. image:: ../Images/image293.png
 :width: 600   

**问题代码**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
    <p>This is a short introduction to the Formula Response editor.</p>

    <p>Write an expression for the product of R_1, R_2, and the inverse of R_3.</p>
    <formularesponse type="ci" samples="R_1,R_2,R_3@1,2,3:3,4,5#10" answer="$VoVi">
      <responseparam type="tolerance" default="0.00001"/> 
      <formulaequationinput size="40" />
    </formularesponse>

    <p>Let <i>c</i> denote the speed of light. What is the relativistic energy <i>E</i> of an object of mass <i>m</i>?</p>
  <script type="loncapa/python">
  VoVi = "(R_1*R_2)/R_3"
  </script>
    <formularesponse type="cs" samples="m,c@1,2:3,4#10" answer="m*c^2">
      <responseparam type="tolerance" default="0.00001"/> 
      <text><i>E</i> =</text> <formulaequationinput size="40"/>
    </formularesponse>

    <p>Let <i>x</i> be a variable, and let <i>n</i> be an arbitrary constant. What is the derivative of <i>x<sup>n</sup></i>?</p>
  <script type="loncapa/python">
  derivative = "n*x^(n-1)"
  </script>
    <formularesponse type="ci" samples="x,n@1,2:3,4#10" answer="$derivative">
      <responseparam type="tolerance" default="0.00001"/> 
      <formulaequationinput size="40" />
    </formularesponse>

    <!-- Example problem specifying only one variable -->
    <formularesponse type="ci" samples="x@1,9#10" answer="x**2 - x + 4">
      <responseparam type="tolerance" default="0.00001"/> 
      <formulaequationinput size="40" />
    </formularesponse>

    <solution>
      <div class="detailed-solution">
        <p>Explanation</p>
        <p>Use standard arithmetic operation symbols and indicate multiplication explicitly.</p>
        <p>Use the symbol <tt>^</tt> to raise to a power.</p>
        <p>Use parentheses to specify order of operations.</p>
      </div>
    </solution>
  </problem>

**XML 属性资讯**

<script>


  .. image:: ../Images/formularesponse.png


<formularesponse>


  .. image:: ../Images/formularesponse3.png

Children may include ``<formulaequationinput/>``.

If you do not need to specify any samples, you should look into the use of the
Numerical Response input type, as it provides all the capabilities of Formula
Response without the need to specify any unknown variables.

<responseparam>


  .. image:: ../Images/formularesponse6.png

<formulaequationinput/>

========= ============================================= =====
Attribute                  Description                  Notes
========= ============================================= =====
size      (optional) defines the size (i.e. the width)
          of the input box displayed to students for
          typing their math expression.
========= ============================================= =====

.. raw:: latex
  
      \newpage %


图片响应
========

图片响应会显示一张图片并引导使用者点选特定区域作为答案。图片必须先上传到课程目录底下才能使用，评分时会判定是否正确点选到指定的矩形区块当中。

*请注意：Mozilla Firefox 尚不支援此种问题型别*

范例问题如下：

.. image:: ../Images/image294.png
 :width: 600   


**问题代码**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
  <startouttext/>
      <p>You are given three shapes. Click on the triangle.</p>
      <endouttext/>
      <imageresponse>
      <imageinput src="/c4x/edX/edX101/asset/threeshapes.png" width="220" height="150" rectangle="(80,40)-(130,90)" />
      </imageresponse>
  </problem>
  
  <problem>
      <imageresponse>
      <imageinput src="Path_to_Image_File.png" width="220" height="150" rectangle="(80,40)-(130,90)" />
      </imageresponse> 
  </problem>


**XML 属性资讯**


<imageresponse>

  .. image:: ../Images/imageresponse1.png

<imageinput>

  .. image:: ../Images/imageresponse2.png

.. raw:: latex
  
      \newpage %


自定响应
========

透过指定的输入与计算流程，您可以自行撰写一个 Python 的脚本来定义一种自定响应。

范例问题如下：

.. image:: ../Images/image295.png
 :width: 600  


**问题代码**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
  <script type="loncapa/python">

  def test_add_to_ten(expect,ans):
    try:
      a1=int(ans[0])
      a2=int(ans[1])
    except ValueError:
      a1=0
      a2=0
    return (a1+a2)==10

  def test_add(expect,ans):
    try:
      a1=float(ans[0])
      a2=float(ans[1])
    except ValueError:
      a1=0
      a2=0
    return (a1+a2)== float(expect)
  </script>

    <p>This question consists of two parts. </p>
  <p>First, enter two integers which sum to 10. </p>
  <customresponse cfn="test_add_to_ten">
          <textline size="40" /><br/>
          <textline size="40" />
  </customresponse>

    <p>Now enter two (finite) decimals which sum to 20.</p>
  <customresponse cfn="test_add" expect="20">
          <textline size="40" /><br/>
          <textline size="40" />
  </customresponse>

      <solution>
          <div class="detailed-solution">
              <p>Explanation</p>
            <p>For the first part, any two numbers of the form <i>n</i>
              and <i>10-n</i>, where <i>n</i> is any integer, will work. 
              One possible answer would be the pair 0 and 10.
            </p>
            <p>For the second part, any pair <i>x</i> and <i>20-x</i> will work, where <i>x</i> is any real number with a finite decimal representation. Both inputs have to be entered either in standard decimal notation or in scientific exponential notation. One possible answer would be the pair 0.5 and 19.5. Another way to write this would be 5e-1 and 1.95e1.
            </p>
          </div>
      </solution>
  </problem>

**样板**

*显示建议的正确答案*

.. code-block:: xml

  <problem>

  <script type="loncapa/python">
  def test_add(expect,ans):
    a1=float(ans[0])
    a2=float(ans[1])
    return (a1+a2)== float(expect)
  </script>


  <p>Enter two real numbers which sum to 20: </p>
  <customresponse cfn="test_add" expect="20">
          <textline size="40" correct_answer="11"/><br/>
          <textline size="40" correct_answer="9"/>
  </customresponse>

      <solution>
          <div class="detailed-solution">
          </div>
      </solution>
  </problem>


**样板**

*不显示建议的正确答案*


.. code-block:: xml

  <problem>

  <script type="loncapa/python">
  def test_add(expect,ans):
    a1=float(ans[0])
    a2=float(ans[1])
    return (a1+a2)== float(expect)
  </script>


  <p>Enter two real numbers which sum to 20: </p>
  <customresponse cfn="test_add" expect="20">
          <textline size="40" /><br/>
          <textline size="40" />
  </customresponse>

      <solution>
          <div class="detailed-solution">
          </div>
      </solution>
  </problem>


.. raw:: latex
  
      \newpage %

化学方程式响应
==============

化学方程式响应是一种特别的自定响应，学生可以输入化学方程式作答。

范例问题如下：

.. image:: ../Images/image296.png
 :width: 600   

**问题代码**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
    <startouttext/>
    <p>Some problems may ask for a particular chemical equation. Practice by writing out the following reaction in the box below.</p>
    <center>\( \text{H}_2\text{SO}_4 \longrightarrow \text{ H}^+ + \text{ HSO}_4^-\)</center>
    <br/>
    <customresponse>
      <chemicalequationinput size="50"/>
      <answer type="loncapa/python">

  if chemcalc.chemical_equations_equal(submission[0], 'H2SO4 -> H^+ + HSO4^-'): 
      correct = ['correct']
  else:
      correct = ['incorrect']

  </answer>
    </customresponse>
    <p> Some tips:<ul><li>Only real element symbols are permitted.</li><li>Subscripts are entered with plain text.</li><li>Superscripts are indicated with a caret (^).</li><li>The reaction arrow (\(\longrightarrow\)) is indicated with "->".</li></ul>
     So, you can enter "H2SO4 -> H^+ + HSO4^-".</p>
    <endouttext/>
  </problem> 

.. raw:: latex
  
      \newpage %

示意图响应
==========

示意图响应提供了一个互动的网格界面，学生可用来建构电子电路图。

范例问题如下：

.. image:: ../Images/image297.png
 :width: 600 

.. image:: ../Images/image298.png
 :width: 600   

.. image:: ../Images/image299.png
 :width: 600   

**问题代码**:

.. code-block:: xml


    <problem>
      Make a voltage divider that splits the provided voltage evenly.

    <schematicresponse>
    <center>
    <schematic height="500" width="600" parts="g,r" analyses="dc"
    initial_value="[["v",[168,144,0],{"value":"dc(1)","_json_":0},["1","0"]],["r",[296,120,0],{"r":"1","_json_":1},["1","output"]],["L",[296,168,3],{"label":"output","_json_":2},["output"]],["w",[296,216,168,216]],["w",[168,216,168,192]],["w",[168,144,168,120]],["w",[168,120,296,120]],["g",[168,216,0],{"_json_":7},["0"]],["view",-67.49999999999994,-78.49999999999994,1.6000000000000003,"50","10","1G",null,"100","1","1000"]]"
    />
    </center>
    <answer type="loncapa/python">
    dc_value = "dc analysis not found"
    for response in submission[0]:
      if response[0] == 'dc':
          for node in response[1:]:
              dc_value = node['output']

    if dc_value == .5:
      correct = ['correct']
    else:
      correct = ['incorrect']

    </answer>
    </schematicresponse>
    <schematicresponse>
    <p>Make a high pass filter.</p>
    <center>
    <schematic height="500" width="600" parts="g,r,s,c" analyses="ac"
    submit_analyses="{"ac":[["NodeA",1,9]]}"
    initial_value="[["v",[160,152,0],{"name":"v1","value":"sin(0,1,1,0,0)","_json_":0},["1","0"]],["w",[160,200,240,200]],["g",[160,200,0],{"_json_":2},["0"]],["L",[240,152,3],{"label":"NodeA","_json_":3},["NodeA"]],["s",[240,152,0],{"color":"cyan","offset":"0","_json_":4},["NodeA"]],["view",64.55878906250004,54.114697265625054,2.5000000000000004,"50","10","1G",null,"100","1","1000"]]"/>
    </center>
    <answer type="loncapa/python">
    ac_values = None
    for response in submission[0]:
      if response[0] == 'ac':
          for node in response[1:]:
              ac_values = node['NodeA']
    print "the ac analysis value:", ac_values
    if ac_values == None:
      correct = ['incorrect']
    elif ac_values[0][1] < ac_values[1][1]:
      correct = ['correct']
    else:
      correct = ['incorrect']
    </answer>
    </schematicresponse>

        <solution>
            <div class="detailed-solution">
                <p>Explanation</p>
                <p>A voltage divider that evenly divides the input voltage can be formed with two identically valued resistors, with the sampled voltage taken in between the two.</p>
                <p><img src="/c4x/edX/edX101/asset/images_voltage_divider.png"/></p>
                <p>A simple high-pass filter without any further constaints can be formed by simply putting a resister in series with a capacitor. The actual values of the components do not really matter in order to meet the constraints of the problem.</p>
                <p><img src="/c4x/edX/edX101/asset/images_high_pass_filter.png"/></p>
            </div>
        </solution>
    </problem>
