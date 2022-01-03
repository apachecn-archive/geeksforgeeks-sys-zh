# 无线安全|第 2 部分

> 原文:[https://www.geeksforgeeks.org/wireless-security-part-2/](https://www.geeksforgeeks.org/wireless-security-part-2/)

先决条件–[无线安全|设置 1](https://www.geeksforgeeks.org/wireless-security-set-1/)
四种类型的可扩展身份验证协议(EAP)身份验证方法是–

```
1. LEAP
2. EAP-FAST
3. PEAP
4. EAP-TLS 
```

这些解释如下。

1.  **轻量级可扩展认证协议(LEAP)–**
    为了消除 WEP 的弱点，CISCO 推出了一种专有的无线认证方法，称为 LEAP。要进行身份验证，客户端必须提供用户名和密码凭据，然后客户端和接入点交换加密的质询短语。如果加密的质询短语匹配，则向客户端提供访问权限。LEAP 使用动态密钥来加密短语，不像 WEP 使用静态密钥。但是后来发现它容易受到攻击，所以 LEAP 从此就被弃用了。现在虽然无线设备可能提供 LEAP，但你不应该使用它。
2.  **EAP-FAST –**
    Further CISCO introduced a more secure method than LEAP called EAP Flexible Authentication with secure Tunneling (EAP-FAST). In this method authentication credentials are secured by passing a protected access credential (PAC) between AS and client. PAC is a sort of shared secret generated by Authentication server, used for mutual authentication.
    It is series of three phases.
    *   **阶段-1:**
        PAC 在客户端生成并安装。
    *   **阶段 2:**
        在相互认证后，客户端和认证服务器协商传输层安全(TLS)隧道。
    *   **阶段-3:**
        为了增加安全性，客户端随后通过 TLS 隧道进行身份验证。

    值得注意的是，这里有两个独立的身份验证过程。一个在 AS 和客户端之间，称为外部身份验证，另一个与终端用户之间，称为内部身份验证。它们都以嵌套的方式出现。TLS 隧道外的外部认证和 TLS 隧道内的内部认证。

3.  **受保护的 EAP(PEAP)–**
    PEAP 是对 EAP-FAST 的进一步改进。它还使用外部和内部身份验证。该方法的附加步骤是数字证书。在外部认证中，认证服务器向客户端提供数字证书(DC)，如果客户端对 DC 满意，则为内部认证构建一个 TLS 隧道。DC 由识别所有者标准格式的数据组成。它由称为证书颁发机构的第三方验证。客户端和身份验证服务器都知道并信任证书颁发机构。
4.  **EAP-TLS–**
    通过 EAP-TLS 进一步完善了 PEAP。其中，数字证书安装在 AS 和客户端上。它们都相互交换证书，然后建立 TLS 隧道来交换加密密钥材料。EAP-TLS 被认为是最安全的，但是实现起来有点复杂。在数百个客户端上手动安装数字证书是不切实际的。公钥基础设施(PKI)用于向客户端安全地提供证书，并在客户端或用户不再能够访问网络时撤销证书。EAP-TLS 仅在无线客户端可以接受和使用证书时使用。