---
toc: true
layout: post
description: Absolute Moments by Tail Probability
categories: [markdown]
title: Absolute Moments by Tail Probability
---


# 陳述 (statement)
Proposition 7.1. The absolute moments of a random variable $X$ can be expressed as
$$\mathbb{E}|X|^{p}=p\int_{0}^{\infty}\mathbb{P}(|X|\geq t)t^{p-1}dt,\quad p>0$$


---
# 證明 (Proof)

🦐 核心事件 (event): $$\{|X|^{p} \geq x\}$$

1. Recall that $I_{\left\{|X|^{p} \geq x\right\}}$ is the random variable that takes the value 1 on the event $|X|^{p}\geq x$ and 0 otherwise. 
2. Using Fubini's theorem, we derive
$\begin{aligned}
\mathbb{E}|X|^{p} &=\int_{\Omega}|X|^{p} d \mathbb{P}=\int_{\Omega} \int_{0}^{|X|^{p}} 1 d x d \mathbb{P}=\int_{\Omega} \int_{0}^{\infty} I_{\left\{|X|^{p} \geq x\right\}} d x d \mathbb{P} \\
&=\int_{0}^{\infty} \int_{\Omega} I_{\left\{|X|^{p} \geq x\right\}} d \mathbb{P} d x=\int_{0}^{\infty} \mathbb{P}\left(|X|^{p} \geq x\right) d x \\
&=p \int_{0}^{\infty} \mathbb{P}\left(|X|^{p} \geq t^{p}\right) t^{p-1} d t=p \int_{0}^{\infty} \mathbb{P}(|X| \geq t) t^{p-1} d t
\end{aligned}$
where we also applied a change of variables.
