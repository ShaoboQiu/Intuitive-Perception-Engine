# Multi-Layer Abstraction and Intuitive Perception Engine  
**多层抽象与直觉识别引擎**

> *Intuitive perception engine for hazard recognition — a core module of the Safety Right-Brain*  
> 开发一种对危险环境进行直觉判断的识别引擎，是“安全右脑”的核心构成之一。

---

## 🌐 项目简介 | Project Overview

本项目旨在建立一种具备 **直觉识别能力** 的自动驾驶感知-认知系统，  
它作为 “安全右脑（Safety Right-Brain）” 的组成模块之一，用于实现对复杂交通场景的直觉化风险感知与预判。

**基于事故经验的风险推理（Experience-Driven Hazard Reasoning）** 系统的核心理念是参照 **人类认知多层抽象思维（Multi-Level Abstraction）** 的能力，  
构建一个能够理解“场景关系”而非仅仅识别“物理对象”的智能引擎。

---

## 🧠 理论背景 | Theoretical Background

根据 Marvin Minsky 在 *The Emotion Machine* 中的认知分层理论，人类智慧的关键在于能在多个抽象层级间自由切换。  
自动驾驶若要接近人类驾驶的策略与判断能力，就必须从低层像素计算上升到高层语义与关系推理。

**核心思想包括：**

- 从 **Low/Mid Levels**（像素、对象）跃升至 **High Levels**（关系、意图、场景）；
- 以 **Scene Relation** 而非 **Object Property** 为主要分析单元；
- 在 **SOTIF 模型** 四象限框架中，分别解决：
  - 第 II 象限：“显式规则” → 防御驾驶推理；
  - 第 III 象限：“隐式规则” → 基于事故数据的经验风险识别。

---

## 🔍 模块一：多层抽象需求分析  
**AV 的多层抽象要求**

该部分基于 Marvin Minsky 的认知层级理论，分析了人脑与机器在思维抽象方向上的差异。

- 人脑：由上至下（从概念到细节）  
- 机器：由下至上（从像素到语义）

**关键论点：**
1. 自动驾驶的高层智能需引入 **社会关系模型（Social Relation Model）** 与 **未来推理模型（Inference Future Model）**；
2. 场景分析的对象是“要素之间的关系”，而非要素本身；
3. 防御驾驶可视作 **“显式规则”** 的集合，可通过 SWRL / KG 表达；
4. 事故数据驱动模型用于发现 **“隐式规则”**，将 Unknown Unsafe 转化为 Known Unsafe。

📘 详见文件：
- [`AV 的多层抽象要求.pdf`](./AV%20的多层抽象要求.pdf)

---

## 🧩 模块二：事故数据驱动模型  
**根据 NHTSA 数据训练的事故预测模型**

本模块基于美国 NHTSA 的 FARS/CRSS 数据库，利用机器学习方法建立“场景-事故”因果模型，  
通过归纳方法提取隐式风险规则（Implicit Risk Rules），实现对未知危险的概率化预测。

**主要内容：**
- 数据源：NHTSA（美国）、GIDAS（德国）、ITARDA（日本）等；
- 输入：场景要素（人、车、路、设施、天气）；
- 输出：事故类型与事故严重程度；
- 数据规模：1975 – 2018 年 > 1.6 million cases；
- 应用目标：将经验风险注入到“安全右脑”的推理引擎中，解决 SOTIF 第 III 象限问题。

📘 详见文件：
- [`根据NHTSA数据训练的事故预测模型.pdf`](./根据NHTSA数据训练的事故预测模型.pdf)

---

## ⚙️ 系统功能架构 | System Architecture

1. **输入层（Perception Layer）**  
   感知环境场景要素（车辆、行人、道路、气象、信号灯等）

2. **抽象层（Abstraction Layer）**  
   将低层像素信息提升为关系网络（Knowledge Graph）

3. **推理层（Reasoning Layer）**  
   结合显式规则（防御驾驶）与隐式规则（事故经验）进行直觉判断

4. **输出层（Decision Support）**  
   生成可用于 ADAS 或 Autonomous Driving System 的风险指标 R 与安全建议

---

## 🧭 应用与意义 | Applications

- **ADAS / 自动驾驶系统的安全增强**
- **SOTIF 安全验证与风险闭环**
- **事故风险地图 / “危险快照” 生成**
- **基于知识-数据双驱动的安全右脑推理引擎**

---

## 📂 仓库结构 | Repository Structure

