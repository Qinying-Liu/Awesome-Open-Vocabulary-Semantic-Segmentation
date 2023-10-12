# Awesome-Open-Vocabulary-Semantic-Segmentation
A curated publication list on open vocabulary semantic segmentation.

This repository was built to facilitate navigating the mainstream on open vocabulary semantic segmentation.  

The project is ongoing!

##

## Fully-supervised open-vocabulary segmentation
The model is trained on full-supervised semantic segmentation datasets with pixel-level annotations (e.g., COCO Stuff dataset).

1. <span id = "1001">**[LSeg]**</span> | **ICLR'22** | Language-driven Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2201.03546) | [`[code]`](https://github.com/isl-org/lang-seg)
2. <span id = "1001">**[ZegFormer]**</span> | **CVPR'22** | ZegFormer: Decoupling Zero-Shot Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2112.07910) | [`[code]`](https://github.com/dingjiansw101/ZegFormer)
3. <span id = "1002">**[OpenSeg]**</span> | **ECCV'22** | Scaling Open-vocabulary Image Segmentation with Image-level Labels | [`[pdf]`](https://arxiv.org/abs/2112.12143) | [`[code]`](https://github.com/tensorflow/tpu/tree/641c1ac6e26ed788327b973582cbfa297d7d31e7/models/official/detection/projects/openseg)
4. <span id = "1003">**[Xu et al.]**</span> | **ECCV'22** | A Simple Baseline for Open-Vocabulary Semantic Segmentation with Pre-trained Vision-language Model | [`[pdf]`](https://arxiv.org/abs/2112.14757) | [`[code]`](https://github.com/MendelXu/zsseg.baseline)
6. <span id = "1003">**[SegCLIP]**</span> | **ICML'23** | SegCLIP: Patch Aggregation with Learnable Centers for Open-Vocabulary Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2211.14813) | [`[code]`](https://github.com/ArrowLuo/SegCLIP)
7. <span id = "1003">**[OVSeg]**</span> | **CVPR'23** | Open-Vocabulary Semantic Segmentation with Mask-adapted CLIP | [`[pdf]`](https://arxiv.org/abs/2210.04150) | [`[code]`](https://github.com/facebookresearch/ov-seg)
9. <span id = "1003">**[X-Decoder]**</span> | **CVPR'23** | Generalized Decoding for Pixel, Image, and Language | [`[pdf]`](https://arxiv.org/abs/2212.11270) | [`[code]`](https://github.com/microsoft/X-Decoder)
10. <span id = "1003">**[SAN]**</span> | **CVPR'23(Highlight)** | Side Adapter Network for Open-Vocabulary Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2302.12242) | [`[code]`](https://github.com/MendelXu/SAN)
11. <span id = "1003">**[SAN]**</span> | **TAPMI'23** | SAN: Side Adapter Network for Open-vocabulary Semantic Segmentation | [`[pdf]`](https://ieeexplore.ieee.org/abstract/document/10238837) | [`[code]`](https://github.com/MendelXu/SAN)
9. <span id = "1003">**[ODISE]**</span> | **CVPR'23** | Open-Vocabulary Panoptic Segmentation with Text-to-Image Diffusion Models | [`[pdf]`](https://arxiv.org/abs/2303.04803) | [`[code]`](https://github.com/NVlabs/ODISE)
10. <span id = "1003">**[FreeSeg]**</span> | **CVPR'23** | FreeSeg: Unified, Universal and Open-Vocabulary Image Segmentation | [`[pdf]`](https://arxiv.org/abs/2303.17225) | [`[code]`](https://github.com/bytedance/FreeSeg)
11. <span id = "1003">**[CAT-Seg]**</span> | **Arxiv'23** | CAT-Seg : Cost Aggregation for Open-Vocabulary Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2303.11797) | [`[code]`](https://github.com/KU-CVLAB/CAT-Seg)
12. <span id = "1003">**[ADA]**</span> | **Arxiv'23** | Open-Vocabulary Semantic Segmentation via Attribute Decomposition-Aggregation | [`[pdf]`](https://arxiv.org/abs/2309.00096)
13. <span id = "1003">**[HIPIE]**</span> | **NIPS'23** | Hierarchical Open-vocabulary Universal Image Segmentation | [`[pdf]`](https://arxiv.org/abs/2307.00764) | [`[code]`](https://github.com/berkeley-hipie/HIPIE)
14. <span id = "1003">**[FC-CLIP]**</span> | **NIPS'23** | Convolutions Die Hard: Open-Vocabulary Segmentation with Single Frozen Convolutional CLIP | [`[pdf]`](https://arxiv.org/abs/2308.02487) | [`[code]`](https://github.com/bytedance/fc-clip)
15. <span id = "1003">**[OpenSeeD]**</span> | **ICCV'23** | A Simple Framework for Open-Vocabulary Segmentation and Detection | [`[pdf]`](https://arxiv.org/abs/2303.08131) | [`[code]`](https://github.com/IDEA-Research/OpenSeeD)
16. <span id = "1003">**[GKC]**</span> | **ICCV'23** | Global Knowledge Calibration for Fast Open-Vocabulary Segmentation | [`[pdf]`](https://arxiv.org/pdf/2303.09181)
17. <span id = "1003">**[OPSNet]**</span> | **ICCV'23** | Open-vocabulary Panoptic Segmentation with Embedding Modulation | [`[pdf]`](https://arxiv.org/abs/2303.11324) | [`[code]`](https://github.com/XavierCHEN34/OPSNet)

##

## Weakly-supervised open-vocabulary segmentation
The model is trained on weakly-supervised datasets with only image-level annotations/captions (e.g., CC12M dataset).

1. <span id = "2001">**[GroupViT]**</span> | **CVPR'22** | GroupViT: Semantic Segmentation Emerges from Text Supervision | [`[pdf]`](https://arxiv.org/abs/2202.11094) | [`[code]`](https://github.com/NVlabs/GroupViT)
2. <span id = "2002">**[ViL-Seg]**</span> | **ECCV'22** | Open-world Semantic Segmentation via Contrasting and Clustering Vision-Language Embedding | [`[pdf]`](https://arxiv.org/abs/2207.08455)
3. <span id = "2003">**[MaskCLIP+]**</span> | **ECCV'22(Oral)** | Extract Free Dense Labels from CLIP | [`[pdf]`](https://arxiv.org/abs/2112.01071)  | [`[code]`](https://github.com/chongzhou96/MaskCLIP)
4. <span id = "2006">**[ViewCo]**</span> | **ICLR'23** | Viewco: Discovering Text-supervised Segmentation Masks via Multi-view semantic Consistency | [`[pdf]`](https://arxiv.org/abs/2302.10307)
5. <span id = "2004">**[SegCLIP]**</span> | **ICML'23** | SegCLIP: Patch Aggregation with Learnable Centers for Open-Vocabulary Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2211.14813) | [`[code]`](https://github.com/ArrowLuo/SegCLIP)
6. <span id = "2005">**[CLIP-S4]**</span> | **CVPR'23** | CLIP-S4: Language-Guided Self-Supervised Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2305.01040)
7. <span id = "2005">**[PACL]**</span> | **CVPR'23** | Open Vocabulary Semantic Segmentation with Patch Aligned Contrastive Learning | [`[pdf]`](https://arxiv.org/abs/2212.04994)
8. <span id = "2005">**[OVSegmentor]**</span> | **CVPR'23** | Learning Open-vocabulary Semantic Segmentation Models From Natural Language Supervision | [`[pdf]`](https://arxiv.org/abs/2301.09121) | [`[code]`](https://github.com/Jazzcharles/OVSegmentor)
9. <span id = "2005">**[SimSeg]**</span> | **CVPR'23** | A Simple Framework for Text-Supervised Semantic Segmentation | [`[pdf]`](https://openaccess.thecvf.com/content/CVPR2023/html/Yi_A_Simple_Framework_for_Text-Supervised_Semantic_Segmentation_CVPR_2023_paper.html) | [`[code]`](https://github.com/muyangyi/SimSeg)
10. <span id = "2005">**[TCL]**</span> | **CVPR'23** | Learning to Generate Text-grounded Mask for Open-world Semantic Segmentation from Only Image-Text Pairs | [`[pdf]`](https://arxiv.org/abs/2212.00785) | [`[code]`](https://github.com/kakaobrain/tcl)
11. <span id = "2005">**[ZeroSeg]**</span> | **CVPR'23** | Exploring Open-Vocabulary Semantic Segmentation from CLIP Vision Encoder Distillation Only | [`[pdf]`](https://openaccess.thecvf.com/content/ICCV2023/html/Chen_Exploring_Open-Vocabulary_Semantic_Segmentation_from_CLIP_Vision_Encoder_Distillation_Only_ICCV_2023_paper.html)
13. <span id = "2005">**[CLIPpy]**</span> | **ICCV'23** | Perceptual Grouping in Contrastive Vision-Language Models | [`[pdf]`](https://arxiv.org/abs/2210.09996) | [`[code]`](https://github.com/kakaobrain/tcl)
14. <span id = "2005">**[MixReorg]**</span> | **ICCV'23** | MixReorg: Cross-Modal Mixed Patch Reorganization is a Good Mask Learner for Open-World Semantic Segmentation | [`[pdf]`](https://openaccess.thecvf.com/content/ICCV2023/html/Cai_MixReorg_Cross-Modal_Mixed_Patch_Reorganization_is_a_Good_Mask_Learner_ICCV_2023_paper.html)
15. <span id = "2005">**[Zhang et al.]**</span> | **Arxiv'23** | Associating Spatially-Consistent Grouping with Text-supervised Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2304.01114)
16. <span id = "2005">**[Zhang et al.]**</span> | **Arxiv'23** | SimCon Loss with Multiple Views for Text Supervised Semantic Segmentation | [`[pdf]`](https://browse.arxiv.org/abs/2302.03432) 
17. <span id = "2005">**[CoCu]**</span> | **NeurIPS'23** | Bridging Semantic Gaps for Language-Supervised Semantic Segmentation | [`[pdf]`](https://arxiv.org/abs/2309.13505) | [`[code]`](https://github.com/xing0047/CoCu)



##

## Training-free open-vocabulary segmentation
The model is modified from the off-the-shelf large models (e.g., CLIP, Diffusion models) without an additional training phase.

1. <span id = "3001">**[MaskCLIP]**</span> | **ECCV'22(Oral)** | Extract Free Dense Labels from CLIP | [`[pdf]`](https://arxiv.org/abs/2112.01071)  | [`[code]`](https://github.com/chongzhou96/MaskCLIP)
2. <span id = "3001">**[CLIP Surgery]**</span> | **Arxiv'23** | CLIP Surgery for Better Explainability with Enhancement in Open-Vocabulary Tasks | [`[pdf]`](https://arxiv.org/abs/2304.05653) | [`[code]`](https://github.com/xmed-lab/CLIP_Surgery)
3. <span id = "3001">**[OVDiff]**</span> | **Arxiv'23** | Diffusion Models for Zero-Shot Open-Vocabulary Segmentation | [`[pdf]`](https://arxiv.org/abs/2306.09316)
4. <span id = "3001">**[CLIP-DIY]**</span> | **Arxiv'23** | CLIP-DIY: CLIP Dense Inference Yields Open-Vocabulary Semantic Segmentation For-Free | [`[pdf]`](https://arxiv.org/abs/2309.14289)
5. <span id = "3001">**[DiffSegmenter]**</span> | **Arxiv'23** | Diffusion Model is Secretly a Training-free Open Vocabulary Semantic Segmenter | [`[pdf]`](https://arxiv.org/abs/2309.02773)





## Feedback

If you find this project helpful, please consider giving it a star. 

If you have any suggestions or find missing papers, please don't hesitate to contact me.

- [e-mail](mailto:lydyc@mail.ustc.edu.cn)
- [pull request](https://github.com/Qinying-Liu/Awesome-Open-Vocabulary-Semantic-Segmentation/pulls)
