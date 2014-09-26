.. raw:: latex
  
      \newpage %
      

======================
附录 D: 时区
======================

    **概要**
    ~~~一次释出课程教材让所有学生可以看见，在具体制定的时间，有截止日期的作业将一次be due给所有学。 //参考改法：一次更新的课程教材所有学生均可看到，在具体设定的时间，这些有截止日期的作业对于所有学生均将一次性到期。
	然而，许多地方在edX及Studio提出一种时间设定无须指定时区。除非另有规定，大部分日期和时间在Studio和edX中是世界标准时间(下简称UTC)而不是您当地的时区!
	当您设置日期和时间没有设定时区时，您需要转换为UTC。
	您也应该确保学生和老师理解您课程中的时间设定方式。
	
    **详述**
    时间被储存在一个特别的时区中。然而，这个时区可能不会显示在介面中。未标签的时间值以UTC格式被指定、储存，和观看。

	
    Edx和Studio处理时区如下。

    ?	所有时间，不论是标签的还是未标签的，都被在服务器上以UTC格式存储 (a.k.a. UTC or Z)。
    ?	未标签时间不论是在Studio或edX/Edge上均以UTC格式显示。
    ?	在Studio中一个特别时区的时间标签将被具体指明在那个时区，并且转换为UTC。 (这是罕见的。)

    在Studio中的设定，被标签为一个时区，例如课程开始和结束的时间，输入设定在时区中具体指明出来 (通常是您当地时区)。
	
    未标签时区的时间设定，例如课程内容的发表日期和截止日期，从您的当地时区进行转换，并以UTC格式设定日期和时间。您可以使用线上时区转换来转换成为您的当地时区时间。
	
    ~~~*请注意当您使用线上转换时，进入夏令时的时间时需考虑到一天的时间。*

																																		
    例如美国东部标准时间是 "UTC-5"，所以在Studio中纽约的冬令时下午5:00（17:00）截止日期应输入为晚上10:00（或22:00）。 美国夏令时时间，然而，是UTC-4，所以在Studio中纽约的夏天截止日期下午5:00应该输入为下午9:00。

    
	在edX/Edge以学生的角度这些时间设定大部分也不会被加上标签。 当您设定了一个作业的截止日期，请确定学生理解这个截止日期。您可以选择下列方法之一。

    ?	随时提前通知学生，除非另有标签，否则都会被显示成UTC格式，提醒他们通过时区转换来转换到他们当地时区的时间。
    ?	Allow students to assume that all due dates are specified in their local time zone, and specify an unadvertised grace period to invisibly extend all the due dates in your course. For example, some courses set a grace period of "1 day, 6 hours, and 1 minute" to accommodate differences in time zones and any potential system issues. //参考改法：让学生们把您设定的时间理解为他们的当地时区时间，并且设置一个隐藏的时间宽限期。比如，某些课程可以设定一段类似“1天，6小时，1分钟”的宽限期，这样的宽限期可以用来适应时区的差异和可能存在的系统问题。

    *请注意一般不建议设定这样的宽限期。它可能导致问题在应该关闭时没能关闭，同时也可能会误导您的学生。*

    如果您有进一步关于指定时间和时区的问题，或者发现了截止日期或更新日期不一致的情况，请从edX Studio的帮助页面联络我们。

    **参考文献**

    http://help.edge.edx.org/discussions/questions/61-time-zones

    http://help.edge.edx.org/discussions/questions/23-grace-periods
