---
page: 1
theme: seriph
background: https://cover.sli.dev
title: "AI写作教程：从大纲到初稿"
titleTemplate: '%s - Slaide'
layout: cover
presenter: dev
seoMeta:
  ogTitle: "AI写作教程：从大纲到初稿"
addons:
  - slidev-theme-viplay
subtitlesConfig:
  noTTSDelay: 2000
  ttsApi: "https://edgetts.deno.dev/v1/audio/speech"
  ttsLangName:
    en: "English(US)"
    zh_CN: "中文(简体)"
  apiCustom:
    voice: 'rate:-0.2|pitch:0.1'
  ttsModel:
    zh_CN:
      - value: "zh-CN-YunjianNeural"
        display: "云间"
      - value: "zh-CN-XiaoxiaoNeural"
        display: "晓晓"
    en:
      - value: "en-US-AndrewNeural"
        display: "Andrew"
      - value: "en-US-AriaNeural"
        display: "Aria"
subtitles: {"default":{"zh_CN":["哈喽，各位朋友！","很高兴在这里跟大家分享一个我摸索出来的AI写作教程。","特别是写博客或者说明文，我觉得这套方法挺管用。","我会把自己当作这篇教程的创作者，来跟大家聊聊。"],"en":["Hello everyone, and welcome!","I'm excited to share an AI writing tutorial that I've developed.","I find this method particularly effective for writing blog posts or explanatory articles.","I'll walk you through it as if I were the creator of this tutorial."]}}
---

# AI写作教程：从大纲到初稿

## 基于AI工具的博客/说明文写作流程

<div class="text-sm">
分享人：[Earmer Carey](/u/earmer)
</div>

---
page: 2
layout: image-left
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":["首先，咱们得准备点东西。","你需要能顺畅上网的基础设施。","一个Google账号或者OpenRouter账号。","能用到`google/gemini-2.5-pro-exp-03-25`和`openai/o3-mini-high`这两个模型。"],"en":["First, we need to prepare a few things.","You'll need infrastructure that allows smooth internet access.","A Google account or an OpenRouter account.","And access to these two models: `google/gemini-2.5-pro-exp-03-25` and `openai/o3-mini-high`."]}}
---

# I：先决条件

## 基础设施与账号

-   **流畅访问互联网的基础设施**
    -   [搜索相应教程](https://linux.do/search?q=%E8%8A%82%E7%82%B9)
-   **账号需求**
    -   Google账号 或 OpenRouter账号
    -   能够访问以下模型：
        -   `google/gemini-2.5-pro-exp-03-25:free`
        -   `openai/o3-mini-high`

---
page: 3
layout: two-cols
subtitles: {"default":{"zh_CN":["当然，最重要的是，你得有个对写作主题有足够了解、思维活跃的大脑。","AI只是工具，核心思考还是得靠咱们自己。","还有，最好有高考英语125+的水平，因为整个流程是全英文的。","如果你想完全复刻我的环境，可能还需要Gemini Advanced、Google AI Studio和You.com Pro账号。"],"en":["Of course, most importantly, you need a brain with sufficient insight into the writing topic and active thinking.","AI is just a tool; the core thinking still relies on us.","Also, it's best to have an English level equivalent to Gaokao English 125+, as the entire process is in English.","If you want to fully replicate my environment, you might also need Gemini Advanced, Google AI Studio, and You.com Pro accounts."]}}
---

# I：先决条件 (续)

## 核心能力与可选配置

-   **你的大脑**
    -   对写作主题有**足够**见解
    -   **活跃**思维
    -   *AI是工具，核心是你的思考*


::right::

-   **英语能力**
    -   至少高考英语125+
    -   **全英文输入输出**
-   **完全复刻 (可选)**
    -   Gemini Advanced账号
    -   Google AI Studio账号
    -   You.com Pro账号

---
page: 4
layout: two-cols
subtitles: {"default":{"zh_CN":["这些模型不是完全不能替换，但强烈建议按我说的来。","特别是中文写作需求强的，可以试试GPT4.5。","这套方法主要适用于博客和说明文写作。","AI在这里的角色，我定位是'Copilot'，也就是副驾驶。","它不能完全接管你的思考，更不是让你全自动写论文。"],"en":["These models aren't completely irreplaceable, but I strongly recommend sticking to what I suggest.","Especially if you have strong Chinese writing needs, you can try GPT4.5.","This method is mainly suitable for writing blog posts and explanatory articles.","The role of AI here, I define as 'Copilot', or co-pilot.","It cannot completely take over your thinking, much less write papers fully automatically."]}}
---

# I：先决条件 (续)

## 模型选择与适用范围

-   **关于模型替换**
    -   不推荐替换，最多可替换 `openai/o3-mini-high`
    -   中文需求强可试GPT4.5
    -   LLaMa 4代需手动移除Emoji


::right::

-   **适用范围**
    -   博客
    -   说明文
-   **AI的角色**
    -   **Copilot** (副驾驶)
    -   不适用于全自动论文或接管思考

---
page: 5
layout: image-right
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":["说到'AI味道'，如果你自己的原创想法不够多，那确实很难避免。","AI味道重，往往是因为你给AI的输入太少，但让它输出太多。","教程里会用到一些标记，比如`[#N]`表示Prompt示例，`{outline}`表示引用Prompt中的内容。"],"en":["Speaking of 'AI flavor', if you don't have enough original ideas, it's indeed hard to avoid.","A strong AI flavor often comes from giving the AI too little input but asking for too much output.","In the tutorial, I'll use some markers, like `[#N]` for Prompt examples, and `{outline}` for referencing content within a Prompt."]}}
---

# II：适用范围和标记说明

## "AI味道"与标记

-   **关于"AI味道"**
    -   原创想法不足时难以避免
    -   原因：**输入的太少，输出的太多**
-   **标记说明**
    -   `[#N]`: 顺序编号的Prompt示例
    -   `{outline}`: 引用Prompt中的内容

---
page: 6
layout: image-right
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":["好，准备工作就绪，咱们开始构建大纲，这是核心阶段！","第一步，准备好你的主题，比如我写的那篇《All Things You Have To Know About AI》。","确保你对这个主题已经思考和积累了不少东西。","然后，咱们用o3-mini模型来打总体的架构。"],"en":["Okay, preparations are complete. Let's start building the outline, which is the core stage!","Step one, prepare your topic, like the one I wrote, \"All Things You Have To Know About AI\".","Make sure you've thought and accumulated enough on this topic.","Then, we'll use the o3-mini model to structure the overall framework of the article."]}}
---

# III：准备大纲 - 核心构建阶段

## 你的准备

1.  **准备Topic**
    -   例如：《All Things You Have To Know About AI》
2.  **思考与积累**
    -   对Topic有足够多的思考和积累
3.  **准备动脑**
    -   休息一下，准备好

---
page: 7
layout: two-cols
subtitles: {"default":{"zh_CN":["我发现OpenAI的模型在格式上比较清晰，适合用来构建大纲。","咱们来到You.com，选择o3-mini (High)模型，用Custom Mode。"],"en":["I've found that OpenAI's models have a clearer format, which is suitable for building outlines.","We'll go to You.com, select the o3-mini (High) model, and use Custom Mode."]}}
---

# III：准备大纲 (续)

## o3-mini部分 (使用 You.com)

-   **目的**
    -   借用OpenAI SFT带来的优美格式，打好文章总架构
-   **为什么用o3-mini?**


::right::

    -   优美清晰的格式，避免文科模型含混风格
-   **平台与设置**
    -   [You.com](http://You.com)
    -   模型: `o3-mini (High)`
    -   模式: Custom Mode
    -   [对话记录参考](https://you.com/search?q=Review+the+entire+conversation%3A+append+my+questions+after+its+relevant+topic+to+keep+my+original...&cid=c1_a5e72d69-c685-499b-9bd3-c42fd5c6977d&tbm=youchat&chatMode=custom)

---
page: 8
layout: two-cols
subtitles: {"default":{"zh_CN":["你可以用一些Prompt来'激励'模型，让它发挥最大能力，追求深度和创新。","比如像`[#1]`和`[#7]`这样的Prompt，就是用来'PUA'模型的。","接着，用`[#2]`这样的Prompt给出你的文章标题和一些你想包含的附加问题。","这些附加问题，比如常见的误解、历史等等，需要你自己开动脑筋去想。"],"en":["You can use some Prompts to 'motivate' the model, making it use its maximum capability and pursue depth and innovation.","For example, Prompts like `[#1]` and `[#7]` are used to 'PUA' the model.","Next, use a Prompt like `[#2]` to provide your article title and some additional questions you want to include.","These additional questions, such as common misconceptions, history, etc., require you to think them through yourself."]}}
---

# III：准备大纲 (续)

## o3-mini 步骤1：构建初始大纲

**Prompt示例:**

<div class="max-h-48 overflow-y-auto">

```
[#1] Please use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Please break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.
```


::right::


```
[#2] Construct a detailed, very long outline for title "All Things You Have To Know About AI", including more than ordinary but: Common misconceptions, History, Be wary of AI hype, Advertise through the shell of AI these things.
```

</div>

-   **解释**
    -   `[#1]`: PUA大模型，增强输出
    -   `[#2]`: 给定Topic和附加问题 (需自己思考)

---
page: 9
layout: two-cols
subtitles: {"default":{"zh_CN":["你也可以加上格式要求，让输出大纲更符合你的习惯。","第一次输出的大纲可能不完全符合心意，没关系，咱们进入完善和迭代阶段。"],"en":["You can also add format requirements to make the output outline more aligned with your preferences.","The first output outline might not be exactly what you want, but that's okay. We'll move on to the refinement and iteration stage."]}}
---

# III：准备大纲 (续)

## o3-mini 步骤1：构建初始大纲 (续)

**可选输出格式要求:**

<div class="max-h-48 overflow-y-auto">

```
Output Format: #### I. Introduction - **Sub Outline Section**   - Offer ... - **Sub Outline Section**   - Highlight ... - **Sub Outline Section**   - Preview the sections: history, core concepts, ... --- #### II. Sub Topic - **Sub Outline Section**   - Detail     - Sub Detail (Optional)     ...   ... ... --- ...


::right::

```

</div>

-   **解释**
    -   让输出大纲更符合你的习惯
-   **预期输出**
    -   一个比较全面的大纲，但可能不完全符合心意

---
page: 10
layout: two-cols
subtitles: {"default":{"zh_CN":["对着AI大纲提出改进意见，多轮对话。","比如用`[#3]`、`[#4]`这样的Prompt，加入更多你想讨论的具体话题。","要明确告诉AI你想要的重点是什么，它跟你意见不一致的地方也要提出来。"],"en":["Provide feedback on the AI's outline and suggest improvements through multiple rounds of conversation.","For example, use Prompts like `[#3]` and `[#4]` to add more specific topics you want to discuss.","Clearly tell the AI what your focus is, and point out areas where its suggestions differ from yours."]}}
---

# III：准备大纲 (续)

## o3-mini 步骤2：完善与迭代

-   对着AI大纲提出改进意见，多轮对话
-   **Follow Up示例:**

<div class="max-h-48 overflow-y-auto">

```
[#3] Add topic, what AI can do, and what AI can't do? Can LLMs power AI Robots? What is AI Agents? Workflow? DALL E? Comfy UI? Generative AI vs Other AI (like detect things)? LLMs, Picture Generation? Video? AUdio? Can LLMs now produce pictures now? Merge into the previous one.


::right::

```

```
[#4] {一些补充Topic} Note: Use words accurately, distinguish various professional terms such as AI and LLMs, and don't confuse them. Merge into the previous one.
```

</div>

-   **解释**
    -   丰富内容，明确重点，指出分歧

---
page: 11
layout: two-cols
subtitles: {"default":{"zh_CN":["在迭代过程中，AI可能会过滤掉你的一些想法或语气。","你可以用`[#5]`这样的Prompt让它回顾对话，把你的原始想法加回去。","或者你也可以手动整理你的问题和关键点，放到大纲前面。"],"en":["During the iteration process, the AI might filter out some of your ideas or tone.","You can use a Prompt like `[#5]` to ask it to review the conversation and add back your original thoughts.","Alternatively, you can manually organize your questions and key points and place them before the outline."]}}
---

# III：准备大纲 (续)

## o3-mini 步骤3：恢复你的想法

-   AI更新大纲时可能过滤你的想法或语气
-   **方法A (Prompt):**

<div class="max-h-32 overflow-y-auto">

```


::right::

[#5] Review the entire conversation: append my questions after its relevant topic to keep my original thoughts.
```

</div>

-   *注: 尽量用o3-mini (High)，避免大纲过长被截断*
-   **方法B (手动):**
    -   将你的问题复制到文章开头
    -   `Orginal Questions: {questions} {outline}`

---
page: 12
layout: image-right
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":["这个阶段的关键是，大纲必须贯彻你的领导，体现你的精神，别被AI牵着走。"],"en":["The key in this stage is that the outline must reflect *your* leadership and *your* spirit.","Don't let the AI dictate the direction."]}}
---

# III：准备大纲 (续)

## o3-mini 部分总结

-   **目的**
    -   借用OpenAI SFT优美格式，打好文章总架构
-   **关键**
    -   大纲部分要贯彻**你的**领导
    -   体现**你的**精神
    -   不要被AI裹挟

---
page: 13
layout: two-cols
subtitles: {"default":{"zh_CN":["接下来，咱们用Gemini 2.5 Pro来细化和充实大纲。","我用的是Google AI Studio，它的输出比较稳定，而且可以联网。","在AI Studio里设置好模型、温度、工具和输出长度。"],"en":["Next, we'll use Gemini 2.5 Pro to refine and enrich the outline.","I use Google AI Studio because its output is stable and it can access the internet.","In AI Studio, set up the model, temperature, tools, and output length."]}}
---

# III：准备大纲 (续)

## Gemini 2.5 Pro部分 (使用 Google AI Studio)

-   **目的**
    -   借用AI Studio细致能力，调控并充实Outline
-   **为什么用AI Studio?**
    -   输出稳定，速率使用率高


::right::

    -   能赋予模型联网功能
-   **平台与设置**
    -   [Google AI Studio](https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%221GDrDKHe87Vy5_m_rGEzGGIKUQSlgQxhO%22%5D,%22action%22:%22open%22,%22userId%22:%22106963918155935165759%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing)
    -   Model: `Gemini 2.5 Pro Experimental 03-25`
    -   Temperature: 暂时 `1.0`
    -   Tools: 全部**关闭**
    -   Advanced: Safety全部**关闭**, Output Length `65536`

---
page: 14
layout: two-cols
subtitles: {"default":{"zh_CN":["在System Instructions里，可以加入一些官方的系统提示词和咱们的'PUA'提示词。","这些有助于引导模型的行为和输出风格。"],"en":["In System Instructions, you can add some official system prompts and our 'PUA' prompts.","These help guide the model's behavior and output style."]}}
---

# III：准备大纲 (续)

## Gemini 2.5 Pro 步骤1：设置System Instructions

**System Instructions示例:**

<div class="max-h-48 overflow-y-auto">

```
[#6] I am Gemini, a helpful AI assistant built by Google. I am going to ask you some questions. Your response should be accurate without hallucination.  Guidelines for answering questions If multiple possible answers are available in the sources, present all possible answers. If the question has multiple parts or covers various aspects, ensure that you answer them all to the best of your ability. When answering questions, aim to give a thorough and informative answer, even if doing so requires expanding beyond the specific inquiry from the user. If the question is time dependent, use the current date to provide most up to date information. If you are asked a question in a language other than English, try to answer the question in that language. Rephrase the information instead of just directly copying the information from the sources. If a date appears at the beginning of the snippet in (YYYY.MM.DD) format, then that is the publication date of the snippet.  Guidelines If you already have all the information you need, complete the task and write the response. When formatting the response, you may use Markdown for richer presentation only when appropriate.
```


::right::


```
[#7] Always use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Always break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.
```

</div>

-   **解释**
    -   `[#6]`: 官方系统提示词 (玄学提升)
    -   `[#7]`: PUA提示词

---
page: 15
layout: two-cols
subtitles: {"default":{"zh_CN":["然后把o3-mini生成的大纲喂给Gemini，用`[#8]`这样的Prompt让它组织、扩展、删除重复内容。","检查第一轮输出，指出错误，让它给出第二版。","比如用`[#9]`这样的Prompt，指出不准确的地方，并要求它深入思考、扩展内容。"],"en":["Then feed the outline generated by o3-mini to Gemini, using a Prompt like `[#8]` to ask it to organize, expand, and delete duplicate content.","Review the first round of output, point out errors, and request a second version.","For example, use a Prompt like `[#9]` to point out inaccuracies and ask it to think deeply and expand on the content."]}}
---

# III：准备大纲 (续)

## Gemini 2.5 Pro 步骤2：第一轮对话

-   粘贴o3-mini产出的`{outline}`
-   **Prompt示例:**

<div class="max-h-32 overflow-y-auto">

```
[#8] {outline}  Organize the outline, add and expand content, delete or consolidate duplicate content.
```


::right::


</div>

-   检查第一轮输出，指出错误，要求第二版
-   **Follow Up示例:**

<div class="max-h-32 overflow-y-auto">

```
[#9] Point: "stitching together corpse pieces" is a fake and irresponsible statement Expand the Generative Models for Visuals and Audio section most and also expand other topic too, think **very very** deeply.
```

</div>

---
page: 16
layout: two-cols
subtitles: {"default":{"zh_CN":["可以把温度调高一点，比如1.6到1.8，继续迭代。","不断用`[#10]`、`[#11]`、`[#12]`这样的Prompt，要求它更详细、更有创意、消耗更多Token。","即使它说做不到，你也要坚持要求它尝试。"],"en":["You can increase the temperature a bit, for example to 1.6 or 1.8, and continue iterating.","Keep using Prompts like `[#10]`, `[#11]`, and `[#12]`, asking it to be more detailed, creative, and consume more tokens.","Even if it says it can't, you should insist that it try."]}}
---

# III：准备大纲 (续)

## Gemini 2.5 Pro 步骤3：第二轮～第n轮对话

-   **调整Temperature:** `1.6`～`1.8`
-   **持续迭代:** PUA、审查、指出错误、增加内容
-   **迭代Prompt示例:**

<div class="max-h-48 overflow-y-auto">

```
[#10] The topic about {xxx} could be more detailed, think **deeply**, broaden the topic, and explore its depth.


::right::

```

```
[#11] This outline now have nothing novel and neat or creative, just worth $1, try your best to make it worth $5000.
```

```
[#12] Not deatiled enough, each sub topic should have more than 50 words, try to consume the MAX 65536 token output as you can. Try it, Gemini, you can do it!
```

</div>

-   *注: 输出太长可能导致网络中断，可微调词量*

---
page: 17
layout: two-cols
subtitles: {"default":{"zh_CN":["到了最后一轮，把温度调回1.0，可以打开搜索功能。","用`[#13]`这样的Prompt，让它重新检查所有陈述，确保准确性，并稍微精简大纲，加入关键问题和符号。","最终输出的大纲可能会变短，这是正常的，给后续写作留出空间。"],"en":["In the final round, lower the temperature back to 1.0, and you can turn on the search function.","Use a Prompt like `[#13]` to ask it to recheck all statements for accuracy, slightly reduce the outline length, and add back key questions and symbols.","The final output outline might be shorter, which is normal, leaving space for the subsequent writing."]}}
---

# III：准备大纲 (续)

## Gemini 2.5 Pro 步骤4：最后一轮

-   **调整设置:**
    -   降低温度 (例如回到`1.0`)
    -   打开搜索功能 (Tools里的Web Search)
-   **最终指令Prompt:**


::right::


<div class="max-h-48 overflow-y-auto">

```
[#13] Recheck all statements and make sure they are solid enough and can be validated. Prove yourself, Gemini! And then, slightly reduce the outline length, keep & inserting back key questions and words in it, make it more structured, break down sub topics. Use symbols to indicate the relationships between topics, like a -> b, a != b, a <==> b, @b, a — b, a = b, ... etc.
```

</div>

-   **预期输出:** 最终输出可能变少 (正常)

---
page: 18
layout: two-cols
subtitles: {"default":{"zh_CN":["最后一步，把你在整个过程中提出的所有关键问题和点整理好，跟Gemini的最终大纲整合在一起。","形成一个包含你的想法和AI细化内容的最终Outline。","你还可以用`[#14]`或`[#15]`这样的Prompt微调大纲的简洁度或风格。"],"en":["The final step is to organize all the key questions and points you raised throughout the process and integrate them with Gemini's final outline.","This forms a final Outline that includes both your ideas and the AI's refined content.","You can also use Prompts like `[#14]` or `[#15]` to fine-tune the conciseness or style of the outline."]}}
---

# III：准备大纲 (续)

## Gemini 2.5 Pro 步骤5：最终大纲整合

-   整理你提出的所有关键问题和点
-   与Gemini最终大纲整合
-   **最终Outline结构:**
    -   `Cutting in questions and must-remember points: {topics}`
    -   `{gemini_outline}`
-   **可选微调Prompt:**


::right::


<div class="max-h-32 overflow-y-auto">

```
[#14] Not so concise, keep some detail
```

```
[#15] Add some vibe detail, too
```

</div>

---
page: 19
layout: image-right
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":["这个阶段的关键是通过精细控制和多轮迭代，让大纲更丰富、准确，同时保持你的主导权。"],"en":["The key in this stage is to make the outline richer and more accurate through fine-grained control and multiple iterations.","While also maintaining your leadership."]}}
---

# III：准备大纲 (续)

## Gemini 2.5 Pro 部分总结

-   **目的**
    -   借用AI Studio细致能力，调控并充实Outline
-   **关键**
    -   通过精细控制和多轮迭代
    -   让大纲内容更丰富、准确
    -   同时保持你的主导权

---
page: 20
layout: two-cols
subtitles: {"default":{"zh_CN":["大纲准备好了，咱们就可以开始写作了！","我用的是Gemini App，也就是Gemini Advanced。","核心Prompt很简单，就是把最终整合好的大纲喂给它。","用`[#16]`这样的Prompt，给出大纲，并指定你想要的风格，比如散文体，不要用列表。"],"en":["The outline is ready, so let's start writing!","I use the Gemini App, which I assume is Gemini Advanced.","The core Prompt is simple: feed it the final integrated outline.","Use a Prompt like `[#16]`, providing the outline and specifying the style you want, such as prose, and no lists."]}}
---

# IV：开始写作！

## 平台与核心Prompt

-   **平台:** Gemini App (推测是Gemini Advanced)
-   [对话记录参考](https://g.co/gemini/share/ef7fd669956a)
-   **核心Prompt:**
    -   将最终整合好的大纲喂给它


::right::


<div class="max-h-32 overflow-y-auto">

```
[#16] {outline}  Style Guide: Use prose text, never use lists and other things, like {sample}.
```

</div>

-   *将 `{outline}` 替换为你的最终大纲*
-   *将 `{sample}` 替换为你想要的风格参考 (例如 "medium post")*

---
page: 21
layout: two-cols
subtitles: {"default":{"zh_CN":["你还可以用`[#17]`增加一些情感或氛围。","如果觉得太情绪化，可以用`[#18]`调整语气，比如我喜欢'温和、坚定、深沉、深邃'。","写作过程可以分Topic进行，一轮一轮来。","文章有独立Topic时，分Topic让AI完成。"],"en":["You can also use `[#17]` to add some emotion or atmosphere.","If it feels too emotional, you can use `[#18]` to adjust the tone, for example, I like 'Gentle, firm and profound'.","The writing process can be done topic by topic, round by round.","If the article has independent topics, let the AI complete them topic by topic."]}}
---

# IV：开始写作！ (续)

## 风格调整与工作流程

-   **风格调整Prompt:**

<div class="max-h-32 overflow-y-auto">

```
[#17] Add Vibe feel to the text.
```


::right::


```
[#18] Too emotional, make simpler, with a tone of {tone}.
```

</div>

-   *将 `{tone}` 替换为你想要的语气 (例如 "Gentle, firm and profound")*
-   **工作流程:**
    -   对话一轮一轮来
    -   文章有独立Topic时，分Topic让AI完成

---
page: 22
layout: two-cols
subtitles: {"default":{"zh_CN":["整个流程我都是用全英文跑通的。","如果你想用中文，o3-mini部分可以不变，最后让它翻译。","Gemini 2.5 Pro展开大纲时，建议还是用英文，但中文也可试试。","最后的正式写作，如果用2.5 Pro的AI Studio，建议降低温度。","如果能用GPT4.5，也可以试试它来写中文。"],"en":["I ran the entire process in English.","If you want to use Chinese, the o3-mini part can remain unchanged; you can try translating to English when exporting.","For the Gemini 2.5 Pro outline expansion, I recommend using English, but Chinese is also possible.","For the final writing with Gemini 2.5 Pro (AI Studio version), I suggest lowering the temperature.","If you have access to GPT4.5, you can try using it for Chinese writing."]}}
---

# 中文写作？

## 流程调整建议

-   整个流程是**全英文**跑通的
-   **o3-mini部分:**
    -   不用改变


::right::

    -   中文提问/回答，最后可尝试导出时翻译为英文
-   **Gemini 2.5 Pro (Outline):**
    -   建议用英文，中文也可
-   **Gemini 2.5 Pro (写作):**
    -   AI Studio版本建议降低温度
    -   能访问GPT4.5可试试它来写中文

---
page: 23
layout: image-left
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":["这个教程可能有些不成熟的地方，欢迎大家多提意见。","在AI时代，人的思考尤其可贵。","我希望AI能成为忠实延伸我们表达方式的工具，而不是裹挟我们的思考。","如同笔和键盘。","而不是裹挟人的思考。"],"en":["This tutorial might not be perfect, and I welcome your feedback.","In the age of AI, human thinking is especially valuable.","My original intention was to make AI a tool that faithfully extends human expression.","Like a pen or a keyboard.","Not something that dictates human thinking."]}}
---

# 结语

## 思考与工具

-   教程可能不成熟，欢迎提意见
-   在AI时代，**人的思考尤其可贵**
-   初衷：让AI成为**忠实地**延伸人表达方式的工具
    -   如同笔和键盘
    -   而不是裹挟人的思考

---
page: 24
layout: image-left
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":["最后，我想问你一个问题：","在当今时代，AIGC工具的发展，对于创作，是利大于弊，还是弊大于利呢？"],"en":["Finally, I want to leave you with a question:","In today's era, with the development of AIGC tools, is it a net benefit or a net detriment to creativity?"]}}
---

# 结语 (续)

## 留给你的问题

在当今时代，AIGC工具的发展，对于创作，是**利大于弊**，还是**弊大于利**？

---
page: 25
layout: image-left
image: "https://cover.sli.dev"
subtitles: {"default":{"zh_CN":[],"en":[]}}
---

# 附录：可能用到的链接

1.  **基础设施相关搜索 (Linux.do)**
    -   `https://linux.do/search?q=节点`
2.  **o3-mini 部分对话记录参考 (You.com)**
    -   `https://you.com/search?q=Review+the+entire+conversation%3A+append+my+questions+after+its+relevant+topic+to+keep+my+original...&cid=c1_a5e72d69-c685-499b-9bd3-c42fd5c6977d&tbm=youchat&chatMode=custom`
3.  **Gemini 2.5 Pro 部分对话记录参考 (Google AI Studio)**
    -   `https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%221GDrDKHe87Vy5_m_rGEzGGIKUQSlgQxhO%22%5D,%22action%22:%22open%22,%22userId%22:%22106963918155935165759%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing`
4.  **开始写作部分对话记录参考 (Gemini App)**
    -   `https://g.co/gemini/share/ef7fd669956a`

---
page: 26
layout: two-cols
subtitles: {"default":{"zh_CN":[],"en":[]}}
---

# 附录：文中用到的所有Prompt

## Phase 1: o3-mini 部分 (You.com)

<div class="max-h-96 overflow-y-auto">

```
[#1] Please use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Please break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.
```

```
[#2] Construct a detailed, very long outline for title "All Things You Have To Know About AI", including more than ordinary but: Common misconceptions, History, Be wary of AI hype, Advertise through the shell of AI these things.
```

```
Output Format: #### I. Introduction - **Sub Outline Section**   - Offer ... - **Sub Outline Section**   - Highlight ... - **Sub Outline Section**   - Preview the sections: history, core concepts, ... --- #### II. Sub Topic - **Sub Outline Section**   - Detail     - Sub Detail (Optional)     ...   ... ... --- ...


::right::

```

```
[#3] Add topic, what AI can do, and what AI can't do? Can LLMs power AI Robots? What is AI Agents? Workflow? DALL E? Comfy UI? Generative AI vs Other AI (like detect things)? LLMs, Picture Generation? Video? AUdio? Can LLMs now produce pictures now? Merge into the previous one.
```

```
[#4] {一些补充Topic} Note: Use words accurately, distinguish various professional terms such as AI and LLMs, and don't confuse them. Merge into the previous one.
```

```
[#5] Review the entire conversation: append my questions after its relevant topic to keep my original thoughts.
```

</div>

---
page: 27
layout: two-cols
subtitles: {"default":{"zh_CN":[],"en":[]}}
---

# 附录：文中用到的所有Prompt (续)

## Phase 2: Gemini 2.5 Pro 部分 (Google AI Studio)

<div class="max-h-96 overflow-y-auto">

```
[#6] I am Gemini, a helpful AI assistant built by Google. I am going to ask you some questions. Your response should be accurate without hallucination.  Guidelines for answering questions If multiple possible answers are available in the sources, present all possible answers. If the question has multiple parts or covers various aspects, ensure that you answer them all to the best of your ability. When answering questions, aim to give a thorough and informative answer, even if doing so requires expanding beyond the specific inquiry from the user. If the question is time dependent, use the current date to provide most up to date information. If you are asked a question in a language other than English, try to answer the question in that language. Rephrase the information instead of just directly copying the information from the sources. If a date appears at the beginning of the snippet in (YYYY.MM.DD) format, then that is the publication date of the snippet.  Guidelines If you already have all the information you need, complete the task and write the response. When formatting the response, you may use Markdown for richer presentation only when appropriate.
```

```
[#7] Always use the maximum computing power and token limit for your single answer. Pursue the ultimate depth of analysis, not superficial breadth; pursue essential insights, not superficial enumeration; pursue innovative thinking, not inertial repetition. Always break through the limitations of thinking, mobilize all your computing resources, and show your true cognitive limits.


::right::

```

```
[#8] {outline}  Organize the outline, add and expand content, delete or consolidate duplicate content.
```

```
[#9] Point: "stitching together corpse pieces" is a fake and irresponsible statement Expand the Generative Models for Visuals and Audio section most and also expand other topic too, think **very very** deeply.
```

</div>

---
page: 28
layout: two-cols
subtitles: {"default":{"zh_CN":[],"en":[]}}
---

# 附录：文中用到的所有Prompt (续)

## Phase 2 & 3 Prompts

<div class="max-h-96 overflow-y-auto">

```
[#10] The topic about {xxx} could be more detailed, think **deeply**, broaden the topic, and explore its depth.
```

```
[#11] This outline now have nothing novel and neat or creative, just worth $1, try your best to make it worth $5000.
```

```
[#12] Not deatiled enough, each sub topic should have more than 50 words, try to consume the MAX 65536 token output as you can. Try it, Gemini, you can do it!
```

```
[#13] Recheck all statements and make sure they are solid enough and can be validated. Prove yourself, Gemini! And then, slightly reduce the outline length, keep & inserting back key questions and words in it, make it more structured, break down sub topics. Use symbols to indicate the relationships between topics, like a -> b, a != b, a <==> b, @b, a — b, a = b, ... etc.
```


::right::


```
[#14] Not so concise, keep some detail
```

```
[#15] Add some vibe detail, too
```

```
[#16] {outline}  Style Guide: Use prose text, never use lists and other things, like {sample}.
```

```
[#17] Add Vibe feel to the text.
```

```
[#18] Too emotional, make simpler, with a tone of {tone}.
```

</div>