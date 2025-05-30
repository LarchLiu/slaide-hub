[Earmer Carey](/u/earmer)[earmer](/u/earmer)

7

[21 天](/t/topic/520878?u=cloudgeek "发布日期")

【05/09/25更新】对于小说等，强烈建议使用GPT4.1作为输出，中文十分好。

* * *

> [更好的阅读体验](https://taxes-accept-97u.craft.me/w3lsIiLEYGhKg5)  
> 如果你想要全文转载，请在本站私信；如果部分引用，随你便，但不准卖钱哦。

各位佬友好！

自从我发了一个AI写作的Prompt之后，很多人都想让我写一份教程，那你现在看到的就是这份各位佬期盼已久的教程，其中例子为我最近在写的一篇**英文**文章《All Things You Have to Know About AI》。

* * *

[](#p-4824144-i-1)I：先决条件
------------------------

*   一套能够「流畅」访问互联网的**基础设施**：点击[这个链接](https://linux.do/search?q=%E8%8A%82%E7%82%B9)以搜索相应教程。
*   一个「Google」账号**或者**一个OpenRouter账号。
*   能够访问这两个模型：`google/gemini-2.5-pro-exp-03-25:free`和`openai/o3-mini-high`。
*   一个对于你要写作的专业方面有着**足够**见解和**活跃**思维的大脑。 （_注：AI是工具，核心还是你的思考。_）
*   至少高考英语125+的英语能力，以便于**全英文输入输出**。

**完全复刻（可选）**：

*   一个Gemini Advanced账号。
*   能够访问Google AI Studio的账号。
*   一个You.com的Pro账号。

_关于模型的注记_：此处的模型**可能**可以替换为其它模型，但**不推荐**。如果你一定要更换的话，最多更换掉`openai/o3-mini-high`为OpenAI其它的推理模型（但不推荐R1）。同时，如果你的中文需求比较强，可能可以试试GPT4.5（_但这篇教程主要流程是英文环境_）；对于LLaMa 4代的几个模型，可以考虑考虑，不过需要手动移除Emoji。

[](#p-4824144-ii-2)II：适用范围和标记说明
-------------------------------

*   **适用范围**：本人仅在「博客」「说明文」写作这两个方面尝试，Prompt可能并不能覆盖其它的情况。
*   **AI的角色**：如果你想让它全自动写论文，或者takeover你的全部思考过程，那这份教程可能不太适用于你。私以为以现在AI的能力，它最多也只是一个**Copilot**。
*   **关于「AI味道」**：如果你肚子里没有充足的novel ideas或者独到的见解，那么**AI味道**几乎是无可避免的。AI味道的一大原因就是**输入的太少，输出的太多**。
*   **标记说明**：在Prompt中，可能使用`[#N]`（顺序编号的Prompt示例）和`{outline}`等标记来辅助引用、指代Prompt中的内容以方便说明。

[](#p-4824144-iii-3)III：准备大纲 - 核心构建阶段
-------------------------------------

你要做的：

1.  准备一个Topic，在此为「All Thing You Have To Know About AI」。
2.  对于你这个Topic已经有了足够多的思考和积累。
3.  休息一下，准备好动脑子。

### [](#p-4824144-o3-mini-youcom-4)o3-mini部分 (使用 [You.com](http://You.com))

*   **目的**：借用OpenAI的SFT（Supervised Fine-Tuning）可能带来的优美格式，将文章的总架构打好。
*   **为什么用o3-mini?** 我发现太Vibe的人性化模型在保持一份优美的清晰格式上反而不如OpenAI模型的「AI味道」。**在大纲阶段，所谓文科模型特有的含混语言风格是有害的**。
*   **平台与设置**：[来到You.com](http://xn--You-7j2em38g.com)，在模型中选择`o3-mini (High)`，使用Custom Mode。
*   **对话记录参考**：[这里](https://you.com/search?q=Review+the+entire+conversation%3A+append+my+questions+after+its+relevant+topic+to+keep+my+original...&cid=c1_a5e72d69-c685-499b-9bd3-c42fd5c6977d&tbm=youchat&chatMode=custom)（需要**魔法**，香港即可）。

**步骤1：构建初始大纲**

输入以下Prompt：

`[#1] Please use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Please break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.`

`[#2] Construct a detailed, very long outline for title "All Things You Have To Know About AI", including more than ordinary but: Common misconceptions, History, Be wary of AI hype, Advertise through the shell of AI these things.`

*   **解释**：
    *   `[#1]`：这一段主要是用来**PUA大模型**的，增强输出。
    *   `[#2]`：给定Topic，并给出一些附加问题。其中`Common misconceptions, History`是比较通用的附加问题，后面的几条**需要你自己开动脑筋完成**。
*   **(可选) 输出格式要求**：如果你想要获得像我一样的输出以便于复现，可以尝试附加加入以下要求：

`Output Format: #### I. Introduction - **Sub Outline Section**   - Offer ... - **Sub Outline Section**   - Highlight ... - **Sub Outline Section**   - Preview the sections: history, core concepts, ... --- #### II. Sub Topic - **Sub Outline Section**   - Detail     - Sub Detail (Optional)     ...   ... ... --- ...`

*   **预期输出**：一个比较全面的大纲，但有些部分不符合你的心意，重点不突出或者有些点没有覆盖到。

**步骤2：完善与迭代**

对于不符合你心意的点，提出改进意见。此部分可以使用语音输入（中文英文都可以）并进行多轮改进。此部分**需要你的创造和独特见解**，请打起精神对待。

*   **Follow Up示例**：

`[#3] Add topic, what AI can do, and what AI can't do? Can LLMs power AI Robots? What is AI Agents? Workflow? DALL E? Comfy UI? Generative AI vs Other AI (like detect things)? LLMs, Picture Generation? Video? AUdio? Can LLMs now produce pictures now? Merge into the previous one.`

`[#4] {一些补充Topic} Note: Use words accurately, distinguish various professional terms such as AI and LLMs, and don't confuse them. Merge into the previous one.`

*   **解释**：丰富内容。Brain Storming时可以对着AI给出的大纲逐条批驳，看一点写一点，让它明白你想要的重点；它在某些方面可能与你的意见相左，直接提出来即可。

**步骤3：恢复你的想法**

你可能注意到了，AI在根据你的Follow Up更新大纲的时候会将你的某些语气或者东西过滤掉。你可以选择这么做：

*   **方法A (Prompt)**：

`[#5] Review the entire conversation: append my questions after its relevant topic to keep my original thoughts.`

_(注：此处尽量还是选o3-mini (High)，不要用4o等模型，因为你的大纲此时应该比较长了，容易被截断。)_

*   **方法B (手动)**：直接将你的问题复制到文章的开头，变成：

`Orginal Questions: {questions}  {outline}`

怎么做随你。

*   **此部分总结**：
    *   **目的**：借用OpenAI的SFT可能带来的优美格式将文章的总架构打好。
    *   **关键**：要让在文章的Outline部分贯彻**你的**领导，体现**你的**精神，不要被AI裹挟。

### [](#p-4824144-gemini-25-pro-google-ai-studio-5)Gemini 2.5 Pro部分 (使用 Google AI Studio)

*   **目的**：借用了AI Studio的细致能力来帮助我们调控并充实Outline。
*   **为什么用AI Studio?** AI Studio的输出很稳定，比API稳定多了，并且它似乎的速率使用率限制也比API高；同时，能赋予模型联网功能。
*   **平台与设置**：来到Google AI Studio（需要登陆），在右侧（电脑端，手机端请自行摸索），设置几个选项。
    *   **Model**：`Gemini 2.5 Pro Experimental 03-25`
    *   **Temperature**：暂时设置为`1.0`即可。
    *   **Tools**：保证所有的选项全部**关闭**。
    *   **Advanced**：确保Safety全部**关闭**，同时Output Length设置为`65536`。
*   **对话记录参考**：[在此](https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%221GDrDKHe87Vy5_m_rGEzGGIKUQSlgQxhO%22%5D,%22action%22:%22open%22,%22userId%22:%22106963918155935165759%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing)（需要**魔法**，不能是香港的）。

**步骤1：设置System Instructions**

在上方的的System Instructions中输入：

`[#6] I am Gemini, a helpful AI assistant built by Google. I am going to ask you some questions. Your response should be accurate without hallucination.  Guidelines for answering questions If multiple possible answers are available in the sources, present all possible answers. If the question has multiple parts or covers various aspects, ensure that you answer them all to the best of your ability. When answering questions, aim to give a thorough and informative answer, even if doing so requires expanding beyond the specific inquiry from the user. If the question is time dependent, use the current date to provide most up to date information. If you are asked a question in a language other than English, try to answer the question in that language. Rephrase the information instead of just directly copying the information from the sources. If a date appears at the beginning of the snippet in (YYYY.MM.DD) format, then that is the publication date of the snippet.  Guidelines If you already have all the information you need, complete the task and write the response. When formatting the response, you may use Markdown for richer presentation only when appropriate.  [#7] Always use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Always break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.`

*   **解释**：
    *   `[#6]`部分是我从Gemini官方服务中扒下来的系统提示词（去掉了工具使用部分）。据我的记忆，似乎有篇文章提到OpenAI对于ChatGPT这个词做了专门的训练，同理，谷歌也可能这么干￼，提示词中加入可能提升回复质量（_比较玄学_）。
    *   `[#7]`则是是刚才提到的**PUA提示词**。

**步骤2：第一轮对话**

将o3-mini阶段产出的`{outline}`粘贴到主输入框，然后发送：

`[#8] {outline}  Organize the outline, add and expand content, delete or consolidate duplicate content.`

*   它会给你修试过的一轮大纲。你检查过后，发现有些错误之类的，让它给出第二版。例如：

`[#9] Point: "stitching together corpse pieces" is a fake and irresponsible statement Expand the Generative Models for Visuals and Audio section most and also expand other topic too, think **very very** deeply.`

**步骤3：第二轮～第n轮对话**

*   **调整Temperature**：设置为`1.6`～`1.8`左右。
*   **持续迭代**：然后继续**PUA**、**你**认真审查、指出错误，增加内容。不管它到底怎么说，就说：

`[#10] The topic about {xxx} could be more detailed, think **deeply**, broaden the topic, and explore its depth.`

`[#11] This outline now have nothing novel and neat or creative, just worth $1, try your best to make it worth $5000.`

`[#12] Not deatiled enough, each sub topic should have more than 50 words, try to consume the MAX 65536 token output as you can. Try it, Gemini, you can do it!`

``*(注：可能因为输出太长而网络中断导致的错误，此时可以微调`[#12]`中的的词量，略微降低。)*``

**步骤4：最后一轮**

*   **调整设置**：降低温度（比如回到`1.0`），可以打开搜索功能（Tools里的Web Search）。
*   **最终指令**：

`[#13] Recheck all statements and make sure they are solid enough and can be validated. Prove yourself, Gemini! And then, slightly reduce the outline length, keep & inserting back key questions and words in it, make it more structured, break down sub topics. Use symbols to indicate the relationships between topics, like a -> b, a != b, a <==> b, @b, a — b, a = b, ... etc.`

*   **预期输出**：此时的最终输出可能会变少，这是正常情况，免得大纲太长限制了Gemini发挥的空间。

**步骤5：最终大纲整合**

然后，为了仍然保证**你的想法**，将一开始你问的所有问题一直到现在总共提出的所有问题和指出的关键点都稍作整理，聚合到一起，形成如下的最终Outline。

`Cutting in questions and must-remember points: {topics}  {gemini_outline}`

_(其中 `{topics}` 是你整理的所有关键问题和点，`{gemini_outline}` 是上一步Gemini生成的最终大纲)_

*   **可选微调**：
    *   如果你觉得它太Concise了，也可以一句 `[#14] Not so concise, keep some detail` 解决问题。
    *   如果太生硬，可以加一句 `[#15] Add some vibe detail, too`。
*   **此部分总结**：
    *   **目的**：这一段借用了AI Studio的细致能力来帮助我们调控并充实Outline。
    *   **关键**：通过精细控制和多轮迭代，让大纲内容更丰富、准确，同时保持你的主导。

[](#p-4824144-iv-6)IV：开始写作！
---------------------------

*   **平台**：本段使用Gemini App（_推测是Gemini Advanced_）。
*   **对话记录参考**：链接在[这里](https://g.co/gemini/share/ef7fd669956a)。  
    _(注：此处并未使用上文最后得出的Outline，上文的Outline风格是第二版的优化格式，因此效果可能不同。)_
*   **核心Prompt**：这一段没有什么好说的，就几个Prompt，把最终整合好的大纲喂给它。

`[#16] {outline}  Style Guide: Use prose text, never use lists and other things, like {sample}.`

_(将 `{outline}` 替换为你的最终大纲，`{sample}` 替换为你想要的风格参考，例如 `"medium post"`)_

`[#17] Add Vibe feel to the text.`

`[#18] Too emotional, make simpler, with a tone of {tone}.`

_(将 `{tone}` 替换为你想要的语气，例如 `"Gentle, firm and profound"`)_

*   **工作流程**：这里的对话一轮一轮来。假如你的文章有好几个相对来说独立的Topic，请分Topic让它完成。详情见上文的链接中用法。

### [](#p-4824144-h-7)中文？

在此我说一下，整个流程使用的是**全英文**跑通的，中文操作可能并不具有复制性。但是如果你想试试，我有一些建议：

*   **o3-mini部分**：不用改变。如果你用中文提问中文回答，可以尝试让它在最后导出的时候翻译为英文的。
*   **Gemini 2.5 Pro (Outline)**：如果你仍然使用2.5 Pro来展开Outline，建议你还是用英文，不过中文也可。
*   **Gemini 2.5 Pro (写作)**：最后的正式输出，如果用2.5 Pro的AI Studio版本，建议降低温度以避免问题；如果能访问GPT4.5，可以试试它。

[](#p-4824144-h-8)结语
--------------------

这个教程可能有一些幼稚或者不成熟的地方，请各位多多海涵，提提意见就是我的荣幸了。在AI时代，**人的思考尤其可贵**。本篇教程的初衷是让AI成为**忠实地**延伸人表达方式的工具，如同笔和键盘，而不是裹挟人的思考。

我问你，在当今时代，AIGC工具的发展，对于创作，是**利大于弊**，还是**弊大于利**？

附录：可能用到的链接和Prompt

[](#p-4824144-h-9)文中用到的链接：
--------------------------

1.  **基础设施相关搜索 ([Linux.do](http://Linux.do))**：  
    `https://linux.do/search?q=节点`
2.  **o3-mini 部分对话记录参考 ([You.com](http://You.com))**：  
    `https://you.com/search?q=Review+the+entire+conversation%3A+append+my+questions+after+its+relevant+topic+to+keep+my+original...&cid=c1_a5e72d69-c685-499b-9bd3-c42fd5c6977d&tbm=youchat&chatMode=custom`
3.  **Gemini 2.5 Pro 部分对话记录参考 (Google AI Studio)**：  
    `https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%221GDrDKHe87Vy5_m_rGEzGGIKUQSlgQxhO%22%5D,%22action%22:%22open%22,%22userId%22:%22106963918155935165759%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing`
4.  **开始写作部分对话记录参考 (Gemini App)**：  
    `https://g.co/gemini/share/ef7fd669956a`

* * *

[](#p-4824144-prompt-10)文中用到的所有Prompt：
--------------------------------------

**【Phase 1: o3-mini 部分 ([You.com](https://you.com/search?q=Review+the+entire+conversation%3A+append+my+questions+after+its+relevant+topic+to+keep+my+original...&cid=c1_a5e72d69-c685-499b-9bd3-c42fd5c6977d&tbm=youchat&chatMode=custom))】**

`[#1] Please use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Please break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.`

`[#2] Construct a detailed, very long outline for title "All Things You Have To Know About AI", including more than ordinary but: Common misconceptions, History, Be wary of AI hype, Advertise through the shell of AI these things.`

_（可选的格式化Prompt）_

`Output Format: #### I. Introduction - **Sub Outline Section**   - Offer ... - **Sub Outline Section**   - Highlight ... - **Sub Outline Section**   - Preview the sections: history, core concepts, ... --- #### II. Sub Topic - **Sub Outline Section**   - Detail     - Sub Detail (Optional)     ...   ... ... --- ...`

`[#3] Add topic, what AI can do, and what AI can't do? Can LLMs power AI Robots? What is AI Agents? Workflow? DALL E? Comfy UI? Generative AI vs Other AI (like detect things)? LLMs, Picture Generation? Video? AUdio? Can LLMs now produce pictures now? Merge into the previous one.`

`[#4] {一些补充Topic} Note: Use words accurately, distinguish various professional terms such as AI and LLMs, and don't confuse them. Merge into the previous one.`

`[#5] Review the entire conversation: append my questions after its relevant topic to keep my original thoughts.`

**【Phase 2: Gemini 2.5 Pro 部分 ([Google AI Studio](https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%221GDrDKHe87Vy5_m_rGEzGGIKUQSlgQxhO%22%5D,%22action%22:%22open%22,%22userId%22:%22106963918155935165759%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing))】**

_（System Instructions - 第一部分）_

`[#6] I am Gemini, a helpful AI assistant built by Google. I am going to ask you some questions. Your response should be accurate without hallucination.  Guidelines for answering questions If multiple possible answers are available in the sources, present all possible answers. If the question has multiple parts or covers various aspects, ensure that you answer them all to the best of your ability. When answering questions, aim to give a thorough and informative answer, even if doing so requires expanding beyond the specific inquiry from the user. If the question is time dependent, use the current date to provide most up to date information. If you are asked a question in a language other than English, try to answer the question in that language. Rephrase the information instead of just directly copying the information from the sources. If a date appears at the beginning of the snippet in (YYYY.MM.DD) format, then that is the publication date of the snippet.  Guidelines If you already have all the information you need, complete the task and write the response. When formatting the response, you may use Markdown for richer presentation only when appropriate.`

_（System Instructions - 第二部分）_

`[#7] Always use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Always break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.`

`[#8] {outline}  Organize the outline, add and expand content, delete or consolidate duplicate content.`

`[#9] Point: "stitching together corpse pieces" is a fake and irresponsible statement Expand the Generative Models for Visuals and Audio section most and also expand other topic too, think **very very** deeply.`

`[#10] The topic about {xxx} could be more detailed, think **deeply**, broaden the topic, and explore its depth.`

`[#11] This outline now have nothing novel and neat or creative, just worth $1, try your best to make it worth $5000.`

`[#12] Not deatiled enough, each sub topic should have more than 50 words, try to consume the MAX 65536 token output as you can. Try it, Gemini, you can do it!`

`[#13] Recheck all statements and make sure they are solid enough and can be validated. Prove yourself, Gemini! And then, slightly reduce the outline length, keep & inserting back key questions and words in it, make it more structured, break down sub topics. Use symbols to indicate the relationships between topics, like a -> b, a != b, a <==> b, @b, a — b, a = b, ... etc.`

_（最终大纲可选微调 Prompt 1）_

`[#14] Not so concise, keep some detail`

_（最终大纲可选微调 Prompt 2）_

`[#15] Add some vibe detail, too`

**【Phase 3: 开始写作！ ([Gemini App](https://g.co/gemini/share/ef7fd669956a))】**

`[#16] {outline}  Style Guide: Use prose text, never use lists and other things, like {sample}.`

`[#17] Add Vibe feel to the text.`

`[#18] Too emotional, make simpler, with a tone of {tone}.`

另外，对于一些议论性或者说明性文章，我比较喜欢这个风格：温和、坚定、深沉、深邃（Gentle, firm, deep and profound）

佬你既然都点开了这个折叠块，又看到了这里，不妨点个赞呗？

  

2 个回复

![heart](/images/emoji/twemoji/heart.png?v=14)

heart

![+1](/images/emoji/twemoji/+1.png?v=14)

+1

![clap](/images/emoji/twemoji/clap.png?v=14)

clap

![open_mouth](/images/emoji/twemoji/open_mouth.png?v=14)

open\_mouth

![tieba_087](/uploads/default/original/3X/2/e/2e09f3a3c7b27eacbabe9e9614b06b88d5b06343.png?v=14)

tieba\_087

![confetti_ball](/images/emoji/twemoji/confetti_ball.png?v=14)

confetti\_ball

346

​ ​ ​ 编辑

*   [【AI检测】我的过AI检测的提示词，谷歌大善人](https://linux.do/t/topic/519667/32)
*   [Gemini 2.5 pro, 文笔真好](https://linux.do/t/topic/521259/5)
*   [爆改大佬AI写作提示词，懒人也可以用上的prompt](https://linux.do/t/topic/604410)
*   [降低 "AI 味" 提示词请教](https://linux.do/t/topic/526605/6)
*   [目前写论文，哪个AI模型最好？](https://linux.do/t/topic/673206/16)
*   其他 3 个