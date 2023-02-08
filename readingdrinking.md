## 1.安全世界观
----
----
对于现代计算机系统来说：
- 用户态的最高权限是root（administrator）
- 黑客使用的漏洞利用代码，称为“exploit”
- 互联网安全的核心问题是数据安全问题。
----
### 1.1安全的本质

>安全问题的本质是信任问题。

- 数据从高等级的信任域流向低等级的信任域，是不需要经过安全检查的，反之则需要。
- 安全是一个持续的过程，没有银弹。
---
### 1.2安全三要素
- 机密性（**C**onfidentiality）
- 完整性（**I**ntegrity）
- 可用性（**A**vailability）

|要素|机密性|完整性|可用性|
|---|---|---|---|
|内容|要求保护数据内容不能泄露|要求保护数据内容是完整、没有被篡改的|要求保护资源是“随需而得”的|
|常见手段|加密|数字签名|...|

以上是最基本三要素，后面还有扩充的**可审计性**、**不可抵赖性** 

----

### 1.3安全评估
:one:资产等级划分:arrow_right: :two:威胁分析:arrow_right: :three:风险分析:arrow_right: :four:确认解决方案

|step|资产等级划分|威胁分析|风险分析|确认解决方案|
|---|---|---|---|---|
|作用|所有工作的基础，明确目标是什么，要保护什么|把所有的威胁都找出来|衡量一个威胁能造成的危害|...|

---
#### 1.3.1威胁分析相关
>在安全领域里
>>威胁（Threat）：可能造成危害的来源。
>>风险(Risk)：可能会出现的损失。

微软提出一种威胁建模方法，<a href="https://img-blog.csdnimg.cn/20201205172119956.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzQ2NTgzMDgx,size_16,color_FFFFFF,t_70">STRIDE模型</a>
<br>
<a href=http://www.uml.org.cn/modeler/202104202.asp>几种威胁建模</a>

<font size=1><font color=red>一旦这个信任基础不存在了，所有的安全方案都将化为浮云。</font></font>

----
#### 1.3.2风险分析相关
|组成风险的因素|
|---|
|**Risk** = **Probability** x **Damage Poten** - **tial**|

一个例子：<a href="https://img-blog.csdnimg.cn/20201206095806356.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzQ2NTgzMDgx,size_16,color_FFFFFF,t_70">DREAD模型</a>

----
#### 1.3.3设计安全方案相关
>基本原则
>>**Secure By Default**: <br>（1）白名单和黑名单的思想。<br>（2）最小权限原则（安全设计基本原则之一）<br>
>>**Defense in Depth**： <br>（1）在不同层面，不同方面实施安全方案，避免疏漏，不同安全方案之间需要相互配合，构成一个整体。<br>（2）要在正确的地方做正确的事。在解决根本问题的地方实施针对性的安全方案。<br>
>>**数据与代码分离原则**： <br>是从漏洞成因上看问题，广泛适用于各种由于''注入''而引发的安全问题场景。XSS、SQL Injection...<br>
>>**不可预测性原则**： <br>从克服攻击方法的角度看问题<br>有效对抗基于篡改、伪造的攻击，如微软使用的<a href="https://blog.csdn.net/CSNN2019/article/details/113082616">ASLR技术</a><br>其实现往往需要用到**加密算法**、**随机数算法**、**哈希算法**。

<font color=red>对于一个复杂的系统而言，Denfense in Depth是构建安全体系的必要选择</font>