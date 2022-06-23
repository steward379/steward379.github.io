---
title : Javascript 這個討厭鬼！
subtitle: 幾乎每個寫程式的人，都曾經討厭 Javascript 一遍、兩遍
description: 很多人從 jQuery 走到 Javascript 就卡關了。支持先學 Javascript 的那一派説，沒有對那種 Functional 的程式語言有所了解 ，又要如何從 html, css, jQuery 的思維跨越到那種「真正」的程式語言呢？但這知易行難呀！即使，像我一開始就碰 Javascript，卻被相關原理弄得暈頭轉向，感覺東缺西缺。直到⋯⋯
---
> 「分號又忘了加！」、「奇怪是不是忘了括號？」的日子持續不斷，面對龐雜的程式碼，雖然感恩 Es6+ Seafood 用載入 import 與箭頭函數 => 稍微感化了 Javascript。但看看彈性有趣的 Ruby、 Python 的簡潔與美麗！又看看其他強型別語言雖麻煩而嚴謹，甚至做物聯網的 Processing 跟 Arduino (註一) 也提供程式初學者創造的可能性。 但是，Javascript 真讓人覺得麻煩又怪異。糟了，是 Javascript！

幾乎每個寫程式的人，都曾經討厭 Javascript 一遍、兩遍 —— 或者一直討厭下去。畢竟，一個總是讓人摸不著頭緒，花幾天就寫成的語言，即使經過更新的標準 ES6+ 以上的修正，還是讓人恨得拳頭癢癢、無法輕易掌握。可是大家還是那麼需要它，甚至將更加需要 —— 不只是前端，看看 Node.js 如何攻佔後端與物聯網、React Native 發展行動端、從 Electron 開始的電腦桌面應用程式 desktop App ……。

![](https://miro.medium.com/max/1400/1*6UmMz77Ks_72mrqKbaXgoQ.jpeg)

source: http://getfreetutorial.com/udemy-full-javascript-es6-tutorial-including-es7-react/

[在 2016 年学 JavaScript 是一种什么样的体验？ — 知乎专現在2017，ES8 又來囉！不暈頭才怪呢zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/22782487)

# Javascript 這個討厭鬼！

視覺設計與英文翻譯出身，我學習 Javascript 是研究所的事。了解各種 Javascript 的原理真的頗痛苦，上課還要考試（昏）。雖然，在一年的課程中，甚至還學到了基本的 JS 後端與資料庫 NoSQL： Node.js、mongodb，但是，我不但沒有接觸框架，而且一直到上了線上課程，在做中學中更了解接資料的 Ajax、事件 (Events)，並學了漂在 Javascript 世界的函式庫（註二）寶箱 jQuery 甚至一點新興的前端框架 Vue，才開始對學 Javascript 這語言有了一絲絲信心跟手感。

![](https://miro.medium.com/max/1400/1*_RzQVKZoS5DDPsp027Hvcw.png)

source : http://www.javascripttutorial.net

不過，很可惜的，這樣並不夠啊。對於 Javascript 這門語言的基本原理、文法雖有了解、看得懂程式碼，經過「所見即所得」的線上課程也真正實作了網頁邏輯 html/樣式 css /互動與資料處理 jQuery，但總覺得自己對 Javascript 的了解十分皮毛。常常看到別人的前端程式碼，即使不用 ES6+、不套框架，甚至變數命名跟程式碼可讀性低，但卻能寫出優美正確的邏輯，看了好生羨慕。

# 寫完歡樂的 HTML、CSS 之後，就要學 JQuery ?

[技术 - javascript学习顺序：先系统学习jQuery再学习基本JavaScript是否会相对快捷？为什么？ - SegmentFault个人情况： 半年前端学习积累： html，css基本熟练 javascript能看懂，会写简单的轮播图代码。会改大部分的js特效。 问题背景： 想要利用暑假两个月的时间系统学习javascript，目的是熟练打好js基础。咨询老师，...segmentfault.com](https://segmentfault.com/q/1010000000579646)

關於程式的原理也懂了、實作也嘗試了，然而無論是實作框架或者讀文件，總有一種生疏感，到底該怎麼辦呢？這時我就想到，關於  **「jQuery 跟 Javascript 誰該先學」** 可說是場大戰。JQuery 作為 Javascript 的函式庫，利用了如網站樣式語言 css 般所見即所得的特性，因此很多人贊同，jQuery 是個適合新手從 Html、Css 等很難真正寫錯（除非你又忘了加分號的那種語法錯誤 (syntax error)！那種該打屁屁）—— 所謂的寫錯不是指效果出不來，而是程式直接壞掉那種 —— 跟文章ㄧ樣的文本語言 (script languages)。好像只要看個線上互動課程 codecademy，死背著

> $(“放個名稱 (id) 或類類 (class)” ).on ( “事件，例如按下去click 之類的”, function(傳送進去東西){ 放一些有的沒的功能在這裡 ; });

就好了。但事實上，很多人從 jQuery 走到 Javascript 就卡關了。支持先學 Javascript 的那一派説，沒有對那種 Functional 的程式語言有所了解 ，又要如何從 html, css, jQuery 的思維跨越到那種「真正」的程式語言呢？但這知易行難呀！即使，像我一開始就碰 Javascript，卻被相關原理弄得暈頭轉向，感覺東缺西缺。

> 關於學習，#講個秘訣

上了 Kuro 老師的課，就像是跟著高超的馴獸師，一起馴服了一匹有著高度潛能、卻頑劣不能敵的悍馬。前幾堂課，Kuro 老師耐心教著 jQuery，用那種 Html, css 所見所得的方式教著，讓我們在做的時候有手感，同時偷渡一些 Javascript 的基本語法進來。這階段並不稀奇，跟我照線上課程實作差不多。

但到了第三堂課，奇妙的事情發生了。「你懂了 jQuery 用法、你會了 Javascript 基本語法，盎！DOM (Document Object Model，文件物件模型)。」「什麼？我沒看清楚，再一遍？」到底發生了什麼事呢？

[HTML DOM 到底是什麼 ？在網頁中，HTML 存放網頁的內容與架構，CSS 標記內容的呈現樣式； 而 JavaScript 則用來產生豐富的互動效果或應用程式。 之前筆記分享過，為什麼要使用HTML5, HTML5更加語義化，...ithelp.ithome.com.tw](http://ithelp.ithome.com.tw/articles/10108783)

說到這裡，想聊聊無論是學校課堂或線上課程，自己常常會陷入一種「背就對了」、「做就對了」的心態。也許是資訊領域門檻高，教學者不是變成 **「反正我是講給工程師聽的、有心懂的人自然會懂」** 的方式在教學，導致不懂的人還是不懂；就是教得太簡單，或是邏輯不是這麼「攻城獅」，反而沒有辦法真正上場實戰。但是在這個資源俯首即是的時代，那些有心懂的人，其實根本就不需要被教 —— 他們早就聽慣了術語，知道如何查找資料，也許只是要個理由做專案罷了。那我們這種不上不下的傢伙，又該如何是好？

真正的差異，在於對學習的「後設心態 」。後設（元認知）的意思是「跳出原本的假設」（註三）。練習與背誦固然重要，但那種對「蛤，為什麼？」的熱情，是無法抹滅且讓人興奮的。 Kuro 老師的『Pen Pinapple ApplePen 魔法』就在於先前細心講解 jQuery 以及 Javascript 每個細節的實際意義，配合現場實作跟回家真的讓人要「想一陣子」、不是那麼好完成的作業，這些細節當下看似瑣碎、實作看似太難，但連貫在一起，好像就鋪出了一條從不會寫程式到會寫程式的康莊大道 🌟（至少讓你進入新手蜜月期 XD）。

![](https://miro.medium.com/max/1400/1*LGlfY-c_38_52SztitOelA.png)

Designed by Tsou Po-Hsuan

（補：接軌的意思不代表能直接就業，而是對業界需求反應快，比起學校與預錄的線上課程更能跟上時代，想補充也能以工作坊形式直接實現。）

# 半生不熟開智慧

即使之前碰過程式，我也是到這時候，才真正體驗一遍「懂」的感覺。不知道是工作坊式的教學，抑或是 Kuro 老師精妙的課程安排，在學校學 Javascript 一知半解、所見所得學 jQuery，直到 **「究竟是重新碰 Javascript，還是不小心就從 jQuery 跌進了 javascript 的世界」** 的神秘感。 **五倍的龍哥 *(寶石鑑定商、永遠的 18 歲) *曾說：「如果一個程式語言不能讓你改變思維，那就不要學了。」** 一個讓我們敢於自問「為什麼？」的老師，讓你不只從看程式悶著寫、讀理論文法的老師，融會貫通的首選 —— 我推薦 Kuro。

他也讓我重拾了對 Javascript 的熱情。

**「我敬仰學習，因為學習是最基礎卻重要的靈感，不是為了工作，學習是我們的本能。
想學習的意志、想學習的渴望，是世間最偉大的靈感。…….
重點不是你學了多少，而是你用學習榮耀自己，你必須融會貫通、感知你學習的本能，並將它融入你的工作與創造。
那，就是你所能達致的最佳狀態。」**

**《靜謐與光明》建築大師路易・康**

[《靜謐與光明》建築大師路易・康自行翻譯www.facebook.com](https://www.facebook.com/photo.php?fbid=10150385620148559&set=a.10150385617863559.372540.551278558&type=3&theater)

（註一）分別以函式化的 Java 與 C 所寫成。
（註二）大致上就是別人幫你寫好的程式，可拿來當工具使用。
