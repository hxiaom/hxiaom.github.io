---
layout: post
title: 【Book】The Master of Algorithm
categories: Analytics
---

本文为《终极算法》Pedro Domingos 的读书笔记。

能够用生活中的语言，把机器学习的故事讲出来，让大家明白，真的很厉害。

* TOC
{:toc}

## 序

机器学习的核心就是预测： 预测我们想要什么，预测我们行为的结果，预测如何能实现我们的目标，预测世界将如何改变。

机器学习主要有5个学派，我们会对每个学派分别介绍：

1. 符号学派将学习看作逆向演绎，并从哲学、心理学、逻辑学中寻求洞见；
2. 联结学派对大脑进行逆向分析，灵感来源于神经科学和物理学；
3. 进化学派在计算机上模拟进化，并利用遗传学和进化生物学知识；
4. 贝叶斯学派认为学习是一种概率推理形式，理论根基在于统计学；
5. 类推学派通过对相似性判断的外推来进行学习，并受心理学和数学最优化的影响。

机器学习的5个学派都有自己的主算法：

1. 符号学派 - 逆向演绎；
2. 联结学派 - 反向传播；
3. 进化学派 - 遗传编程；
4. 贝叶斯学派 - 贝叶斯推理；
5. 类推学派 - 支持向量机

## 第一章 机器学习革命

### 机器学习算法入门

每个算法都会有输入和输出：数据输入计算机，算法会利用数据完成接下来的事，然后结果就出来了。机器学习则颠倒了这个顺序：输入数据和想要的结果，输出的则是算法，即把数据转换成结果的算法。学习算法能够制作其他算法。

学习算法是种子，数据是土壤，被掌控的程序是成熟的作物。机器学习专家就像农民，播下种子，灌溉，施肥，留意作物的生长状况，事事亲力亲为，而不是退居一旁。

一旦我们这样看待机器学习，随即也会发生两件事：

第一，我们掌握的数据越多，我们能学的也越多。

第二，机器学习是一把剑，利用这把剑可以杀死复杂性怪兽。只要有足够的数据，一段只有几百行代码的程序可以轻易生成拥有上百万行代码的程序，而且它可以为解决不同问题不停产生不同的程序。

有些学习算法学习知识，有的则学习技能。在机器学习中，知识往往以统计模型的形式出现，技能往往以程序的形式出现。

机器学习有时会和人工智能（AI）混淆。严格来讲，机器学习是人工智能的子领域。人工智能的目标是教会计算机完成现在人类做得最好的事，而机器学习可以说就是其中最重要的事。

在信息处理这个生态系统中，学习算法是顶级掠食者。数据库、网络爬虫、索引器等相当于食草动物，耐心地对无线领域中的数据进行蚕食。统计算法、线上分析处理等则相当于食肉动物。食草动物有必要存在，因为没有它们，其他动物无法存活，但顶级掠食者有更为刺激的生活。数据爬虫就像一头牛，网页相当于它的草原，每个网页就是一根草。当网络爬虫进行破坏行动时，网站的副本就会保存在其硬盘中。索引器接着做一个页面的列表，每个词都会出现在页面当中，这很像一本书后的索引。数据库就像大象，又大又重，永远不会被忽略。在这些动物当中，耐心的野兽飞快运转统计和分析算法，压缩并进行选择，将数据变为信息。学习算法将这些信息吞下、消化，然后将其变成知识。

计算机科学通常需要的是准确思维，但机器学习需要的是统计思维。这种思维上的差别很大程度上也解释了为什么微软能赶上网景公司，但想赶上谷歌却困难得多。

工业革命使手工业自动化，信息革命解放了脑力劳动，而机器学习则使自动化本身自动化。

### 为什么商业用户机器学习 （商业变革）

当公司不断发展壮大后，它会经历三个阶段：第一阶段的所有事都由人工完成；第二阶段是最辛苦的时期，公司变得越来越大，需要用到计算机。经过一段时间进入第三阶段，没有足够的程序员和顾问满足公司的需要，因此公司不可避免地向机器学习寻求帮助。

公司确保学习算法喜爱其产品的最佳方法就是，让公司自己运行算法。谁有最佳算法、数据最多，谁就能赢。新型网络效应占据上风：谁有最多的用户，谁就能积累最多的数据，谁有最多的数据，谁就能学到最好的模型，谁学到最好的模型，谁就能吸引最多的用户，这是一种良性循环。

你可能会认为，过一段时间，更多的数据结果意味着更多的重复，但数据的饱和点还未出现，长尾效应持续起作用。

### 给科学方法增压 （科学变革）

机器学习是”打了类固醇“的科学方法，也遵循同意的过程：产生假设、验证、放弃或完善。科学家可能会花费毕生精力来提出或验证几百个假设，而机器学习系统却能在一秒钟内完成这些事。机器学习使科学的发现过程自动化。因此，并不奇怪，这既是商业领域的革命，也是科学领域的革命。

为了取得进步，科学的每个领域都需要足够的数据，以与其研究现象的复杂性相对应。大数据时代使得有更多数据。

然而最大的挑战就是将所有这些数据组合成一个整体。导致你患心脏病的因素有哪些？这些因素如何互相影响？牛顿需要的只是三个运动定律和一个万有引力定律，但一个细胞、一个有机体、一个社会的完整模型却无法由一个人来发现。虽然随着知识的增长，科学家的分工变得越来越细，但是没有人能够将所有知识整合到一起，因为知识太多了。虽然科学家们会合作，但语言是传播速度非常缓慢的介质。虽然科学家们想努力追上别人的研究，但出版物的数量如此之多，他们的距离被拉得越来越远。通常是，重做一项实验比找到该实验的报告还要容易。机器学习在这时就会起作用，它能根据相关信息搜索文献，将某领域的行话翻译到另一个领域，并建立联系，而科学家们在过去都没有意思到。渐渐地，机器学习成为一个巨大的中心，通过这个中心，某领域里发明的建模技术将会被引入其他领域。

### 10亿个比尔·克林顿 （政治变革）

政治家最大伟大的才能之一，就是能够了解其选民个人或者选民团体，然后直接与他们对话，比尔·克林顿就是其中的一个典范。机器学习的作用就是，让每位选民都觉得克林顿对待他们亲力亲为、非常用心。

学习算法是最强大的政治家推销商。

更大范围的结果就是，民主会更好地得到实现，因为选民与政治家之间交流的范围会飞速扩大。

### 学习算法与国家安全 （军事变革）

寻找恐怖分子。预测犯罪倾向。

### 我们将走向何方

## 第二章 终极算法

如果那么少的学习算法就可以做那么多事，那么有一个逻辑上的疑问：单个学习算法可以把所有事情都做完吗？换句话说，单个算法可以学习所有能从数据中学习的东西吗？这是一个非常艰巨的任务，因为这基本上包含成年人大脑里以及人类进步所创造的一切，还有所有科学知识的总和。实际上，对所有主要的学习算法——包括最近邻算法、决策树学习算法以及贝叶斯网络(朴素贝叶斯的概况)——来说，如果你为学习算法提供足够、适当的数据，该算法可以实现任一功能（对学习任何东西来说，都与数学相关）。需要注意的是，“足够的数据”也有可能无限。

学习无限数据需要做出假设，如我们会看到的那样，而且不同的学习算法会有不同的假设。如果不把这些假设嵌入算法中，而是将其连同是数据一起，当作显示输入，并允许用户选择插入哪一个，甚至陈述新的假设，那么会怎么样？有没有这种算法，可以接受任何数据及假设并输出隐藏其中的知识？我相信有。当然，我们得限制假设的可能性，否则如果把整个目标知识都以假设形式赋予算法，那就是在作弊。我们可以通过限制输入的规模、要求假设弱于当前学习算法等方法，来实现这个Udine。

那么疑问就会变成：这些假设要弱到何种程度，但仍能够从无限数据中获得所有相关知识？注意“相关”这个词：我们仅仅对存在于世界的知识感兴趣，对不存在的世界没有兴趣。

这就是本书的中心假设：

**所有的知识，无论是过去的、现在的还是未来的，都有可能通过单个通用学习算法来从数据中获得。**

### 来自神经科学的论证

对于天生看不见的人，视觉皮层可以负责大脑的其他功能。对于听不见的人，听觉皮层也可以这么做。大脑皮层具有一定统一性。

### 来自进化论的论证

生物多元性源于单一机制：自然选择。

套用查尔斯·巴贝奇（维多利亚时期的计算机先驱人物）的观点，上帝创造的不是物种，而是创造物种的算法。

利用足够多的数据，一种简单的算法能掌握什么？关于这个问题，最经典的例子就是进化论。输入进化论这个算法的信息是所有存在过的、活着的生物的经历以及命运（对现在的算法来说是大数据）。此外，这个进化论算法已经在地球上最强大的计算机运行了300多万年——这台强大的计算机就是地球自己。运行这个算法的真正计算机应该比地球这台“计算机”运转更快、数据密集性更低。

### 来自物理学的论证

生物学是进化学在物理学和化学的约束下进行优化的结果，而物理定律本身又是最优化问题的解决方法。

### 来自统计学的论证

根据一个统计学流派的观点，所有形式的学习都是基于一个简单的公式——如我们所知，就是贝叶斯定理。贝叶斯定理会告诉你，每当你看到新的证据后，如何更新你的想法。

### 来自计算机科学的论证

人工智能的其中一个定义是，人工智能包括找到NP完全问题的所有启发性解决方案。

### 机器学习算法和知识工程师

对终极算法最坚定的反抗来自机器学习永恒的敌人：知识工程。

根据知识工程支持者的观点，知识无法自动被学习，必须通过人类专家编入计算机，才能对它进行学习。的确，学习算法能从数据中提取一些东西，但你不能将这些东西和真知识混为一谈。

尽管机器学习成功了，知识工程师们还是觉得不信服。他们相信，机器学习的局限性很快就会变得明显，钟摆会摆回来，局势会扭转。

### 天鹅咬了机器人

《黑天鹅》一书中强调，有些事情真的无法预料。

有些事可预料，而有些事却不可预料，这个说法是正确的。而机器学习算法的首要任务就是区别可预测的事和不可预测是事。

### 终极算法是狐狸，还是刺猬

有些思想家就是狐狸——他们知道许多微小的事情；而有些思想家则是刺猬——他们知道一件大事。学习算法也是同样情况。我希望终极算法是一只刺猬，但即使它是只狐狸，我们也没法很快抓住它。

### 我们正面临什么危机

许多领域迫切需要通用学习算法

### 新的万有理论

终极算法会给出所有学科的统一思想，并有潜力提出一套新的万有理论。

### 未达标准的终极算法候选项

等式U(X)=0

### 机器学习的五大学派

1. 符号学派 - 逆向演绎；
2. 联结学派 - 反向传播；
3. 进化学派 - 遗传编程；
4. 贝叶斯学派 - 贝叶斯推理；
5. 类推学派 - 支持向量机

## 第三章 符号学派：休谟的归纳问题

### 约不约

自休谟提出归纳问题，哲学家就已经对此进行辩论，但还没有人能给出一个满意的答案。勃兰特·罗素喜欢用“归纳主义者火鸡”这个故事来阐述这个问题。故事的主人公是一只火鸡，它来到农场的第一个早晨，主人在早上9点喂它们，但作为实实在在的归纳法优越论者，它不想过早下结论：主人每天都9点喂它们。首先它在不同情况下观察了很多天，收集了许多观察数据。主人连续多天都是9点喂它们，最终它得出结论，认为主人每天早上9点喂火鸡，那么主人一直会在早上9点给它喂食。接下来是平安夜那天的早晨，主人没有喂它，因为它被宰了。

也许这也不是什么大问题？有了足够的数据，大多数事件不就变得“微不足道”了吗？不是的。我们在前面的章节中了解到，为什么记忆不能当作通用学习？我们现在可以用更量化的方式来解释这个问题。假设你现在有一个数据库，含有1万亿条记录，每条记录有1000个布尔字段（也就是说，每个字段回答一个是或否的问题）。这个数据库真的好大。你认为有多少种可能的事件？无论有多少数据——多少兆、多少千兆，你基本上什么也看不到。你要决定的新事件已经存在于数据库中，而数据库非常大，这件事发生的概率低到可以忽略，所以如果不进行一般化，对你就不会有任何帮助。

### “天下没有免费的午餐”定理

沃尔伯特原来是一名物理学家，后来成为机器学习者。他的研究结果被人们称为“天下没有免费的午餐”定理，规定“怎样才算是好的学习算法”。这个规定要求很低：没有哪个学习算法可以比得上随意猜测。

如果存在学习算法比随机猜测好用的领域，我（一个喜欢唱反调的人）会构建一个学习算法没有随机猜测好用的领域。我要做的就是把所有“未知”例子的标签翻过来。因为“经过观察”的标签表明，你的学习算法绝无可能区分世界和反物质世界。在这两个世界中的平均表现，学习算法和随机猜测一样好用。

虽然如此，但我们不关心所有可能存在的世界，而只关心我们生存的这个世界。

只有数字也不够。从零开始只会让你，只会让你一无所有。机器学习就像知识泵，我们可以用它来从数据中提取大量的知识，但首先我们得先对奔进泵进行预设。

数学家认为机器学习这个问题是一个不适定问题（ill-posed problem）。这个问题没有唯一解。下面是一个简单的不适定问题。哪里两个数相加等于的得数是1000？假设这两个数都是正数，答案就有500种……1和999，2和998等等。解决不适定问题的唯一办法就是引入附加假设。如果我告诉你，第二个数是第一个数的三倍，那么答案就是250和750.

汤姆·米切尔（Tom Mitchell）是典型的符号学者，称机器学习体现“无偏见学习的无用性”。在日常生活中，“偏见”是一个贬义词：预设观念不太好。但机器学习中，预设观念是必不可少的；没有这些观念，你就无法进行学习。实际上，预设观念对人类知识来说，也是必不可少的，这些观念是“直线布入”人脑的。对于它们，我们也觉得理所当然的。超出那些观念的偏见才值得质疑。

机器学习不可避免地含有投机的因素。误差是常有的事，并不意外。但没关系，因为我们放弃误差的部分，主要靠没有误差的部分，而计算结果才是最重要的。我们一旦掌握新的知识，基于前面的步骤，就可以得出更多的知识。唯一的问题就是，从哪里开始。

### 对知识泵进行预设

我们见过的所有真实的东西，在宇宙中也是真实的。

牛顿法则是机器学习的第一个不成文规则。我们归纳自己能力范围内、应用最广泛的规则，只有在数据的迫使下，才缩小规则的应用范围。乍一看，这看起来可能过于自信甚至，近乎荒谬，但这种做法已经为科学服务了300余年。当然也可以想象出一个变化无常的宇宙，在那里牛顿法不起作用，但那并不是我们的宇宙。

牛顿法则仅仅是第一步。还得弄明白我们见到的哪些是真实的——如何从原始数据中找出规律。标准的解决方法就是假设我们知道真理的形式，而算法的任务就是把这个形式具体化。

首先做有条件的假设，如果这样无法解释数据，再放松假设的条件，这就是典型的机器学习。这个过程通常由算法自行进行，不需要你的帮助。首先，算法会尝试所有单一因素，然后尝试所有两个因素的组合，之后就是所有三个因素的组合等。但现在我们遇到一个问题：合取概念太多，没有足够时间对其逐个尝试。

这里有一种方法：暂且假设每个配对都合适，然后排除所有不含有某种品质的搭配，对每种品质重复同样的做法，然后选择那个排除了最多不当搭配和最少适合搭配的选项。

### 如何征服世界

所有规则都会有例外。

我们要做的就是学习一系列规则定义的概念，而不仅仅是单个规则。

### 在无知与幻觉之间

规则集在很大程度上比合取概念要有力得多。实际上，规则的力量如此之大，大到你可以用规则来代表任何概念，要找到原因则很难。

规则集的力量是一把双刃剑。从正面看，你知道自己总能找到和数据完美匹配的规则。但你还没来得及开始觉得走运，就意识到自己很有可能会找到一个毫无意义的规则。记住“天下没有免费的午餐”：没有知识，你就无法进行学习。假设某概念能通过规则集来定义，相当于什么也没有假设。

每当算法在数据中找到现实世界不存在的模型时，我们就说它与数据过于拟合。过拟合问题是机器学习中的中心问题。避免幻觉模式唯一安全的方法，就说严格限制算法学习的内容，例如要求学习内容是一个简短的合取概念。很遗憾，这种做法就像把孩子和洗澡水一起倒掉一样，会让学习算法无法看到多数真实的模型，这些模型在数据中是可见的。因此，好的学习算法永远在无知和幻觉的夹缝中行走。

学习算法特别容易过拟合，因为它们拥有从数据中发现模型、近乎无限制的能力。

约翰·冯·诺依曼曾说过一句众所周知的话：“用4个参数，我能拟合一头大象；用5个参数，我可以让它的鼻子扭动起来。”当今我们通常会学习拥有数百万参数的模型，这些参数足以让世界上的每头大象都扭动鼻子。甚至曾有人说过，数据挖掘意味着“折磨数据，直到数据妥协。”

当你有过多假设，而没有足够的数据将这些假设区分开来时，过拟合问题就发生了。坏消息是，即便对最简单的合取概念算法来说，假设的数量也会随着属性的增多和呈指数级增长。幸运的是，在学习过程中，会发生一些事，把其中一个指数消除，只剩下一个“普通的”单一指数难解型问题。

总结：学习就是你拥有的数据的数量和你所做假设数量之间的较量。更多的数据会呈指数级地减少能够成立的假设数量，但如果一开始就做很多假设，最后你可能还会留下一些无法成立的假设。一般来说，如果学习算法只做了一个指数数量的假设（例如，所有可能的合取概念），那么该数据的指数报酬会将其取消，你毫无影响，只要你有许多例子，且属性不太多。另外，如果算法做了一个双指数的假设（例如，所有可能的规则集），那么数据只会取消其中的一个指数，而且你仍会处于麻烦之中。你甚至可以提前弄明白自己需要多少个例子，这是为了保证算法选择的假设和准确的那个非常接近，只要它对所有数据都拟合。换句话说，是为了假设能够尽可能准确。哈佛大学的哈斯利·瓦里安特获得图灵奖，因为他发明了这种分析方法，他在自己的书中将这种方法取名为“可能近似正确”（probably approximately correct），非常恰当。

### 你能信任的准确度

在实践中，瓦里安特式的分析方法往往非常被动，而且需要的数据比你拥有的还要多。那么你怎么决定，是否要相信学习算法告诉你的东西呢？这个很简单：在利用学习算法过去看不到的数据对其进行证实之前，你不要相信任何东西。

测试数据中的准确度就是机器学习中的“黄金标准”。

此前不可见数据的准确度测试确实是一个相当严格的考验，实际上，科学的很多方面都因此没有经得住考验。这并不意味着科学就没有用了，因为科学不仅仅是用来预测的，还能用来解释和理解。但是最后，你的模型如果无法对新的数据做出准确预测，就无法保证自己真的理解或者解释了隐藏在背后的现象。对于机器学习来说，对不可见数据的测试是必不可少的，因为这是判断学习算法是否过拟合的唯一方法。

即使测试集准确度也会出现问题。据说，在早期军事应用中，一种简单的学习算法探测到坦克的训练集和测试集的准确度都为100%，两个集由100张图片组成。结果是所有坦克的图片都比没有坦克的图片亮，所以学习算法就都挑了较亮的图片。

在机器学习从新生领域成长为成熟领域的过程中，务实的经验评价会起到重要的作用。利用加州大学欧文分校的机器学习小组维护的普通实验框架和大型数据集存储库，我们会取得重大进步。

知道何时过拟合这一点还不足够，我们需要第一时间避免过拟合。这就意味着不再对数据进行完全拟合，即便我们能做到。有一个方法就是运用统计显著性检验来确保我们看到的模型真实可靠。如果我们尝试了一条规则，400个例子中的准确率是75%，我们可能会相信这个规则。但如果我们尝试了100万条规则，其中最佳的规则中，400个例子中的准确率是75%，可能就不会相信这个规则，因为这很有可能是偶然发生的。在机器学习中，我们可以把自己尝试了多少条规则记录下来，然后相应地调整显著性检验，不过那样做，这些检验可能会把可靠的规则连同不可靠的一起丢弃。更好的方法就是认识到有些错误的假设会不可避免成立，但要控制它们的数量，方法就是否定低显著性2的假设，然后对剩下的假设做进一步的数据检测。

另一个流行的方法就是选择更加简单的假设。但为了和过拟合做斗争，我们要对更简单的规则有更强的偏好，这样就能在所有负面例子被包含之前，就停止添加条件。

如果你的学习算法检测集准确度不尽如人意，你就得诊断问题在哪里。是因为无知，还是因为幻想？在机器学习中，这些的专业叫法为“偏差”和“方差”。你可以估算一种学习算法的偏差和方差，方法就是在掌握训练集的随机变量之后，对算法的预测进行对比。如果算法一直出错，那么问题就出在偏差上，而你需要一个更为灵活的学习算法（或者只和原来的不一样即可）。如果出现的错误无模式可循，问题就出在方差上，而你要么尝试一种不那么灵活的学习算法，要么获取更多的数据。

### 归纳是逆向的演绎

### 掌握治愈癌症的方法

### 20问游戏

逆向演绎的另外一个局限性就在于，它涉及很密集的计算，因此很难拓展到海量数据集中。因为这些原因，符号学家选择的算法是决策树归纳。

### 符号学派

符号学派的核心理念就是，所有和智力相关的工作都可以归结为对符号的操纵。

符号注意机器学习到了80年代，它们迅速传播，后来却消失了。它们消失的主要原因是人人逃避的知识习得瓶颈：从专家身上提取知识，然后将其编码成为规则，这样做难度太大、太费力、易出故障，会引起很多问题。

另一个重要的问题就是基于知识的系统在处理不确定性时会有问题，在第六章会深入探讨这个问题。

## 第四章 联结学派：大脑如何学习

在符号学派中，符号和它们代表的概念之间有一一对应的关系。相反，联结学派的代表方式却是分散的：每个概念由许多神经元来表示，而每个神经元又会和其他神经元一起代表许多不同的概念。

符号学派和联结学派的另一个区别在于，前者是按次序的，而后者是平行的。

### 感知器的兴盛与衰亡

### 物理学家用玻璃制作大脑

### 世界上最重要的曲线

### 攀登超空间里的高峰

超空间是一把双刃剑：一方面，空间的维度越高，它越有可能存在高度复杂的表面和局部最优解；另一方面，被困在局部最优解中，意味着被困在每个维度中，所以被困在多维中的难度会比被困在三维中的难度大。

### 感知器的复仇

### 一个完整的细胞模型

### 大脑的更深处

掌握拥有一个隐含层的网络没问题，但在那之后，很快事情就会变得很困难。几层的网络，只有为了应用（比如文字识别）而经过精心设计的才能起作用。超出这个范围，反向传播就会瘫痪。随着我们增加越来越多的层数，误差信号会变得越来越散漫，就像河流分成越来越小的支流，直到我们只剩下雨滴，不留痕迹。

“自动编码器”：让隐含层比输入和输出层小很多，那么网络就不会只把输入信息复制到隐含层，然后再从隐含层复制到输出信息那里。

花了十余年来寻找的诀窍，就是让隐含层比输入和输出层小一些？实际上，这只是一半的诀窍，另一半就是，在任何特定时间，只把几个隐藏的单位赶走。这叫做稀疏自动编码器。

下一个聪明的主意就是把稀疏自动编码器逐个堆积起来。

## 第五章 进化学派：自然的学习算法

### 达尔文的算法

遗传算法能够频繁作弊的方法，就是允许有永不灭亡的东西。

### 探索：利用困境

我们应该注意遗传算法和多层感知器的差异程度。反向传播会在任何给定时间坚持单一假设，而且这个假设会渐渐改变，直到其适应某个局部最优值。遗传算法会在每一步中考虑整个群体的假设，而由于交叉行为，这些假设可以从这一代跨到下一代。

机器学习中最重要的问题之一（也是关于生命最重要的问题之一），就是探索-利用困境。如果已经找到能发挥作用的东西，你还好继续找吗？

### 程序的适者生存法则

### 性有何用

### 先天与后天

“鲍德温效应”

### 谁学得最快，谁就会赢

## 第六章 贝叶斯学派：在贝叶斯教堂里

### 统治世界的定理

对于贝叶斯学派来说，学习“仅仅是”贝叶斯定理的另外一个运用，将所有模型当作假设，将数据作为论据：随着你看到的数据越来越多，有些模型会变得越来越有可能性，而有些则相反，直到理性的模型渐渐突出，成为最终的胜者。

贝叶斯学派的回答是：概率并非频率，而是一种主观程度上的信任。因此，用概率来做什么由你决定，而贝叶斯推理让你做的事就是：通过新证据来修正你之前相信的东西，得到后来相信的东西（也被人们称为“转动贝叶斯手柄”）

### 所有模型都是错的，但有些却有用

如果学习算法利用贝叶斯定理，且给定原因时，假定结果相互独立，那么该学习算法被称为“朴素贝叶斯分类器”。

起初看起来可能不是这样，但朴素贝叶斯法与感知器算法密切相关。感知器增加权值，而朴素贝叶斯法则增加概率，但如果你选中一种算法，后者会转化为前者。

### 从《尤金·奥涅金》到Siri

### 所有东西都有关联，但不是直接关联

### 推理问题

### 掌握贝叶斯学派的方法

### 逻辑与概率：一对不幸的组合

## 第七章 类推学派：像什么就是什么

### 完美的另一半

### 维数灾难

### 空中蛇灾

### 爬上梯子

### 起床啦

## 第八章 无师自通

### 物以类聚，人以群分

### 发现数据的形状

### 拥护享乐主义的机器人

### 熟能生巧

### 学会关联

## 第九章 解开迷惑

### 万里挑一

### 终极算法之城

### 马尔科夫逻辑网络

### 从休谟到你的家用机器人

### 行星尺度机器学习

### 医生马上来看你

## 第十章 建立在机器学习之上的世界

### 性、谎言和机器学习

### 数码镜子

### 充满模型的社会

### 分享与否？方式、地点如何？

### 神经网络抢了我的工作

### 战争不属于人类

### 谷歌+终极算法=天网？

### 进化的第二部分

## 后记