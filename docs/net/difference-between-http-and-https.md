# http://和 https://

的区别

> 原文:[https://www . geesforgeks . org/http-和-https 之间的区别/](https://www.geeksforgeeks.org/difference-between-http-and-https/)

在浏览器的地址栏中，你在浏览网站的时候有没有注意到 *http://* 或者 *https://* ？如果这两个都不存在，那么最有可能的是 *http://* 让我们找出区别…

简而言之，这两种协议都是在网络服务器和网络浏览器之间交换特定网站信息的协议。但是这两者有什么区别呢？额外的 ***s*** 存在于 *https* 中，这使得它变得安全！有什么不同🙂 *http* 和 *https* 的一个非常简洁的区别就是 *https* 比 *http* 安全多了。

让我们多挖一点。
**H**yper**T**ext**T**transfer**P**rotocol(HTTP 是一种通过网络传输超文本的协议。由于其简单性， *http* 已经成为网络上最广泛使用的数据传输协议，但是使用 *http* 交换的数据(即超文本)并不像我们希望的那样安全。事实上，使用 *http* 交换的超文本是纯文本的，也就是说，浏览器和服务器之间的任何人都可以相对容易地阅读它，如果一个人截获了这种数据交换。但是为什么我们需要网络安全呢？想想在亚马逊或 Flipkart 的“网上购物”。你可能已经注意到，只要我们点击这些在线购物门户网站上的结账，地址栏就会被更改为使用 *https* 。这样做是为了随后的数据传输(即金融交易等)。)是安全的。这就是为什么*引入 https* 以便首先在服务器和浏览器之间建立安全会话。事实上，SSL 和/或 TLS 等密码协议将 *http* 变成了 *https* 即**https**=**http**+**密码协议**。此外，为了在 *https* 中实现这种安全性，使用公钥基础设施(PKI)，因为公钥可以由几个网络浏览器使用，而私钥可以由该特定网站的网络服务器使用。这些公钥的分发是通过由浏览器维护的证书来完成的。您可以在浏览器设置中检查这些证书。我们将在另一篇文章中详细介绍这个设置安全会话的过程。

此外， *http* 和 *https* 的另一个句法差异是 *http* 使用默认端口 80，而 *https* 使用默认端口 443。但需要注意的是， *https* 中的这种安全性是以处理时间为代价实现的，因为 Web Server 和 Web Browser 需要使用 Certificates 交换加密密钥才能传输实际数据。基本上，安全会话的建立是在服务器和浏览器之间的实际超文本交换之前完成的。

【HTTP 和 HTTPS 的区别

*   在 HTTP 中，URL 以“http://”开头，而 URL 以“https://”开头
*   HTTP 使用端口号 80 进行通信，HTTPS 使用 443
*   HTTP 被认为是不安全的，HTTPS 是安全的
*   HTTP 在应用层工作，HTTPS 在传输层工作
*   如上所述，在 HTTP 中，加密是不存在的，而加密在 HTTPS 是存在的
*   HTTP 不需要任何证书，HTTPS 需要 SSL 证书