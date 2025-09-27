# Abstract

- 问题1：这篇论文的主要内容是什么？（用1-2句话概括）
- 问题2：论文的哪些部分是支撑性的论据？（列出关键证据、图表、数据）
- 问题3：这篇论文有哪些亮点和不足？或者它引发了什么新思考？（批判性思考）

digital twins, which serve as virtual replicas of a real scene but are
expensive to generate and cannot produce cross-domain generalization.

摘要：在现实世界中训练机器人策略可能不安全、成本高昂且难以扩展。模拟是一种廉价且可能无限的训练数据来源，但存在模拟环境和真实环境之间的语义和物理差异。这些差异可以通过数字孪生的训练来最小化，数字孪生充当真实场景的虚拟副本，但生成成本高昂，并且无法产生跨域泛化。为了解决这些限制，我们提出了数字表亲的概念，这是一种虚拟资产或场景，与数字孪生不同，它没有明确模拟现实世界的对应物，但仍表现出相似的几何和语义可供性。因此，数字表亲同时降低了生成类似虚拟环境的成本，同时还通过提供类似训练场景的分布来促进模拟到真实域传输过程中更好的鲁棒性。利用数字表亲，我们引入了一种新的自动化创建方法，并提出了一种全自动的真实到模拟到真实的管道，用于生成完全交互的场景和训练可以在原始场景中零样本部署的机器人策略。我们发现，可以自动生成保留几何和语义可供性的数字表亲场景，并可用于训练优于在数字孪生上训练的策略的策略，在零样本模拟到真实传输下实现 90% 和 25% 的成功率。

 real-to-sim-to-real pipeline

Fully interactive digital cousin scenes can be generated completely automatically from
a single RGB image. 

 relax the assumption of completely reconstructing
the minute details of a given scene and instead focus on preserving higher-level details,

解决模拟世界和真实世界语义和物理属性不匹配的方法：
1. “增强合成数据分布” 就是有目的地扩大和丰富合成数据的统计特征，使其更接近真实世界的分布。
- 随机化物品核心属性，如视觉语义和物理属性
- 人工策划或程序生成的场景级分布
生成环境分布：
these approaches can fail to capture necessary affordances
needed for downstream tasks and still require human input
**无法抓住下游任务所需的必要属性
需要人工输入
缺乏交互质量和数据规模**

  **与生成场景相比，引出数字孪生和数字表亲**
  
数字表亲：

解决数字孪生生成成本高，针对单一场景优化而无法泛化到原始世界的两个极端问题
实现方法
- 数字表亲放宽了重建精确副本的要求，包含数字表亲的场景反而侧重于保留高级场景属性，例如空间对象布局以及关键语义和物理可供性。
- 可以为单个真实场景生成多个不同的表亲，而同一场景只能存在一个数字孪生。

因此，这种放松有两个目的：
(a)它减少了手动微调的需求，以保证一定程度的保真度，从而使得完全自动创建数字表亲成为可能
(b)通过提供用于训练机器人策略的增强场景集，它提高了对原始场景变化的鲁棒性。
