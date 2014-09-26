.. raw:: latex
  
      \newpage %
      

======================
附录 D: 时区
======================

    **概要**
    一次释出课程教材让所有学生可以看见，在具体指名的设定时间，有截止日期的作业将一次be due给所有学。
	然而，许多地方在edX及Studio提出一种时间设定无须指定时区。除非另有规定，大部分日期和时间在Studio和edX中是UTC而不是您当地的时区!
	当您指定日期和时间设定没有一个时区标签，您需要转换值为UTC。
	您也应该确保学生和老师知道如何理解您课程中的时间设定。
	
    **详述**
    时间被储存在一个特别的时区中。然而，这个时区可能不会显示在介面中。未标签的时间值以UTC格式被指定、储存，和观看。

	
    Edx和Studio处理时区如下。

    ?	所有时间，标签和未标签，都被储存在伺服器上以UTC格式 (a.k.a. UTC or Z)。
    ?	未标签时间被显示在不论是Studio或edX/Edge上以UTC格式。
    ?	在Studio中一个特别时区的时间标签被具体指明在那个时区，并且转换为UTC。 (这是罕见的。)

    在Studio中的设定，被标签为一个时区，像是课程开始和结束时间，输入设定在时区中具体指明出来 (通常是您当地时区)。
	
    未标签时区的时间设定，像是课程内容的释出日期和截止日期，从您的当地时区转换，以及设定日期和时间以UTC格式。您可以使用线上时区转换来转换成为您的当地时区时间。
	
    *请注意当您使用一个线上转换，进入日光节约日子时间时同时考虑到一天的时间。*

																																		
    例如美国东部标准时间是 "UTC-5"，所以在Studio中纽约的冬天下午5:00（17:00）截止日期应输入为晚上10:00（或22:00）。 美国日光节约时间，然而，是UTC-4，所以在Studio中纽约的夏天截止日期下午5:00应该输入为下午9:00。

    
	在edX/Edge以学生的角度这些时间设定大部分也不会被标签。 当您设定了一个作业的截止日期，请确定告诉学生该如何解释这个截止日期。您可以选择下列选项之一。

    ?	随时提前通知学生，除非另有标签，都会被显示成UTC格式，指点他们到一个时区转换来转换他们当地时区时间。
    ?	Allow students to assume that all due dates are specified in their local time zone, and specify an unadvertised grace period to invisibly extend all the due dates in your course. For example, some courses set a grace period of "1 day, 6 hours, and 1 minute" to accommodate differences in time zones and any potential system issues.

    *请注意一般不建议设定一个宽限期。它可能导致问题没有关闭 "when they should"，以及可能会误导您的学生。*

    如果您有进一步关於指定时间和时区的问题，或者正遭受截止日期或释出日期不一致的特性，请从edX Studio的帮助页面联络我们。

    **参考文献**

    http://help.edge.edx.org/discussions/questions/61-time-zones

    http://help.edge.edx.org/discussions/questions/23-grace-periods
