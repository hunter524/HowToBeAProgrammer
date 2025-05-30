# 如何分析数据

当你检查一个商业活动并且发现了把它转换为软件应用程序的需求时，数据分析是软件开发早期的一个过程。这是一个官方的定义，当你，一个程序员，应该集中注意力在写别人设计的东西的代码时，这可能会让你相信数据分析是一种更应该归入系统分析的行为。如果我们严格遵循软件工程范式，这可能是正确的。有经验的程序员会成为设计者，最尖锐的设计者变成商业分析师，因此被冠名去思考所有数据需要，并且给你充分定义的任务去执行。这不完全是对的，因为数据是每种编程活动的核心。不管你在你的程序里做什么，你不是在移动数据就是在修改数据。商业分析师分析的是更大尺度上的需要，软件设计者更加压榨这个比例以至于，当问题在你的桌上落地时，好像你需要做的所有事情是应用聪明的算法，开始移动已经存在的数据。

不是这样的。

不管你开始观察它的是哪个阶段，数据是一个良好设计的应用程序主要考虑的因素，如果你仔细观察一个数据分析师是怎么从客户请求中获取需求的，你会意识到，数据扮演了一个基本的角色。分析师创建了所谓的数据流表，所有的数据源被标记出来，信息的流动被塑造出来。清晰定义了什么数据应该是系统的一部分，设计师将会用数据关系，数据交换协议，文件格式的形式塑造数据源，这样任务就准备好传递给程序员了。然而，这个过程还没结束，因为你（程序员）在这个周密的数据提取过程后，需要分析数据以用最好的可能方式表现任务。你的任务的底线是 Niklaus Wirth，多种语言之父，的金句：“算法+数据结构=程序”。这永远不是一个独立的自嗨的算法。每个算法都至少被设计去做一些至少与一段数据相关的事情。

因此，由于算法不会在真空中滚动轮子，你需要分析其他人已经为你标记好的数据和必须写入代码的必要的数据。 一个小例子会使得事情更清楚。实现一个图书馆的搜索程序时，通过你的说明书，用户用类型/作者标题/出版社/出版年份/页数来选择书本。你的程序的中级目标是提供一个合法的 SQL 语句去搜索后端数据库。基于这些需要，你有几个选择：按顺序检查每个控制条件，使用一个 switch 语句，或者几个 if 语句；用一个数据控制数组，把它们与一个事件驱动引擎相连。

如果你的需求也包括提高查询性能，通过确认每个项在一个特殊顺序里，你可能考虑使用组件树去构建你的 SQL 语句。正如你可以看到的，算法的选择依赖于你决定使用或将要创建的数据。这样的决定产生高效算法和糟糕算法间的区别。 然而,效率不是唯一要考虑的因素。你可能在你的代码里使用一打命名变量，让它变得尽可能高效。但这样一段代码可能不能容易地维护。可能为你的变量选择一种合适的容器可以保持相同的速度，此外，在的你同事明年看代码的时候，让他们能够更好地理解代码。更多的，选择一个良好设计的数据结构可能允许他们在不重写代码的前提下，拓展你的代码的功能。长久看来，你对数据的选择决定了你结束代码的工作后，它能工作多久。

让我给你看另一个例子，只是一些思想粮食，让我们假设你的任务是找到字典里超过三位的同字异构词（一个异构词必须在同样的字典里有另一个词）。如果你把这当做一个计算任务，你将会结束于无尽的，尝试找出每个单词的所有组合，然后拿它跟列表里的所有其他单词比较，这样一个无尽的努力中。然而，如果你分析了手头的数据，你会意识到，每个单词可能被一个包含这个词本身以及用它的字母作为 ID 的排序数组的记录所代表，这个蛮力算法可能需要运行几天，而小的那个算法只是一件几秒的事。下次面对一个棘手的问题时，记住这个例子。

Next [团队技能 - 如何管理开发时间](../Team-Skills/01-How-to-Manage-Development-Time.md)
