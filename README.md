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

对称初始条件(1.0,1.0,0.0,0.0)下的规则周期运动轨迹
<img width="5370" height="1454" alt="fig_trajectory_regular" src="https://github.com/user-attachments/assets/01076146-a3ae-4614-96f1-3151996e7427" />

系统总能量随时间的演化及能量漂移
<img width="3570" height="1166" alt="fig_energy_conservation" src="https://github.com/user-attachments/assets/82a2cf57-7905-4be0-aa21-58b597d0d4c7" />

二维\(x^2y^2\)势场中经典哈密顿系统的混沌运动特征  
初始条件为\(z_0=[x_0,y_0,v_{x0},v_{y0}]=[1.0, 0.0, 0.0, 0.5]\)，势场强度\(\lambda=1.0\)。  
左图：粒子在x-y平面的运动轨迹，呈现无周期性、遍历性的非闭合不规则缠绕结构，红点标记粒子初始位置；  
中图：50个积分时间单位内坐标变量\(x(t)\)（蓝线）与\(y(t)\)（橙线）的时间序列；  
右图：哈密顿量守恒验证，全积分时段内最大绝对能量漂移\(\Delta E_{max}=3.60\times10^{-12}\)，验证了所采用四阶龙格-库塔积分方案的高数值精度。
<img width="1564" height="420" alt="image" src="https://github.com/user-attachments/assets/8a369c48-8045-487a-ac45-b53be12ebfec" />

初始 (x,y) 平面上最大 Lyapunov 指数的空间分布  
为进一步验证系统的通用特性，参考文献对 (α,E) 参数平面的混沌分布进行了扫描，结果如图所示：高耦合强度和高能量区域的平均最大 Lyapunov 指数显著更高，与固定 λ=1 时，高能量初始位置（如四角区域）MLE 更大的结论一致
<img width="1200" height="900" alt="LLE_heatmap_small" src="https://github.com/user-attachments/assets/d0f6bc0a-587c-4056-b0f9-059df829bed8" />
