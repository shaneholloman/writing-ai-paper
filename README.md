# Writing AI Conference Papers: A Handbook for Beginners

**We believe that what this article needs the most is peer review, and we warmly welcome valuable suggestions in any form.**

Author: [hzwer](https://github.com/hzwer), [DingXiaoH](https://github.com/DingXiaoH)

知乎 [1](https://zhuanlan.zhihu.com/p/593195527)-[2](https://zhuanlan.zhihu.com/p/639732057)-[3](https://zhuanlan.zhihu.com/p/627032371)｜[跃问中翻](https://yuewen.cn/share/145749938443137024?utm_source=share&utm_content=web_linkcopy&version=2) | [豆包总结](https://www.doubao.com/thread/w750d882cf0af6419) | [公众号](https://mp.weixin.qq.com/s/MjeBZDV6xapuA_L6ODpVcA)

**Abstract.** *Crafting a research manuscript can pose significant challenges for novices, particularly when time is scarce before the deadline and the authors lack experience in academic submissions. An ill-prepared manuscript can be a source of distress for both collaborators and readers, frequently leading to rejection or necessitating substantial revisions. In this article, we'll share some tips for beginners who want to write AI conference papers. Our goal is for this article to be a guide for beginners, making it easier to share academic achievements.*

## Introduction

> **Background.** The GPU cluster has been running for half a year, and you feel that the results are already significant. You realize that the deadline for an upcoming conference is less than a month away, yet you have only written some course assignment reports. How far in advance should the first draft be completed to avoid missing the deadline? What distinguishes a good research paper from a bad one? What should be done before starting to write? These questions plague you like a nightmare, leaving you staring at the blank Overleaf homepage. Luckily, this article is written for you. 

In this article, we will discuss the aspects related to writing conference papers, with a focus on common pitfalls, catering to novices. Our article mainly consists of two parts: **[completing a paper](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#build-a-paper-from-scratch)** and **[refining its details](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#readability-improvement)**. We aim to provide practical guidance that will enable novices to navigate the complexities of academic writing and contribute to the field with clarity and confidence. Sincerely, we recommend the [Resource List of Writing Tips](https://vision.sjtu.edu.cn/writing.html) curated by Chao Ma.

## Build a Paper from Scratch

This section outlines writing an AI paper from scratch, covering core idea, whole framework, introduction and related work.

### Find the Core Idea
You may have interesting findings and experimental results, but you're unsure how to define the core theme. *The key contribution of most published papers falls into exactly one out of the following three categories (from [Nowozion](https://www.nowozin.net/sebastian/blog/ten-tips-for-writing-cs-papers-part-1.html)):*

*Insight: you have an explanation for something that is already there.*

*Performance: you can do something better.*

*Capability: you can do something that could not be done before.*

Identify the core advantages of your work and emphasize them early in the paper. This way, readers can read the remaining parts with expectations. You can further expand the overall novelty from other aspects as well. **Novelty seems to be elusive, what is it?** Key research topics, efficient solutions, and innovative technical contributions are the primary elements that contribute to a paper's novelty. For instance, numerous early influential works of deep learning emerged from foundational model research due to their potential to impact the entire field. The RAFT/NeRF methods have attracted a large number of researchers due to their outstanding performance, and they involve a lot of engineering handling beyond their core ideas. Techniques such as "Batch Normalization" and "Residual Learning" are esteemed for their effectiveness. By emphasizing the novelty of your work, you'll be able to discern which aspects are worth the effort and which are inconsequential details.

> A little squiggle of paint by Picasso can be as beautiful as an intricate painting by Rembrandt. —— [Novelty in Science](https://medium.com/@black_51980/novelty-in-science-8f1fd1a0a143) (highly recommended for readers)

***Take-away: Clearly understand the increment over previous methods and find one or two core ideas.***

When readers read papers, they seek novel insights. A good paper should have strong points that are easy to remember. You should refine your central ideas until you're confident that people will be eager to learn about them and share them widely. It is particularly worth noting that some ideas may be great, but if they lack originality, it may not be advisable to describe them in detail in the paper. When writing a paper, the focus should be on providing novel, unique, and valuable insights to attract readers' attention and inspire their interest.

Don't underestimate the novelty of your own work. Delve deep to uncover the underlying principles. If the ResNet paper were rewritten as: "We designed a model using a large number of $3\times3$ convolutions (inspired by VGGNet) and parallel shortcuts (simplified from GoogleNet) **based on** the former two", then it will also become a paper without novelty. The story told by the ResNet paper is to propose a problem, abstract the underlying principles, propose its own solutions and specific implementations, and verify them experimentally. This might not totally reflect [their research process](https://www.zhihu.com/question/406913672/answer/1339549216), but it effectively showcases their discoveries.

***Take-away: Discovering new phenomena and sharing new ideas matter more than performance gains.***

A good number of excellent papers often show strong results in experiments. This can make people think that good results are all that matters in a paper. But actually, experimental results are just proof of new discoveries. Small improvements in results don't always mean new knowledge. When you write a paper, think first about what new things readers can learn from your work—not just about showing off better results than others.

In addition, as Kaiming He points out, researchers should focus on the future rather than solely on past "state-of-the-art." By applying Occam's Razor—seeking simple yet effective solutions—and validating research in real scenarios while forecasting experimental outcomes and future needs, researchers can reduce "overfitting" in their studies. Rather than meticulously refining experimental designs and metrics solely for immediate validation, it's more valuable to consider the long-term correctness and relevance of the work during the paper-writing process. The enduring, correct discoveries sustain their influence over time. By stripping away convoluted techniques used merely for paper publication and identifying straightforward, effective solutions, researchers increase the likelihood of their work generalizing to future scenarios.

### Construct the Framework
***Take-away: Abstract - Introduction - Main body, which are gradually unfolded. Each part is self-complete.***

The typical structure of a paper includes 1. an abstract, 2. an introduction, and 3. the main body, which encompasses sections such as related work, methodology, experiments, discussion, conclusion, and references. We can break down this structure into three levels. At each level, you should aim to convey a comprehensive research narrative. Each level serves as an expansion of the preceding one. With this understanding, let's explore how to effectively present a research story. For those who are starting out, it's advisable to focus on completing the main body of the paper first.

***Take-away: Consider the target audience, introduce the valuable findings rather than the tortuous research process.***

While adhering to the core ideas, start outlining the content you intend to present in your paper. Begin by creating a simple slide to demonstrate your research approach and achievements to your peers, colleagues, or mentors, in order to assess their understanding. It may be beneficial to intentionally seek feedback from researchers unfamiliar with your work to identify potential gaps in comprehension. Unlike the experimental process, it is advisable to emphasize valuable novelties and avoid presenting incomplete or complex aspects of your research. Researchers all understand the pain of research, but the bitter portrayal is only suitable for the postscript of the project. Continuously review and refine your presentation from the reader's perspective until it is easily understandable.

It may also be necessary to supplement your work with additional experiments if you feel that your experimental rationale lacks rigor. At the same time, it is advisable to conduct thorough literature research, ideally identifying several papers with highly relevant topics. Consider these as potential competitors to your paper and examine them for areas of improvement. Reflect on which aspects would captivate the community and accentuate them, while minimizing the inclusion of clichéd content. 

***Take-away: Around the contribution statements, conduct a solid analysis in the result section.***

Many readers will initially assess the method's effectiveness by examining the results before deciding to read the entire paper. They will look to see if your contribution aligns with the experimental findings. Even with strong confidence in your method's efficacy, you will likely need additional comparative and ablation experiments. It's important to create more tables and visuals, selecting the most significant aspects to present. Honesty and objectivity are crucial; overstating claims is particularly undesirable. If concerned about overclaiming, discussing with peers is advisable.

### Write an Introduction
With the above materials, you can start trying to write the introduction. Regarding the structure of the introduction, we directly quote from the textbook (from [Elena](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3178846/)):

**Move 1. Establish a research territory**

a. Show that the general research area is important, central, interesting, and problematic in some way;

**Move 2. Find a niche**

a. Indicate a gap in the previous research, or extend previous knowledge in some way.

**Move 3. Occupy the niche**

a. Outline purposes or state the nature of the present research;

b. List research questions or hypotheses;

c. Announce principle findings;

d. State the value of the present research;

e. Indicate the structure of the research paper.

**Additional suggestions:**

a. Knuth: *Keep the reader upper-most in your mind;*

b. Cut to the chase and don't write too much irrelevant to the paper's topic. The novel and interesting aspects of the paper should appear as early as possible;

c. Dedicate more space to describing original and novel ideas;

d. Respect the work of predecessors, and affirm historical contributions before pointing out shortcomings;

e. Consider using a "page one figure" to highlight the most important aspects of the paper and catch the reader's attention.

As we mentioned earlier, the main body is actually an extended version of the introduction. Typically, supplementing the introduction with additional experimental details forms the main body of the paper.

### Describe the Related Work
***Take-away: The mediocre approach is to describe the correct history, while the better approach is to focus on how different methods relate to what you do.***

The part may not be included in the context of the introduction. A paper typically has a separate section dedicated to discussing related work, including some background work and competing work. Find three or four topics that are most relevant to your paper, and outline the historical evolution under each topic. Do not list all the negative aspects of other techniques, but rather explain how you improve upon them. You can first write a literature review that is independent of your work. When classifying and ordering the previous methods (for example, refer to a certain method as a pioneer), it is important to pay attention to the correctness of discussion. If you are not confident enough, check the "related work" sections of the papers you referenced. Finally, rewrite this section from a more appropriate angle to reflect the unique aspects of your paper. 

## Readability Improvement
> "Writing endures through the ages, its merits and faults known only to the author's heart. (文章千古事，得失寸心知）" —— [Du Fu](https://en.wikipedia.org/wiki/Du_Fu)

> "The best writing instruction ever: Good writing is bad writing rewritten. I got it from Stephen King. Where Stephen King got it, I don't know. I'm giving it to you. You tell your students." —— [Robert Weiss](https://robweiss.faculty.biostat.ucla.edu/writing_advice_2)

***Take-away: The more prominent part, the more time you invest in it.***

Next, we will mainly discuss the polishing of the details. At present, AI assistants like [ChatGPT](https://chatgpt.com) and [Claude](https://www.anthropic.com/news/claude-3-5-sonnet) can easily help authors address the basic issues in English writing. We also recommend that authors in the Chinese region use [跃问](https://yuewen.cn/chats/new) or [豆包](https://www.doubao.com/chat/). You can have the AI generate multiple versions and choose the most suitable one. When utilizing these tools, remember that prioritize clarity over style.

Let's move on to discuss the issues that are not easy to handle automatically. We will measure the readability of papers using the following concepts: logical strength, defensibility, confusion time, and information density. Based on these concepts, some practical suggestions and techniques are described to improve the readability.

### Enhance Logical Strength
***Take-away: Do not misuse or abuse connectives.***

In academic writing, logical coherence is more crucial than elegant vocabulary. Logical coherence is rooted in the logic itself, not in the connectives. We should view connectives as enhancements that smooth language, rather than using them to artificially construct sentence logic. Misalignment between connectives and actual logic can be confusing and greatly diminish readability. Here are a few specific examples:

> We argue that problem A is critical. To this end, we propose method B.

"To this end" refers to which end? In fact, the previous context only presents a viewpoint without specifying any actions or goals, so the use of this connective is inherently incorrect. Connectives must be grammatically correct.

> The system comprises three modules. First of all, Module A is .... Second, Module B is .... Last but not least, Module C is ....

Here, several connectives impose a certain order on these three things that originally have no order relationship. We should not use connectives to create logical relationships. It would be better to introduce the three modules separately.

### Consider Defensibility
When we write, we should think about how readers might find fault with every sentence we write. If they believe something that seems wrong, they might doubt the whole paper. To enhance the paper's trustworthiness, we need to minimize the likelihood of being challenged.

***Take-away: Make statements based on references and facts.***

When we write "Problem A is a pain point in this field and has not been solved yet," we should consider that the reader may ask, "Why is this a pain point? How serious are the consequences? Does this consequence have a significant impact on the final performance?" This requires the addition of appropriate references.

> It is reported that problem A results in ... [1,2,3] and ... [4,5], which are critical to ... because ... [6, 7, 8].

When discussing the results of a paper, it is even more necessary to be rigorous:

> The performance improves, which is attributed to the fact that XXX...

The evidence should be presented prominently;

> The improvement may be explained by the fact that XXX...
 
Some indirect evidence such as visualizations can be shown.

Be as objective as possible and avoid exaggerating.

### Shorten Confusion Time
"Confusion time" is the sum of the time readers spend on each "hmm, what's this?" to "oh, I get it" moment during the reading process. The shorter the total confusion time of a paper, the higher the readability, and the more peaceful the reader will be.

***Take-away: Explain a concept as close as possible when it is proposed.***

It is recommended to directly explain the essence of a component after giving its name; for example, "We propose XXX, which is implemented with a two-layer multilayer perceptron (MLP)." If a concept is not easy to explain, it can be supplemented by referring to literature.

***Take-away: Resolve relative pronoun ambiguity.***

If it is not possible to make a long sentence completely unambiguous, it should be broken down into short sentences. A large proportion of the readership is not native speakers, and fancy sentence structures do not earn extra points.

***Take-away: Frequently use topic sentences, preferably at the beginning of paragraphs.***

The reader may not be able to quickly understand all the details, at which point the main information can be quickly obtained by the reader through the topic sentences, to avoid affecting the overall reading experience.

### Increase Information Density
"Information density" refers to the efficiency with which text provides effective information to readers. Low information density may cause readers to lose focus and question the expertise.

***Take-away: Get to the point as soon as possible.***

The beginning of each section may talk about the history. Try not to be lengthy. "Do not write irrelevant content, nor should you write about things that most readers are already familiar with." Discussing the development of human writing skills, would certainly deter the vast majority of our readers.

***Take-away: Both text and charts should be appropriately detailed or concise.***

Use an appropriate layout that balances text and visuals. Avoid common pitfalls like featuring a large chart with only a few key points highlighted. Or a very long passage describing the experimental details and hyper-parameters, which should really be placed in the appendix.

***Take-away: Important explanations and elucidations should be as close to the charts as possible.***

The ideal situation is that each chart can be understood independently of the main text. In the caption, try to clearly state the theme and key conclusions. If there are abbreviations in the chart, it is best to have an explanation. 

If you want to emphasize a certain result in Table 5, it is best for the sentence analyzing that result to be on the same page as Table 5, and it is best to have the words "Table 5" before and after that sentence. This is because readers may not carefully read the text you write, but first look at the charts and then look for text related to the content of the charts. When they see a striking result in Table 5 and become curious, they may use the search function in the PDF reader to search for "Table 5". 

Do not expect readers to figure out for themselves from a complex table who should be compared with whom to draw conclusions. We should put the content we want to compare. If such a table is difficult to design, it is worth repeating a certain result (usually a baseline that needs to be compared with several groups of results) several times, even if it means sacrificing the elegance. No one will reject your paper because the tables are not elegant, but it is very annoying if the table is not clear.

### Detail Checklist
First and foremost, avoid making mistakes. Prioritize the rigor of the paper before considering its aesthetics. The following is a checklist that can help authors improve their writing:

- [ ] Go through the charts to ensure the story is complete. Strive to improve the quality of the charts and make them self-explanatory.
- [ ] Check for any inconsistencies in symbols, abbreviations, and references.
- [ ] Whether the level of detail in the text and charts is appropriate?
- [ ] Place important information in prominent positions.
- [ ] Can the text and legends in the figure be larger?
- [ ] Can the understanding speed of tables be improved by using methods such as column division, bolding text, and deleting redundancy?
- [ ] Can the reproducibility be improved? For example, by providing details and key code in the appendix.

We will list more minor items in the [Appendix](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#appendix).
## Conclusion
***Take-away: Good luck!***

As this manuscript stands without the benefit of peer review, it undoubtedly contains numerous imperfections. The concepts presented herein are primarily derived from widely shared community knowledge, which we have endeavored to synthesize and simplify for the benefit of newcomers to the community. Our goal is to provide a concise yet comprehensive guide that can ease the learning curve for those embarking on the journey of writing AI conference papers. If this document serves as a beacon of clarity and direction for any reader, we would consider our efforts successful. *Leaving a star will be a great encouragement to us.*

## Appendix
In the Appendix, several topics are covered:

[Checklist for Last Few Hours](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#checklist-for-last-few-hours): It provides a checklist to ensure the paper is in order before submission.

[AI Paper Production and Publication](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#ai-paper-production-and-publication): It outlines the process of paper submission, review, and publication in AI conferences.

[Common Negative Review Comments](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#common-negative-review-comments): It lists common criticisms reviewers might have and suggestions for revision.

[If the Paper Is Not Accepted](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#if-the-paper-is-not-accepted): It offers advice on dealing with rejection and improving the paper for future submissions.

[AI Conference List](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#ai-conference-list): Some information of notable AI conferences that you might find useful.

### Checklist for the Last Few Hours
- [ ] Check that various numbers are not copied incorrectly.
- [ ] Search for question marks to check for latex errors.
- [ ] Make sure that all charts are mentioned in the main text and that the order of mentions matches the order in which the charts appear.
- [ ] The caption is very noticeable. Avoid grammatical errors, and it is recommended to use a period at the end.
- [ ] Vectorize the charts. 
- [ ] Check that all formulas are complete, they are easily overlooked in the editing process.
- [ ] Go through all the subtitles and unify the capitalization style.
- [ ] Confirm that there are no figures outside the main body pages.
- [ ] Check for anonymity. You may need to delete acknowledgments. If you have submitted code or a demo, you must also pay great attention to anonymity.
- [ ] **Ensure the number of pages is correct to avoid being desk rejected.**

### AI Paper Production and Publication

This section mainly introduces the process of producing papers and the review process. A conference paper usually runs about eight pages in a two-column layout, or over ten pages in a single-column layout, based on the conference's specifications. Authors prepare and submit their paper along with supplementary materials like code and demo videos by the given deadline.

Provided there are no critical oversights, such as neglecting to anonymize the submission, substantial formatting issues, or surpassing the page limit — any of which could result in an immediate rejection (known as a "desk reject") — the paper proceeds to the review phase. Following approximately two months, authors receive feedback from typically three reviewers in the form of comments and an overall score for their paper. Many of these reviewers have published work in related domains and might be cited in the submitted paper. With the initial review outcomes, authors must craft a brief rebuttal, generally one page, to address queries or provide additional findings. Roughly half of the papers are withdrawn during this rebuttal phase. Reviewers then deliberate for a week or two (commonly on a private platform) based on the rebuttal, indicating whether their concerns have been alleviated and discussing the paper's merits. Usually, reviewers align on a positive or negative stance, though occasionally, the area chair decides.

The final acceptance outcome necessitates waiting for approximately another month, after which it will be revealed via the email system. Typically, acceptance rates range from one-sixth to one-quarter of submitted manuscripts. Authors then revise their work based on reviewer feedback before submitting the final, camera-ready version for publication. The majority of papers, however, face rejection and are returned to the authors. These authors may opt to resubmit following the previously mentioned process or decide to discontinue work on the paper. It is worth noting that most papers undergo an extensive period of refinement and revision, colloquially dubbed the "Fibonacci Submission Approach." (Recommendation: [a Chinese lecture by Boxin Shi](https://hub.baai.ac.cn/view/8659)).

### Common Negative Review Comments
We have listed some common negative reviews and suggested revisions (in italics).

- Criticizing the author for being unprofessional: Important references are missing; the paper structure is messy, and some essential elements are lacking, such as not submitting supplementary video results for a video-related study; the experimental setup is significantly different from previous work. 

*Refer to the reference list of recent papers to fill in the gaps, and the configuration should be aligned.*

- Questioning the validity: The reported results do not conform to common sense and are not credible; exaggerating one's own achievements or making some obviously incorrect assertions; there are flaws in the experimental setup or argumentation. 

*Conduct more experiments, refine the expression, and strive for rigor.*

- Not respecting previous work: Not citing the latest results, conducting low-benchmark experiments; excessively demeaning the work of predecessors; confusing one's own work with the contributions of predecessors. 

*Compare more with existing work tables, conduct more paper research, and if you say others have done a poor job, provide evidence.*

- Lack of novelty: The story is not well written, the logic is not clear, or most of it is known knowledge; feeling that the work is incremental and does not contribute much. In other words, the effect is not impressive.

*Discuss with some peers, and highlight the strengths.*

- Poor paper presentation quality: Many grammatical errors, poor writing, poor English level; difficult to understand, lacking some details. 

*Use AI tools or [Grammarly](https://www.grammarly.com) to revise, and ask friends for help to read.*

- Disagreement on the approach: Not approving of the experimental design or not believing in this technical route.

*Conduct more experiments or cite similar expressions in relevant literature to support your argument, and try to win over other reviewers.*

### If the Paper is Not Accepted
> Review process is highly random. But there is one golden rule that withstands the test of time and randomness - **badly written papers get bad reviews. Period.** It doesn’t matter if the idea is good, result is good, citations are good. Not at all. Writing is critical — and this is ironic because engineers are the worst-trained writers among all disciplines in a university. You need to discipline yourself: leave time for writing, think deeply about writing, and write it over and over again till it’s as polished as you can think of. (Fei-Fei Li)

There are many papers that stayed on arXiv after being rejected and now have a huge impact [1](https://arxiv.org/abs/1503.02531);[2](https://arxiv.org/abs/1907.11692);[3](https://arxiv.org/abs/1704.04861);[4](https://arxiv.org/abs/1606.06160). [Many great works have been rejected and even got extremely negative comments.](https://www.reddit.com/r/MachineLearning/comments/vywfx3/d_are_there_any_rejected_papers_that_ended_up/) The review process is especially painful for novices, who may be putting all their eggs in one basket. The paper will be significantly improved throughout the process. If this process helps you produce a truly good paper, you can benefit from and be proud of it for many years to come. Remember, the paper is only the initial step or a small part of the overall work.

### AI Conference List
The schedule can usually be found on [AI Conference Deadlines](https://aideadlin.es/?sub=CV,ML,NLP). The acceptance rate can be found on [Conference-Acceptance-Rate](https://github.com/lixin4ever/Conference-Acceptance-Rate).

Note: Acceptance rates and submission dates vary. Always check the official conference website for the most current information.

| Conference Name | Typical Submission Month | Recent Acceptance Rate |
| --- | --- | --- |
| IJCAI | January | ~14% |
| ICML | January | ~27% |
| ICCV/ECCV | March | ~27% |
| BMVC | April | ~26% |
| ACMMM | April | ~26% |
| NeurIPS | May | ~26% |
| EMNLP | May | ~23% |
| WACV | June and August | ~45% |
| ACCV | July | ~33% |
| AAAI | July | ~24% | 
| ICASSP | September | ~45% |
| ICLR | September | ~31% |
| NAACL | September | ~23% |
| ICRA | September | ~45% | 
| AISTATS | October | ~28% |
| CVPR | November | ~24% | 
| ACL | Rolling Review | ~23% |
