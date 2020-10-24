---
layout: docs
title: rendering formula
group: docs-volantis-latest
order: 404
short_title: 4-4 rendering formula
sidebar: [docs-volantis-latest, toc]
mathjax: true
disqus:
  path: /wiki/volantis/
---

The default is not to render. If there is a formula in the article, it needs to be set to enable in front-matter. Even if it is turned on, the article list will not be rendered. Please be careful not to write the formula at the beginning of the article.

<!-- more -->


```md example.md:
---
title: Rendering formula (MathJax)
date: 2020-02-23
mathjax: true # false: do not render, true: render
---

Add a descriptive text

<!-- more -->

$$t+1=2$$

$$
\mbox{accumulation factor}=\begin{cases}
1+ni & \mbox{simple interest}\\\\
(1+i)^n & \mbox{compound interest}
\end{cases}
$$

$$
\begin{equation}
\sum_{i=0}^n F_i \cdot \phi (H, p_i)-\sum_{i=1}^n a_i \cdot (\tilde{x_i}, \tilde{y_i}) + b_i \cdot ( \tilde{x_i}^2, \tilde{y_i}^2)
\end{equation}
$$
$$
\begin{equation}
\beta^*(D) = \mathop{argmin} \limits_{\beta} \lambda {||\beta||}^2 + \sum_{i=1}^n max(0, 1-y_i f_{ \beta}(x_i))
\end{equation}
$$
```

{% folding View formula rendering effect %}
$$t+1=2$$

$$
\mbox{accumulation factor}=\begin{cases}
1+ni & \mbox{simple interest}\\\\
(1+i)^n & \mbox{compound interest}
\end{cases}
$$

$$
\begin{equation}
\sum_{i=0}^n F_i \cdot \phi (H, p_i)-\sum_{i=1}^n a_i \cdot (\tilde{x_i}, \tilde{y_i}) + b_i \cdot ( \tilde{x_i}^2, \tilde{y_i}^2)
\end{equation}
$$
$$
\begin{equation}
\beta^*(D) = \mathop{argmin} \limits_{\beta} \lambda {||\beta||}^2 + \sum_{i=1}^n max(0, 1-y_i f_{ \beta}(x_i))
\end{equation}
$$
{% endfolding %}


If the formula still cannot be rendered correctly, you can read this article by [@MicDZ](https://www.micdz.cn):

{% link Use KaTeX on Material-X, https://www.micdz.cn/article/katex-on-volantis/, https://www.micdz.cn/img/h.jpeg %}