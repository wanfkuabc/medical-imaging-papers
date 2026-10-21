# Medical Imaging Papers Collection

> **更新日期：2026-10-21** ｜ **时间范围：2020–2026** ｜ **收录标准：仅 CCF A 类正式会议主会论文**
>
> 论文覆盖医学图像分割、医学点云/三维重建、医学图像检测/定位以及医学图像配准。

## 筛选规则与使用说明

- **会议**：CVPR、ICCV、AAAI、NeurIPS（均按 CCF A 类会议口径）。
- **任务概念区别**：半监督 ≠ 弱监督 ≠ 完全无监督；医学图像配准中的“无监督”也不等于无监督医学分割。
- **主题相关性**：三维重建中部分方法为医学适用的通用几何方法，已显式标注；深度估计作为上游技术单列，不伪称完整重建。

## 目录

- [Part I. 医学图像分割与医学点云/三维重建](#part-i-医学图像分割与医学点云三维重建)
  - [1. 半监督医学图像分割](#1-半监督医学图像分割)
  - [2. 弱监督医学图像分割](#2-弱监督医学图像分割)
  - [3. 医学分割基础模型与结构创新](#3-医学分割基础模型与结构创新)
  - [4. 医学点云与三维重建](#4-医学点云与三维重建)
- [Part II. 医学图像检测/定位与医学图像配准](#part-ii-医学图像检测定位与医学图像配准)
  - [5. 医学图像检测/定位](#5-医学图像检测定位)
  - [6. 医学图像配准](#6-医学图像配准)
- [推荐阅读顺序](#推荐阅读顺序)
- [从旧版移除的非 A 类作品](#从旧版移除的非-a-类作品)

---

# Part I. 医学图像分割与医学点云/三维重建

## 1. 半监督医学图像分割

### 2023

**1. Bidirectional Copy-Paste for Semi-Supervised Medical Image Segmentation (BCP)**  
- **会议**：CVPR 2023 · **CCF A 类主会**  
- **方向**：半监督 / Teacher–Student  
- **核心内容**：Mean Teacher + 双向 Copy-Paste，缓解有标签/无标签图像间的数据分布差异；代表性入门论文。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2023/papers/Bai_Bidirectional_Copy-Paste_for_Semi-Supervised_Medical_Image_Segmentation_CVPR_2023_paper.pdf) · [Code](https://github.com/DeepMed-Lab-ECNU/BCP)  

**2. CauSSL: Causality-inspired Semi-supervised Learning for Medical Image Segmentation**  
- **会议**：ICCV 2023 · **CCF A 类主会**  
- **方向**：半监督 / 因果学习  
- **核心内容**：因果启发的双分支协同训练，借助 min-max 优化增强分支独立性。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/ICCV2023/papers/Miao_CauSSL_Causality-inspired_Semi-supervised_Learning_for_Medical_Image_Segmentation_ICCV_2023_paper.pdf) · [Code](https://github.com/JuzhengMiao/CauSSL)  

**3. MagicNet: Semi-Supervised Multi-Organ Segmentation via Magic-Cube Partition and Recovery**  
- **会议**：CVPR 2023 · **CCF A 类主会**  
- **方向**：半监督 / 三维器官  
- **核心内容**：将 3D CT 划分为立方体，在有/无标签样本间进行分块混合与恢复，并改进多器官伪标签。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2023/papers/Chen_MagicNet_Semi-Supervised_Multi-Organ_Segmentation_via_Magic-Cube_Partition_and_Recovery_CVPR_2023_paper.pdf) · [Code](https://github.com/DeepMed-Lab-ECNU/MagicNet)  

**4. XNet: Wavelet-Based Low and High Frequency Fusion Networks for Fully- and Semi-Supervised Semantic Segmentation of Biomedical Images**  
- **会议**：ICCV 2023 · **CCF A 类主会**  
- **方向**：全监督 + 半监督 / 频域  
- **核心内容**：以小波变换融合低频/高频表征，覆盖全监督与半监督、2D 与 3D 医学分割。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhou_XNet_Wavelet-Based_Low_and_High_Frequency_Fusion_Networks_for_Fully-_ICCV_2023_paper.pdf) · [Code](https://github.com/Yanfeng-Zhou/XNet)  

### 2024

**5. Adaptive Bidirectional Displacement for Semi-Supervised Medical Image Segmentation (ABD)**  
- **会议**：CVPR 2024 · **CCF A 类主会**  
- **方向**：半监督 / 置信度  
- **核心内容**：按预测置信度进行双向 patch 置换，并针对困难区域设计反向置信度增强。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2024/papers/Chi_Adaptive_Bidirectional_Displacement_for_Semi-Supervised_Medical_Image_Segmentation_CVPR_2024_paper.pdf) · [Code](https://github.com/chy-upc/ABD)  

**6. Constructing and Exploring Intermediate Domains in Mixed Domain Semi-supervised Medical Image Segmentation (MiDSS)**  
- **会议**：CVPR 2024 · **CCF A 类主会**  
- **方向**：跨域半监督  
- **核心内容**：通过中间域构建和伪标签指导，处理少量标注与跨中心域偏移同时存在的情况。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2024/papers/Ma_Constructing_and_Exploring_Intermediate_Domains_in_Mixed_Domain_Semi-supervised_Medical_CVPR_2024_paper.pdf) · [Code](https://github.com/MQinghe/MiDSS)  

### 2025

**7. Adaptive Learning of High-Value Regions for Semi-Supervised Medical Image Segmentation (ALHVR)**  
- **会议**：ICCV 2025 · **CCF A 类主会**  
- **方向**：半监督 / 高价值区域  
- **核心内容**：按双分支预测稳定性与可靠性划分区域，对高价值区域设计差异化学习策略。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/ICCV2025/papers/Lei_Adaptive_Learning_of_High-Value_Regions_for_Semi-Supervised_Medical_Image_Segmentation_ICCV_2025_paper.pdf) · [Code](https://github.com/ziziyao/ALHVR)  

**8. Annotation Ambiguity Aware Semi-Supervised Medical Image Segmentation (AmbiSSL)**  
- **会议**：CVPR 2025 · **CCF A 类主会**  
- **方向**：半监督 / 多标注者 / Latent  
- **核心内容**：通过随机剪枝解码器生成多样化伪标签，并学习标注歧义对应的潜在分布。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2025/papers/Kumari_Annotation_Ambiguity_Aware_Semi-Supervised_Medical_Image_Segmentation_CVPR_2025_paper.pdf)  

**9. DyCON: Dynamic Uncertainty-aware Consistency and Contrastive Learning for Semi-supervised Medical Image Segmentation**  
- **会议**：CVPR 2025 · **CCF A 类主会**  
- **方向**：半监督 / 不确定性  
- **核心内容**：结合不确定性感知一致性损失与焦点熵感知对比学习，改善 3D 病灶分割的困难区域与类别不平衡。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2025/papers/Assefa_DyCON_Dynamic_Uncertainty-aware_Consistency_and_Contrastive_Learning_for_Semi-supervised_Medical_CVPR_2025_paper.pdf) · [Code](https://github.com/CVML-KU/DyCON)  

### 2026

**10. Divide, Conquer, and Aggregate: Asymmetric Experts for Class-Imbalanced Semi-Supervised Medical Image Segmentation (DCA)**  
- **会议**：CVPR 2026 · **CCF A 类主会**  
- **方向**：半监督 / 类别不平衡  
- **核心内容**：共享编码器与非对称专家解码器分工处理头部/中部/尾部类别，通过 logit 拼接与聚合提升多器官分割。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_Divide_Conquer_and_Aggregate_Asymmetric_Experts_for_Class-Imbalanced_Semi-Supervised_Medical_CVPR_2026_paper.pdf) · [Code](https://github.com/PHPJava666/DCA)  

**11. SemiGDA: Generative Dual-distribution Alignment for Semi-Supervised Medical Image Segmentation**  
- **会议**：CVPR 2026 · **CCF A 类主会**  
- **方向**：半监督 / 双分布 Latent 对齐  
- **核心内容**：对齐图像与分割掩码的潜在特征分布，利用一致性驱动的跳跃适配器强化跨分支语义。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2026/papers/Huang_SemiGDA_Generative_Dual-distribution_Alignment_for_Semi-Supervised_Medical_Image_Segmentation_CVPR_2026_paper.pdf) · [Code](https://github.com/taozh2017/SemiGDA)  

---

## 2. 弱监督医学图像分割

### 2026

**1. Rethinking Box Supervision: Bias-Free Weakly Supervised Medical Segmentation (WeakMed)**  
- **会议**：CVPR 2026 · **CCF A 类主会**  
- **方向**：框监督 / 弱监督  
- **核心内容**：只用边界框作为训练监督；Mask-to-Box 变换和尺度一致性损失减轻框形状偏置，不依赖 GT 像素级 Mask。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2026/papers/Wei_Rethinking_Box_Supervision_Bias-Free_Weakly_Supervised_Medical_Segmentation_CVPR_2026_paper.pdf)  

---

**关于完全无监督医学分割**：本版未将缺少确认的完全无监督分割论文硬塞进 A 类清单；上面的 BCP、ABD、WeakMed 等均使用不同程度的真实标注。

---

## 3. 医学分割基础模型与结构创新

### 2022

**1. UCTransNet: Rethinking the Skip Connections in U-Net from a Channel-Wise Perspective with Transformer**  
- **会议**：AAAI 2022 · **CCF A 类主会**  
- **方向**：全监督 / 模型结构  
- **核心内容**：Channel Transformer (CCT + CCA) 改进 U-Net 跳跃连接，融合不同尺度通道语义。  
- **资源**：[**PDF 直达**](https://ojs.aaai.org/index.php/AAAI/article/view/20144/19903) · [Code](https://github.com/McGregorWwww/UCTransNet)  

### 2023

**2. Devil Is in the Queries: Advancing Mask Transformers for Real-World Medical Image Segmentation and Out-of-Distribution Localization**  
- **会议**：CVPR 2023 · **CCF A 类主会**  
- **方向**：Mask Transformer / OOD  
- **核心内容**：通过 object queries 和 query-distribution loss 同时改进病灶分割与分布外病灶定位。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2023/papers/Yuan_Devil_Is_in_the_Queries_Advancing_Mask_Transformers_for_Real-World_CVPR_2023_paper.pdf)  

### 2024

**3. SegVol: Universal and Interactive Volumetric Medical Image Segmentation**  
- **会议**：NeurIPS 2024 · **CCF A 类主会**  
- **方向**：3D 基础模型 / 提示式分割  
- **核心内容**：面向 3D CT 的通用交互分割基础模型；使用无标签和有标签 CT 预训练，并支持语义与空间提示。  
- **资源**：[**PDF 直达**](https://proceedings.neurips.cc/paper_files/paper/2024/file/c7c7cf10082e454b9662a686ce6f1b6f-Paper-Conference.pdf) · [Code](https://github.com/BAAI-DCAI/SegVol)  
- **说明**：使用无标注数据参与训练，但不是严格意义上“无监督分割”工作。  

### 2026

**4. SegMoTE: Token-Level Mixture of Experts for Medical Image Segmentation**  
- **会议**：CVPR 2026 · **CCF A 类主会**  
- **方向**：MoE / SAM 适配  
- **核心内容**：通过 token 级专家路由与渐进提示 token 化高效适配 SAM，提高跨模态的自动与交互式分割能力。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2026/papers/Lu_SegMoTE_Token-Level_Mixture_of_Experts_for_Medical_Image_Segmentation_CVPR_2026_paper.pdf)  

---

## 4. 医学点云与三维重建

### 2022

**1. SMPL-A: Modeling Person-Specific Deformable Anatomy**  
- **会议**：CVPR 2022 · **CCF A 类主会**  
- **方向**：解剖点云 / 形变建模  
- **核心内容**：利用点云自编码器与人体姿态条件建模特定患者器官变形，适用于医学解剖几何重建与估计。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2022/papers/Guo_SMPL-A_Modeling_Person-Specific_Deformable_Anatomy_CVPR_2022_paper.pdf)  

### 2025

**2. CrossSDF: 3D Reconstruction of Thin Structures From Cross-Sections**  
- **会议**：CVPR 2025 · **CCF A 类主会**  
- **方向**：医学相关 3D 表面重建  
- **核心内容**：从少量二维截面恢复三维 SDF；面向细薄结构和血管类拓扑保真，论文讨论医疗成像应用。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2025/papers/Walker_CrossSDF_3D_Reconstruction_of_Thin_Structures_From_Cross-Sections_CVPR_2025_paper.pdf)  
- **说明**：通用三维重建方法，包含医学应用背景；不属于仅在医疗数据上提出的方法。  

---

### 相关上游技术：医学内镜/眼科深度估计（不是完整 3D 重建）

- **Depth Any Endoscopy: Towards Self-Supervised Generalizable Depth Estimation in Monocular Endoscopy** — CVPR 2026（CCF A）；单目内镜自监督深度估计；作为三维重建前端深度先验使用，不等同于完整三维表面重建。 [PDF](https://openaccess.thecvf.com/content/CVPR2026/papers/Shao_Depth_Any_Endoscopy_Towards_Self-Supervised_Generalizable_Depth_Estimation_in_Monocular_CVPR_2026_paper.pdf)
- **Real2Sim2Real: RetinalDepth-64K for Depth Estimation in Posterior Segment Ophthalmic Surgery** — CVPR 2026（CCF A）；眼科术中深度估计基准和方法，为眼底三维重建及导航提供基础。 [PDF](https://openaccess.thecvf.com/content/CVPR2026/papers/Dong_Real2Sim2Real_RetinalDepth-64K_for_Depth_Estimation_in_Posterior_Segment_Ophthalmic_Surgery_CVPR_2026_paper.pdf)

**筛选说明**：旧版的 MeshDeformNet（期刊）、PX2Tooth（MICCAI）、Point2Mesh-Net（Workshop）、3DAngioNet（ISBI）、以及 MIDL 2026 超声点云方法均不符合“只要 CCF A 主会”的限制，故不进入本节正式清单。

---

# Part II. 医学图像检测/定位与医学图像配准

## 5. 医学图像检测/定位

### 2020

**1. Cross-View Correspondence Reasoning Based on Bipartite Graph Convolutional Network for Mammogram Mass Detection**  
- **会议**：CVPR 2020 · **CCF A 类主会**  
- **方向**：乳腺肿块 / 双视图推理  
- **核心内容**：双视角乳腺 X 光的二分图卷积对应关系推理与肿块检测。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Liu_Cross-View_Correspondence_Reasoning_Based_on_Bipartite_Graph_Convolutional_Network_for_CVPR_2020_paper.pdf)  

**2. FocalMix: Semi-Supervised Learning for 3D Medical Image Detection**  
- **会议**：CVPR 2020 · **CCF A 类主会**  
- **方向**：半监督 3D 检测  
- **核心内容**：3D CT 肺结节半监督检测，结合软标签与 focal 风格目标函数。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_FocalMix_Semi-Supervised_Learning_for_3D_Medical_Image_Detection_CVPR_2020_paper.pdf)  

### 2021

**3. Leveraging Large-Scale Weakly Labeled Data for Semi-Supervised Mass Detection in Mammograms**  
- **会议**：CVPR 2021 · **CCF A 类主会**  
- **方向**：弱标签 / 半监督检测  
- **核心内容**：融合弱标注数据、样本筛选与软标签损失，提高乳腺钼靶肿块检测。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2021/papers/Tang_Leveraging_Large-Scale_Weakly_Labeled_Data_for_Semi-Supervised_Mass_Detection_in_CVPR_2021_paper.pdf)  

### 2022

**4. Which Images To Label for Few-Shot Medical Landmark Detection?**  
- **会议**：CVPR 2022 · **CCF A 类主会**  
- **方向**：少样本 Landmark  
- **核心内容**：自监督表征 + Keypoint Proposal + Representative Score，筛选最值得标注的少样本模板图像。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2022/papers/Quan_Which_Images_To_Label_for_Few-Shot_Medical_Landmark_Detection_CVPR_2022_paper.pdf)  

### 2023

**5. Devil Is in the Queries: Advancing Mask Transformers for Real-World Medical Image Segmentation and Out-of-Distribution Localization**  
- **会议**：CVPR 2023 · **CCF A 类主会**  
- **方向**：OOD 病灶定位  
- **核心内容**：采用查询分布和 MaxQuery 进行医学病灶的分割与 OOD 定位；在分割与定位两个章节交叉引用。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2023/papers/Yuan_Devil_Is_in_the_Queries_Advancing_Mask_Transformers_for_Real-World_CVPR_2023_paper.pdf)  
- **说明**：与分割章节为同一论文，不重复计入唯一论文数。  

### 2024

**6. Adapting Visual-Language Models for Generalizable Anomaly Detection in Medical Images**  
- **会议**：CVPR 2024 · **CCF A 类主会**  
- **方向**：医学 VLM / 异常定位  
- **核心内容**：使用 CLIP 多层视觉特征适配和像素级视觉语言对齐，实现医学异常定位/异常分割。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2024/papers/Huang_Adapting_Visual-Language_Models_for_Generalizable_Anomaly_Detection_in_Medical_Images_CVPR_2024_paper.pdf) · [Code](https://github.com/MediaBrain-SJTU/MVFA-AD)  

---

## 6. 医学图像配准

### 2020

**1. DeepFLASH: An Efficient Network for Learning-Based Medical Image Registration**  
- **会议**：CVPR 2020 · **CCF A 类主会**  
- **方向**：低维频域 / 高效配准  
- **核心内容**：在低维带限空间学习和约束配准变换，减少计算与显存开销。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_DeepFLASH_An_Efficient_Network_for_Learning-Based_Medical_Image_Registration_CVPR_2020_paper.pdf)  

**2. Fast Symmetric Diffeomorphic Image Registration with Convolutional Neural Networks**  
- **会议**：CVPR 2020 · **CCF A 类主会**  
- **方向**：无监督 / 可微同胚  
- **核心内容**：学习前向/反向形变映射的对称可微同胚配准，强调拓扑与可逆性。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Mok_Fast_Symmetric_Diffeomorphic_Image_Registration_with_Convolutional_Neural_Networks_CVPR_2020_paper.pdf)  

### 2021

**3. Generative Adversarial Registration for Improved Conditional Deformable Templates**  
- **会议**：ICCV 2021 · **CCF A 类主会**  
- **方向**：GAN / 模板配准  
- **核心内容**：借助对抗目标生成条件形变模板，改善医学群体影像配准与模板质量。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/ICCV2021/papers/Dey_Generative_Adversarial_Registration_for_Improved_Conditional_Deformable_Templates_ICCV_2021_paper.pdf)  

### 2022

**4. Affine Medical Image Registration With Coarse-To-Fine Vision Transformer**  
- **会议**：CVPR 2022 · **CCF A 类主会**  
- **方向**：ViT / 仿射配准  
- **核心内容**：C2FViT 对 3D 医学图像进行粗到细仿射配准。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2022/papers/Mok_Affine_Medical_Image_Registration_With_Coarse-To-Fine_Vision_Transformer_CVPR_2022_paper.pdf) · [Code](https://github.com/cwmok/C2FViT)  

**5. Aladdin: Joint Atlas Building and Diffeomorphic Registration Learning With Pairwise Alignment**  
- **会议**：CVPR 2022 · **CCF A 类主会**  
- **方向**：Atlas / 可微同胚  
- **核心内容**：联合 Atlas 构建与可微同胚配准，采用成对对齐改善解剖结构一致性。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2022/papers/Ding_Aladdin_Joint_Atlas_Building_and_Diffeomorphic_Registration_Learning_With_Pairwise_CVPR_2022_paper.pdf)  

### 2023

**6. Fourier-Net: Fast Image Registration with Band-Limited Deformation**  
- **会议**：AAAI 2023 · **CCF A 类主会**  
- **方向**：Fourier / 无监督配准  
- **核心内容**：学习低维带限 Fourier 形变表示，通过无参数逆变换得到高分辨率位移场。  
- **资源**：[**PDF 直达**](https://ojs.aaai.org/index.php/AAAI/article/view/25182/24954) · [Code](https://github.com/xi-jia/Fourier-Net)  

**7. GradICON: Approximate Diffeomorphisms via Gradient Inverse Consistency**  
- **会议**：CVPR 2023 · **CCF A 类主会**  
- **方向**：逆一致性 / 形变正则  
- **核心内容**：以形变复合映射 Jacobian 的梯度逆一致性提升变形场正则性与稳定性。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2023/papers/Tian_GradICON_Approximate_Diffeomorphisms_via_Gradient_Inverse_Consistency_CVPR_2023_paper.pdf) · [Code](https://github.com/uncbiag/ICON)  

**8. Preserving Tumor Volumes for Unsupervised Medical Image Registration**  
- **会议**：ICCV 2023 · **CCF A 类主会**  
- **方向**：肿瘤体积保持 / 无监督  
- **核心内容**：先估计软肿瘤区域，再约束配准前后的肿瘤体积变化。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/ICCV2023/papers/Dong_Preserving_Tumor_Volumes_for_Unsupervised_Medical_Image_Registration_ICCV_2023_paper.pdf)  

### 2024

**9. Correlation-aware Coarse-to-fine MLPs for Deformable Medical Image Registration**  
- **会议**：CVPR 2024 · **CCF A 类主会**  
- **方向**：多窗口 MLP / 粗到细  
- **核心内容**：通过多窗口相关性感知 MLP 和由粗到细策略建模不同尺度的形变。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2024/papers/Meng_Correlation-aware_Coarse-to-fine_MLPs_for_Deformable_Medical_Image_Registration_CVPR_2024_paper.pdf)  

**10. Modality-Agnostic Structural Image Representation Learning for Deformable Multi-Modality Medical Image Registration**  
- **会议**：CVPR 2024 · **CCF A 类主会**  
- **方向**：跨模态 / 结构表征  
- **核心内容**：学习跨模态无关的结构表示，改进不同医学成像模态之间的可变形配准。  
- **资源**：[**PDF 直达**](https://openaccess.thecvf.com/content/CVPR2024/papers/Mok_Modality-Agnostic_Structural_Image_Representation_Learning_for_Deformable_Multi-Modality_Medical_Image_CVPR_2024_paper.pdf)  

---

## 推荐阅读顺序

### 医学半监督/弱监督分割（重点）

```text
BCP (CVPR 2023)          — Mean Teacher + 双向增强
    ↓
ABD (CVPR 2024)          — 伪标签置信度 + 困难区域
    ↓
ALHVR (ICCV 2025)        — 高价值区域分层学习
    ↓
DyCON (CVPR 2025)        — 不确定性一致性 + 对比学习
    ↓
AmbiSSL (CVPR 2025)      — 多解伪标签 + latent 分布
    ↓
SemiGDA (CVPR 2026)      — 图像/Mask 潜在分布对齐
    ↓
WeakMed (CVPR 2026)      — 框标注替代像素级 GT Mask
    ↓
SegMoTE (CVPR 2026)      — SAM 的 MoE 轻量适配
```

### 医学三维重建/点云

```text
SMPL-A (CVPR 2022)       — 点云自编码器 / 器官形变
    ↓
CrossSDF (CVPR 2025)     — 2D 截面 → 3D SDF
    ↓
Depth Any Endoscopy (CVPR 2026) — 内镜深度估计（上游技术）
```

### 医学检测/定位

```text
FocalMix (CVPR 2020)     — 半监督 3D 肺结节检测
    ↓
Few-Shot Landmark (CVPR 2022) — 少样本模板选择
    ↓
Devil Is in the Queries (CVPR 2023) — 病灶/OOD 定位
    ↓
Medical VLM Anomaly Detection (CVPR 2024) — 跨模态异常定位
```

### 医学图像配准

```text
Fast Symmetric / DeepFLASH (CVPR 2020) — 可微同胚 / 低维频域
    ↓
C2FViT / Aladdin (CVPR 2022)         — ViT 仿射 / Atlas
    ↓
GradICON (CVPR 2023)                — 梯度逆一致性
    ↓
Fourier-Net (AAAI 2023)             — 带限 Fourier 位移场
    ↓
Modality-Agnostic / CorrMLP (CVPR 2024) — 跨模态 / 多尺度
```

---

## 从旧版移除的非 A 类作品

以下只用于解释筛选口径，**不是本版推荐清单**：

| 旧版代表性论文 | 实际出处 | 不保留的原因 |
|---|---|---|
| UNet 3+ | ICASSP 2020 | 非 CCF A 会议 |
| PraNet | MICCAI 2020 | 非所要求的 CCF A 会议 |
| Medical Transformer / CoTr | MICCAI 2021 | 非所要求的 CCF A 会议 |
| Swin-Unet | ECCV Workshop 2022 | Workshop；不能视为 CCF A 主会 |
| UNETR | WACV 2022 | 非 CCF A 会议 |
| SegMamba / FastSAM3D / Tri-Plane Mamba | MICCAI 2024 | 非所要求的 CCF A 会议 |
| PX2Tooth | MICCAI 2024 | 非所要求的 CCF A 会议 |
| Check and Link / DiffuseMorph | ECCV 2022 | CCF B，不符合只要 A 类 |
| Adaptive Correspondence Scoring / Unsupervised Multi-modal Registration via Invertible Translation | ECCV 2024 | CCF B，不符合只要 A 类 |
| MedSAM / nnU-Net / TransMorph / MeshDeformNet | 期刊 | 不是会议主会论文 |
| Real-Time Novel-View Freehand Ultrasound Imaging via Point-Cloud Rendering and Diffusion-Bridge Completion | MIDL 2026 | 不是 CCF A 主会；PMLR 出版不等于 ICML |

---

**统计**：正式清单 34 条主题记录，去重后 **33 篇** CCF A 类主会论文；另列 2 篇严格 A 类、但只作为三维重建上游技术的工作。

**学术用途提示**：如用于毕业/奖学金/职称认定，仍应按所在单位实际采纳的 CCF 目录版本确认。
