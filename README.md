# Lyapunov指数谱数值分析 (Benettin算法)

## 项目简介
基于Hamiltonian系统 (势能 V = λ x² y²)，使用四阶Runge‑Kutta积分和QR重正交化方法计算Lyapunov指数谱。分析了能量对最大Lyapunov指数的影响，并绘制了区域谱图。

## 主要功能
- 修正Gram‑Schmidt与Householder QR分解
- 四阶Runge‑Kutta积分器
- Benettin算法计算Lyapunov指数
- 参数扫描与可视化

## 环境依赖
Python 3.7+, numpy, scipy, matplotlib, tqdm

## 运行示例
见notebook中的代码单元格。

## 结果示例
<img width="1200" height="900" alt="LLE_heatmap_small" src="https://github.com/user-attachments/assets/d0f6bc0a-587c-4056-b0f9-059df829bed8" />

<img width="5370" height="1454" alt="fig_trajectory_regular" src="https://github.com/user-attachments/assets/01076146-a3ae-4614-96f1-3151996e7427" />

<img width="3570" height="1166" alt="fig_energy_conservation" src="https://github.com/user-attachments/assets/82a2cf57-7905-4be0-aa21-58b597d0d4c7" />
