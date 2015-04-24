# 前言

JavaScript 的核心语言特性在 ECMA-262 标准中被定义，标准中定义的语言被称为 ECMAScript，它是浏览器和 Node.js 环境中使用的 JavaScript 语言的超集，JavaScript 保留了标准中定义的 ECMAScript 语言的核心部分，浏览器和 Node.js 通过额外的对象和方法为 JavaScript 添加更多的功能。总的来说，ECMA-262 标准的持续发展对 JavaScript 的成功来说至关重要。

2007 年，JavaScript 走到了十字路口，Ajax 的流行开创了动态 web 应用的新时代。在那之前的 8 年中（ECMA-262 标准第三版于 1999 年发布）JavaScript 语言没有任何改变。TC-39 是一个负责驱动 EMCAScript 语言发展的委员会，他们为 ECMAScript 4 整合了大量的规范草案，其内容囊括范围甚广，新增的语言特性包括：新语法、模块、类、类继承、私有对象成员、可选的类型注释等。

ECMAScript 4 的改动的内容在 TC-39 组织内部引发了巨大分歧，一些成员认为第四版试图实现的功能太多了。一些来自 Yahoo、Google 和 微软 的技术负责人为下一代 ECMAScript 提出一个可选的提案 —— ECMAScript 3.1。“3.1” 意在表明这是对现有标准的增量修改。

ECMAScript 3.1 引入的语法变动非常少，这一版标准主要实现了属性特性、原生 JSON 支持，并且为已有的对象增加方法。组织早先尝试过融合 ECMAScript 3.1 与 ECMAScript 4 这两个标准，但阵营双方在语言未来发展方向上意见分歧过大，最终以失败告终。

2008 年，JavaScript 的创始人 Brendan Eich 宣布 TC-39 组织将着重对 ECMAScript 3.1 进行标准化。直到下一个版本的 ECMAScript 被标准化之前，他们将暂时搁置 ECMAScript 4 主要语法和特性的改动，在那之后，委员会所有成员将努力提取出 ECMAScript 3.1 和 4 中的精华部分融合到一起，并赋予它一个昵称 —— ECMAScript Harmony。

ECMAScript 3.1 通过标准化后最终作为 ECMA-262 的第五版发布，同时也被称为 ECMAScript 5。委员会永不发布 ECMAScript 4，以此来避免与那个不复存在的“ECMAScript 4”产生命名冲突。后续的工作基于 ECMAScript Harmony 陆续展开，ECMAScript 6 将继承其精华成为 Harmony 之后第一个发布的标准。

ECMAScript 6 标准特性的草案早在 2014 年就已完成，新特性中全新的对象和语法模式与现有对象相去甚远。令人感到激动的是，ECMAScript 6 中一点一滴的改变全都是面向开发者实际工作中遇到的问题。ECMAScript 6 标准被完全采用并实现出开发者可接受的最小子集尚需时间，在这段日子里，如果我们能充分地了解一下 JavaScript 的未来发展将会获益良多。

## 浏览器和 Node.js 中的兼容性

开发者们正在积极地为 web 浏览器 和 Node.js 这样的 JavaScript 环境提供 ECMAScript 6 的支持。这本书不会试图找出各种实现的不同，只会关注在规范中定义的正确行为。同样，你的 JavaScript 环境也有可能与本书中所描述的行为不符。

## 目标读者

这本书打算作为一本指南供那些早已熟悉 JavaScript 和 ECMAScript 5 的读者阅读。想要深入理解这门语言不必使用这本书，它只对于你理解 ECMAScript 5 和 6 之间的差异非常有帮助。这本书特别适合想要了解这门语言的未来特性的中高级 JavaScript 开发者，无论你是在 Node.js 环境中工作还是在浏览器中编写 JavaScript，这本书都很适合你。

这本书不适合从未写过 JavaScript 的初学者，你需要对这门语言有一个相当不错的基本理解才能这本书的最大效用。

## 内容简介

**第 1 章：基础知识** 本章将介绍这门语言中最小的改动。这些新特性不一定改变原有语法，更多的是基于 ECMAScript 5 语法的增量改动。

**第 2 章：函数** 本章将讨论针对函数的多处改动。这一章的内容包括：箭头函数类型、默认参数、不定参数等。

**第 3 章：对象** 本章将为你解释在对象创建、修改、使用方面的改动，这一章的内容包括：对象字面量语法变化、新的反射方法。

**第 4 章：Symbols** 本章将介绍 symbol 的概念，一个定义属性的新方法。Symbol 是一个新的原始类型，可用于创建外部无法直接访问的对象属性和方法。

**第 5 章：数组** 本章将详述原生数组的改动，以及 JavasScrpt 中有趣的新数组应用。

**第 6 章：集合** 本章将详述四种新的集合类型：`Set`、`WeakSet`、`Map`和`WeakMap`。这些类型为数组增添了新的语义、去重机制以及专门为 JavaScript 设计的内存管理机制，这些功能极大地开拓了数组的实用性。

**第 7 章：类** 本章将介绍 JavaScript 中第一个正式的类概念。那些先前使用其它语言的开发者经常对 JavaScript 的类概念感到困惑。JavaScript 中新增的类语法使其变得更易于使用，并且对 JavaScript 热衷者来说新的类也更加简洁。

**第 8 章：迭代器和生成器** 本章将讨论这门语言中新增的迭代器和生成器。这些特性允许你使用早期 JavaScript 中不可能实现的超强方法来结合数据集合一起工作。

**第 9 章：代理** 本章将讨论新的代理对象。代理对象允许你拦截每一个在对象上执行的操作，它赋予开发者对于对象空前的控制权，同样，这也为定义新的交互模式带来无限制的可能。

**第 10 章：Promise** 本章将介绍这门语言中的新成员 Promise。Promise 是草根群体的努力成果，由于各大 JavaScript 库陆续支持 Promise，这个新功能正变得广受欢迎。ECMAScript 6 正式确定 promise 将被纳入标准，并且使之默认可用。

**第 11 章：模块** 本章将详述 JavaScript 正式的模块风格。加入这一定义旨在代替过去几年中出现过的许多非正式的模块定义风格。

**第 12 章：模板字符串** 本章将讨论新加入的内建模板功能。你可以通过模板字符串以一种安全的方式轻松创建领域特定语言。

**第 13 章：反射** 本章将介绍 JavaScript 中正式确定的反射 API。ECMAScript 6 的反射与其它语言类似，允许你在粒度级别检查你没有创建的对象。

## 帮助和支持

你可以提交 issue 告知我对文章的修改意见，也可以访问 [https://github.com/nzakas/understandinges6](https://github.com/nzakas/understandinges6) 发起一个 pull requests 来修改这本书的内容。

如果您对本书有任何疑问，可以通过邮件列表 [http://groups.google.com/group/zakasbooks](http://groups.google.com/group/zakasbooks) 跟我联系。
