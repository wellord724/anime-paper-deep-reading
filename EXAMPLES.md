# 使用与编辑示例

“精读这篇论文，生成可切换中英文的离线交互报告。”
输出中文与英文 Markdown、同一份双语 HTML；从模板复用视觉与控制，替换领域图解，完整覆盖方法、实验、局限与八问。

“只要英文，篇幅适合组会前阅读。”
遵循单语要求，保留原风格；根据证据密度压缩，不强行生成另一份全文。

## 写作

避免：“该创新框架显著提升了表现，为层级表示学习开辟了全新道路。”
改为：“在 WordNet 缺失关系预测中，5维 Poincaré 的 MAP 为0.825，同维欧氏模型为0.024（表1）。这支持低维层级排序的优势，但没有覆盖非层级数据。”示例数值须重新核对原论文后使用。

Avoid: “This groundbreaking approach unlocks unprecedented possibilities.”
Prefer: “The result supports compact hierarchical ranking in this benchmark. It does not establish an advantage on arbitrary non-hierarchical data.”

## 数学公式

不要把 `softmax(QK^T / sqrt(d_k))V` 当作最终公式，或放入 `text` 代码块。Markdown 写作：

$$
\operatorname{Attention}(Q,K,V)
=\operatorname{softmax}\!\left(\frac{QK^{\top}}{\sqrt{d_k}}\right)V.
$$

HTML 必须把对应 LaTeX 渲染为专业数学排版。动态输出向量可使用 `\mathbf z=\begin{bmatrix}0.340\\0.000\end{bmatrix}`；它是教学数值示例，实际数值须与交互计算一致。中英文只切换解释文字，公式符号保持一致。

## 交互选择

几何论文可用半径滑块联动位置、距离与公式；优化论文可展示真实算法步骤与明确标注的数值演示；实验论文可切换报告过的配置；理论论文可展示条件与推导依赖。不要给所有论文套用圆盘、虚构消融开关或流动粒子。
