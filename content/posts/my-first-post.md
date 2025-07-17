---
title: "Understanding Observability in Nonlinear Systems"
date: 2025-07-17
draft: false
---

In this post, I’ll explore the basics of **observability** in nonlinear systems—a topic central to my research.

---

## 🧠 What Is Observability?

Observability refers to whether a system’s internal state can be **inferred from its outputs** over time.

For a **nonlinear system**:

$$
\begin{aligned}
\dot{x}(t) &= f(x(t), u(t)) \\\\
y(t) &= h(x(t))
\end{aligned}
$$

where:
- \( x(t) \in \mathbb{R}^n \) is the state,
- \( u(t) \in \mathbb{R}^m \) is the input,
- \( y(t) \in \mathbb{R}^p \) is the output.

We say the system is **locally observable** at \( x_0 \) if different initial states around \( x_0 \) produce different outputs.

---

## 🔍 Lie Derivatives

A powerful tool in nonlinear observability is the **Lie derivative**. For a scalar output \( y = h(x) \), we define:

$$
L_f h(x) = \frac{\partial h}{\partial x} f(x)
$$

We compute higher-order Lie derivatives as needed.

---

## 🧪 Example

Let:

$$
\begin{aligned}
\dot{x}_1 &= x_2 \\\\
\dot{x}_2 &= -x_1 \\\\
y &= x_1
\end{aligned}
$$

This is a harmonic oscillator. You can verify that it is **observable**, since \( y = x_1 \), and differentiating gives access to \( x_2 \).

---

## 🧾 Summary

Observability is critical in designing sensors and state estimators. Future posts will explore:
- The observability Gramian
- Empirical observability
- Sensor placement algorithms

---

*Thanks for reading! Let me know if there’s a topic you’d like me to dive deeper into.*
