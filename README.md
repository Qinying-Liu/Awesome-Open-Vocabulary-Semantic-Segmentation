# Awesome-Open-Vocabulary-Semantic-Segmentation
A curated publication list on awesome open vocabulary semantic segmentation.

This repository was built to facilitate navigating the mainstream on open vocabulary semantic segmentation.  

##

## Table of Contents
- [Performance Tables](#performance-tables)
  - [THUMOS14](#thumos14)
  - [ActivityNet1.2](#activitynet12)
  - [ActivityNet1.3](#activitynet13)
  - [FineAction](#fineaction)
  - [FineGym](#finegym)
- [Paper List](#paper-list)
- [Feedback](#feedback)

##

## Performance Tables
The mean average precisions (mAPs) under the standard intersection over union (IoU) thresholds are reported.
For example, '@0.5' indicates the mAP score at the IoU threshold of 0.5.  
The AVG denotes the average mAP under the IoU thresholds from 0.1 to 0.7 (for THUMOS14), from 0.1 to 0.5 (for FineGym), or from 0.5 to 0.95 with a step size of 0.05 (for ActivityNet both versions and FineAction).

In addition, links to the implementations are attached with their framework specification if available. 'o-' and 'u-' indicate the official and the unofficial implementations, respectively.

\[Note\] <br/>
*: use of additional trimmed videos <br/>
&dagger;: use of additional information such as action count, pose, audio, and a large vision-language model

##

### THUMOS14

| ID | Year | Venue |   Model<br/>(or Authors)   |  @0.1   |  @0.2   |  @0.3   |  @0.4   |  @0.5   |  @0.6   |  @0.7   |   AVG   |  code  |
|:--:|:----:|:-----:|:--------------------------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:------:|
| 1  | 2017 | CVPR  | [UntrimmedNets](#1001)     |  44.4   |  37.7   |  28.2   |  21.1   |  13.7   |    -    |    -    |    -    |[`[o-matlab]`](https://github.com/wanglimin/UntrimmedNet)|
| 2  | 2017 | ICCV  | [Hide-and-seek](#1002)     |  36.4   |  27.8   |  19.5   |  12.7   |   6.8   |    -    |    -    |    -    |[`[o-torch]`](https://github.com/kkanshul/Hide-and-Seek)|
| 3  | 2018 | CVPR  | [STPN](#1003)              |  52.0   |  44.7   |  35.5   |  25.8   |  16.9   |   9.9   |   4.3   |  27.0   |[`[u-tensorflow]`](https://github.com/bellos1203/STPN)|
| 4  | 2018 | ECCV  | [AutoLoc](#1004)           |    -    |    -    |  35.8   |  29.0   |  21.2   |  13.4   |   5.8   |    -    |[`[o-caffe]`](https://github.com/zhengshou/AutoLoc)|
| 5  | 2018 | ECCV  | [W-TALC](#1005)            |  55.2   |  49.6   |  40.1   |  31.1   |  22.8   |    -    |   7.6   |    -    |[`[o-pytorch]`](https://github.com/sujoyp/wtalc-pytorch)<br/>[`[o-tensorflow]`](https://github.com/sujoyp/wtalc-tensorflow)|
| 6  | 2018 | MM    | [Zhong et al.](#1006)      |  45.8   |  39.0   |  31.1   |  22.5   |  15.9   |    -    |    -    |    -    |        |
| 7  | 2019 | AAAI  | [TSRNet\*](#1007)          |  55.9   |  46.9   |  38.3   |  28.1   |  18.6   |  11.0   |   5.6   |  29.2   |        |
| 8  | 2019 | AAAI  | [STAR&dagger;](#1008)      |  68.8   |  60.0   |  48.7   |  34.7   |  23.0   |    -    |    -    |    -    |        |
| 9  | 2019 | ICLR  | [MAAN](#1009)              |  59.8   |  50.8   |  41.1   |  30.6   |  20.3   |  12.0   |   6.9   |  31.6   |[`[o-pytorch]`](https://github.com/yyuanad/MAAN)|
| 10 | 2019 | CVPR  | [Liu et al.](#1010)        |  57.4   |  50.8   |  41.2   |  32.1   |  23.1   |  15.0   |   7.0   |  32.4   |[`[o-pytorch]`](https://github.com/Finspire13/CMCS-Temporal-Action-Localization)|
| 11 | 2019 | ICIP  | [Park et al.](#1011)       |    -    |    -    |  40.2   |  32.2   |  21.7   |    -    |   9.2   |    -    |        |
| 12 | 2019 | ICIP  | [ACN](#1012)               |    -    |    -    |  35.9   |  30.7   |  24.2   |  15.7   |   7.4   |    -    |        |
| 13 | 2019 | MM    | [ASSG](#1013)              |  65.6   |  59.4   |  50.4   |  38.7   |  25.4   |  15.0   |   6.6   |  37.3   |        |
| 14 | 2019 | ICCV  | [CleanNet](#1014)          |    -    |    -    |  37.0   |  30.9   |  23.9   |  13.9   |   7.1   |    -    |        |
| 15 | 2019 | ICCV  | [TSM](#1015)               |    -    |    -    |  39.5   |    -    |  24.5   |    -    |   7.1   |    -    |        |
| 16 | 2019 | ICCV  | [3C-Net&dagger;](#1016)    |  59.1   |  53.5   |  44.2   |  34.1   |  26.6   |    -    |   8.1   |    -    |[`[o-pytorch]`](https://github.com/naraysa/3c-net)|
| 17 | 2019 | ICCV  | [Nguyen et al.](#1017)     |  60.4   |  56.0   |  46.6   |  37.5   |  26.8   |  17.6   |   9.0   |  36.3   |        |
| 18 | 2020 | AAAI  | [PreTrimNet&dagger;](#1018)|  57.5   |  50.7   |  41.4   |  32.1   |  23.1   |  14.2   |   7.7   |  32.4   |        |
| 19 | 2020 | AAAI  | [BaS-Net](#1019)           |  58.2   |  52.3   |  44.6   |  36.0   |  27.0   |  18.6   |  10.4   |  35.3   |[`[o-pytorch]`](https://github.com/Pilhyeon/BaSNet-pytorch)|
| 20 | 2020 | AAAI  | [RPN](#1020)               |  62.3   |  57.0   |  48.2   |  37.2   |  27.9   |  16.7   |   8.1   |  36.8   |        |
| 21 | 2020 | WACV  | [WSGN](#1021)              |  57.9   |  51.2   |  42.0   |  33.1   |  25.1   |  16.7   |   8.9   |  33.6   |        |
| 22 | 2020 | WACV  | [Islam and Radke](#1022)   |  62.3   |    -    |  46.8   |    -    |  29.6   |    -    |   9.7   |    -    |[`[o-pytorch]`](https://github.com/asrafulashiq/wsad)|
| 23 | 2020 | WACV  | [Rashid et al.](#1023)     |  63.7   |  56.9   |  47.3   |  36.4   |  26.1   |    -    |    -    |    -    |[`[o-pytorch]`](https://github.com/menorashid/action_graphs)|
| 24 | 2020 | CVPR  | [ActionBytes](#1024)       |    -    |    -    |  43.0   |  35.8   |  29.0   |    -    |   9.5   |    -    |        |
| 25 | 2020 | CVPR  | [DGAM](#1025)              |  60.0   |  54.2   |  46.8   |  38.2   |  28.8   |  19.8   |  11.4   |  37.0   |[`[o-pytorch]`](https://github.com/bfshi/DGAM-Weakly-Supervised-Action-Localization)|
| 26 | 2020 | CVPR  | [Gong et al.](#1026)       |    -    |    -    |  46.9   |  38.9   |  30.1   |  19.8   |  10.4   |    -    |[`[o-pytorch]`](https://github.com/GGQ1996/action_co_localization/tree/master/ACL_Anet_release)|
| 27 | 2020 | ECCV  | [EM-MIL](#1027)            |  59.1   |  52.7   |  45.5   |  36.8   |  30.5   |  22.7   |  16.4   |  37.7   |[`[o-pytorch]`](https://github.com/airmachine/EM-MIL-WeaklyActionDetection)|
| 28 | 2020 | ECCV  | [A2CL-PT](#1028)           |  61.2   |  56.1   |  48.1   |  39.0   |  30.1   |  19.2   |  10.6   |  37.8   |[`[o-pytorch]`](https://github.com/MichiganCOG/A2CL-PT)|
| 29 | 2020 | ECCV  | [TSCN](#1029)              |  63.4   |  57.6   |  47.8   |  37.7   |  28.7   |  19.4   |  10.2   |  37.8   |        |
| 30 | 2020 | MM    | [ACM-BANet](#1030)         |  64.6   |  57.7   |  48.9   |  40.9   |  32.3   |  21.9   |  13.5   |  40.0   |        |
| 31 | 2021 | WACV  | [RefineLoc](#1031)         |    -    |    -    |  40.8   |  32.7   |  23.1   |  13.3   |   5.3   |    -    |[`[o-pytorch]`](https://github.com/HumamAlwassel/RefineLoc)|
| 32 | 2021 | AAAI  | [Liu et al.](#1032)        |    -    |    -    |  50.8   |  41.7   |  29.6   |  20.1   |  10.7   |    -    |        |
| 33 | 2021 | AAAI  | [ACSNet](#1033)            |    -    |    -    |  51.4   |  42.7   |  32.4   |  22.0   |  11.7   |    -    |        |
| 34 | 2021 | AAAI  | [HAM-Net](#1034)           |  65.9   |  59.6   |  52.2   |  43.1   |  32.6   |  21.9   |  12.5   |  41.1   |[`[o-pytorch]`](https://github.com/asrafulashiq/hamnet)|
| 35 | 2021 | AAAI  | [Lee et al.](#1035)        |  67.5   |  61.2   |  52.3   |  43.4   |  33.7   |  22.9   |  12.1   |  41.9   |[`[o-pytorch]`](https://github.com/Pilhyeon/WTAL-Uncertainty-Modeling)|
| 37 | 2021 | CVPR  | [ASL](#1037)               |  67.0   |    -    |  51.8   |    -    |  31.1   |    -    |  11.4   |    -    |[`[o-pytorch]`](https://github.com/layer6ai-labs/ASL)|
| 38 | 2021 | CVPR  | [CoLA](#1038)              |  66.2   |  59.5   |  51.5   |  41.9   |  32.2   |  22.0   |  13.1   |  40.9   |[`[o-pytorch]`](https://github.com/zhang-can/CoLA)|
| 39 | 2021 | CVPR  | [AUMN](#1039)              |  66.2   |  61.9   |  54.9   |  44.4   |  33.3   |  20.5   |   9.0   |  41.5   |        |
| 40 | 2021 | CVPR  | [TS-PCA](#1040)            |  67.6   |  61.1   |  53.4   |  43.4   |  34.3   |  24.7   |  13.7   |  42.6   |        |
| 41 | 2021 | CVPR  | [UGCT](#1041)              |  69.2   |  62.9   |  55.5   |  46.5   |  35.9   |  23.8   |  11.4   |  43.6   |        |
| 42 | 2021 | ICCV  | [D2-Net](#1042)            |  65.7   |  60.2   |  52.3   |  43.4   |  36.0   |    -    |    -    |    -    |[`[o-pytorch]`](https://github.com/naraysa/D2-Net)|
| 43 | 2021 | ICCV  | [FAC-Net](#1043)           |  67.6   |  62.1   |  52.6   |  44.3   |  33.4   |  22.5   |  12.7   |  42.2   |[`[o-pytorch]`](https://github.com/LeonHLJ/FAC-Net)|
| 44 | 2021 | MM    | [CSCL](#1044)              |  68.0   |  61.8   |  52.7   |  43.3   |  33.4   |  21.8   |  12.3   |  41.9   |        |
| 45 | 2021 | MM    | [CO<sub>2</sub>-Net](#1045)|  70.1   |  63.6   |  54.5   |  45.7   |  38.3   |  26.4   |  13.4   |  44.6   |[`[o-pytorch]`](https://github.com/harlanhong/MM2021-CO2-Net)|
| 46 | 2022 | AAAI  | [ACGNet](#1046)            |  68.1   |  62.6   |  53.1   |  44.6   |  34.7   |  22.6   |  12.0   |  42.5   |        |
| 47 | 2022 | CVPR  | [FTCL](#1047)              |  69.6   |  63.4   |  55.2   |  45.2   |  35.6   |  23.7   |  12.2   |  43.6   |[`[o-pytorch]`](https://github.com/MengyuanChen21/CVPR2022-FTCL)|
| 48 | 2022 | CVPR  | [DCC](#1048)               |  69.0   |  63.8   |  55.9   |  45.9   |  35.7   |  24.3   |  13.7   |  44.0   |        |
| 49 | 2022 | CVPR  | [Huang et al.](#1049)      |  71.3   |  65.3   |  55.8   |  47.5   |  38.2   |  25.4   |  12.5   |  45.1   |[`[o-pytorch]`](https://github.com/LeonHLJ/RSKP)|
| 50 | 2022 | CVPR  | [ASM-Loc](#1050)           |  71.2   |  65.5   |  57.1   |  46.8   |  36.6   |  25.2   |  13.4   |  45.1   |[`[o-pytorch]`](https://github.com/boheumd/ASM-Loc)|
| 51 | 2022 | MM    | [DGCNN](#1051)             |  66.3   |  59.9   |  52.3   |  43.2   |  32.8   |  22.1   |  13.1   |  41.3   |        |
| 52 | 2022 | MM    | [Li et al.](#1052)         |  69.7   |  64.5   |  58.1   |  49.9   |  39.6   |  27.3   |  14.2   |  46.1   |        |
| 54 | 2022 | ECCV  | [DELU](#1054)              |  71.5   |  66.2   |  56.5   |  47.7   |  40.5   |  27.2   |  15.3   |  46.4   |[`[o-pytorch]`](https://github.com/MengyuanChen21/ECCV2022-DELU)|
| 55 | 2023 | WACV  | [TFE-DCN](#1055)           |  72.3   |  66.5   |  58.6   |  49.5   |  40.7   |  27.1   |  13.7   |  46.9   |[`[o-pytorch]`](https://github.com/jianxiong-zhou/TFE-DCN)|
| 56 | 2023 | CVPR  | [Wang et al.](#1056)       |  73.0   |  68.2   |  60.0   |  47.9   |  37.1   |  24.4   |  12.7   |  46.2   |        |
| 57 | 2023 | CVPR  | [Li et al.](#1057)         |    -    |    -    |  56.2   |  47.8   |  39.3   |  27.5   |  15.2   |    -    |[`[o-pytorch]`](https://github.com/lgzlIlIlI/Boosting-WTAL)|
| 58 | 2023 | CVPR  | [Ren et al.](#1058)        |  71.8   |  67.5   |  58.9   |  49.0   |  40.0   |  27.1   |  15.1   |  47.0   |[`[o-pytorch]`](https://github.com/RenHuan1999/CVPR2023_P-MIL)|
| 59 | 2023 | CVPR  | [Zhou et al.](#1059)       |  74.0   |  69.4   |  60.7   |  51.8   |  42.7   |  26.2   |  13.1   |  48.3   |[`[o-pytorch]`](https://github.com/zhou745/GauFuse_WSTAL)|
| 60 | 2023 | CVPR  | [Ju et al.&dagger;](#1060) |  73.5   |  68.8   |  61.5   |**53.8** |  42.0   |  29.4   |**16.8** |  49.4   |        |
| 61 | 2023 | CVPR  | [PivoTAL](#1061)           |**74.1** |**69.6** |**61.7** |  52.1   |**42.8** |**30.6** |  16.7   |**49.6** |        |

##

### ActivityNet1.2

| ID | Year | Venue |   Model<br/>(or Authors)   |  @0.5   |  @0.75  |  @0.95  |   AVG   |  code  |
|:--:|:----:|:-----:|:--------------------------:|:-------:|:-------:|:-------:|:-------:|:------:|
| 4  | 2018 | ECCV  | [AutoLoc](#1004)           |  27.3   |  15.1   |   3.3   |  16.0   |[`[o-caffe]`](https://github.com/zhengshou/AutoLoc)|
| 5  | 2018 | ECCV  | [W-TALC](#1005)            |  37.0   |    -    |    -    |  18.0   |[`[o-pytorch]`](https://github.com/sujoyp/wtalc-pytorch)<br/>[`[o-tensorflow]`](https://github.com/sujoyp/wtalc-tensorflow)|
| 6  | 2018 | MM    | [Zhong et al.](#1006)      |  27.3   |  14.7   |   2.9   |  15.6   |        |
| 10 | 2019 | CVPR  | [Liu et al.](#1010)        |  36.8   |  22.0   |   5.6   |  22.4   |[`[o-pytorch]`](https://github.com/Finspire13/CMCS-Temporal-Action-Localization)|
| 11 | 2019 | ICIP  | [Park et al.](#1011)       |  33.7   |    -    |    -    |    -    |        |
| 12 | 2019 | ICIP  | [ACN](#1012)               |  30.4   |  15.4   |   3.7   |  17.0   |        |
| 14 | 2019 | ICCV  | [CleanNet](#1014)          |  37.1   |  20.3   |   5.0   |  21.6   |        |
| 15 | 2019 | ICCV  | [TSM](#1015)               |  28.3   |  17.0   |   3.5   |  17.1   |        |
| 16 | 2019 | ICCV  | [3C-Net&dagger;](#1016)    |  37.2   |    -    |    -    |  21.7   |[`[o-pytorch]`](https://github.com/naraysa/3c-net)|
| 19 | 2020 | AAAI  | [BaS-Net](#1019)           |  38.5   |  24.2   |   5.6   |  24.3   |[`[o-pytorch]`](https://github.com/Pilhyeon/BaSNet-pytorch)|
| 20 | 2020 | AAAI  | [RPN](#1020)               |  37.6   |  23.9   |   5.4   |  23.3   |        |
| 22 | 2020 | WACV  | [Islam and Radke](#1022)   |  35.2   |    -    |    -    |    -    |[`[o-pytorch]`](https://github.com/asrafulashiq/wsad)|
| 23 | 2020 | WACV  | [Rashid et al.](#1023)     |  29.4   |    -    |    -    |    -    |[`[o-pytorch]`](https://github.com/menorashid/action_graphs)|
| 24 | 2020 | CVPR  | [ActionBytes](#1024)       |  39.4   |    -    |    -    |    -    |        |
| 25 | 2020 | CVPR  | [DGAM](#1025)              |  41.0   |  23.5   |   5.3   |  24.4   |[`[o-pytorch]`](https://github.com/bfshi/DGAM-Weakly-Supervised-Action-Localization)|
| 26 | 2020 | CVPR  | [Gong et al.](#1026)       |  40.0   |  25.0   |   4.6   |  24.6   |[`[o-pytorch]`](https://github.com/GGQ1996/action_co_localization/tree/master/ACL_Anet_release)|
| 27 | 2020 | ECCV  | [EM-MIL](#1027)            |  37.4   |    -    |    -    |  20.3   |[`[o-pytorch]`](https://github.com/airmachine/EM-MIL-WeaklyActionDetection)|
| 29 | 2020 | ECCV  | [TSCN](#1029)              |  37.6   |  23.7   |   5.7   |  23.6   |        |
| 31 | 2021 | WACV  | [RefineLoc](#1031)         |  38.7   |  22.6   |   5.5   |  23.2   |[`[o-pytorch]`](https://github.com/HumamAlwassel/RefineLoc)|
| 32 | 2021 | AAAI  | [Liu et al.](#1032)        |  39.2   |  25.6   | **6.8** |  25.5   |        |
| 33 | 2021 | AAAI  | [ACSNet](#1033)            |  40.1   |  26.1   | **6.8** |  26.0   |        |
| 34 | 2021 | AAAI  | [HAM-Net](#1034)           |  41.0   |  24.8   |   5.3   |  25.1   |[`[o-pytorch]`](https://github.com/asrafulashiq/hamnet)|
| 35 | 2021 | AAAI  | [Lee et al.](#1035)        |  41.2   |  25.6   |   6.0   |  25.9   |[`[o-pytorch]`](https://github.com/Pilhyeon/WTAL-Uncertainty-Modeling)|
| 36 | 2021 | ICLR  | [Lee et al.&dagger;](#1036)|  44.8   |  26.7   |   1.0   |  26.0   |        |
| 37 | 2021 | CVPR  | [ASL](#1037)               |  40.2   |    -    |    -    |  25.8   |[`[o-pytorch]`](https://github.com/layer6ai-labs/ASL)|
| 38 | 2021 | CVPR  | [CoLA](#1038)              |  42.7   |  25.7   |   5.8   |  26.1   |[`[o-pytorch]`](https://github.com/zhang-can/CoLA)|
| 39 | 2021 | CVPR  | [AUMN](#1039)              |  42.0   |  25.0   |   5.6   |  25.5   |        |
| 41 | 2021 | CVPR  | [UGCT](#1041)              |  41.8   |  25.3   |   5.9   |  25.8   |        |
| 42 | 2021 | ICCV  | [D2-Net](#1042)            |  42.3   |  25.5   |   5.8   |  26.0   |[`[o-pytorch]`](https://github.com/naraysa/D2-Net)|
| 44 | 2021 | MM    | [CSCL](#1044)              |  43.8   |  26.9   |   5.6   |  26.9   |        |
| 45 | 2021 | MM    | [CO<sub>2</sub>-Net](#1045)|  43.3   |  26.3   |   5.2   |  26.4   |[`[o-pytorch]`](https://github.com/harlanhong/MM2021-CO2-Net)|
| 46 | 2022 | AAAI  | [ACGNet](#1046)            |  41.8   |  26.0   |   5.9   |  26.1   |        |
| 51 | 2022 | MM    | [DGCNN](#1051)             |  42.0   |  25.8   |   6.0   |  26.2   |        |
| 52 | 2022 | MM    | [Li et al.](#1052)         |  41.6   |  24.8   |   5.4   |  25.2   |        |
| 54 | 2022 | ECCV  | [DELU](#1054)              |  44.2   |  26.7   |   5.4   |  26.9   |[`[o-pytorch]`](https://github.com/MengyuanChen21/ECCV2022-DELU)|
| 58 | 2023 | CVPR  | [Ren et al.](#1058)        |  44.2   |  26.1   |   5.3   |  26.5   |[`[o-pytorch]`](https://github.com/RenHuan1999/CVPR2023_P-MIL)|
| 60 | 2023 | CVPR  | [Ju et al.&dagger;](#1060) |**48.3** |**29.3** |   6.1   |**29.6** |        |

##

### ActivityNet1.3

| ID | Year | Venue |   Model<br/>(or Authors)   |  @0.5   |  @0.75  |  @0.95  |   AVG   |  code  |
|:--:|:----:|:-----:|:--------------------------:|:-------:|:-------:|:-------:|:-------:|:------:|
| 3  | 2018 | CVPR  | [STPN](#1003)              |  29.3   |  16.9   |   2.6   |    -    |[`[u-tensorflow]`](https://github.com/bellos1203/STPN)|
| 7  | 2019 | AAAI  | [TSRNet*](#1007)           |  33.1   |  18.7   |   3.3   |  21.8   |        |
| 8  | 2019 | AAAI  | [STAR&dagger;](#1008)      |  31.1   |  18.8   |   4.7   |    -    |        |
| 9  | 2019 | ICLR  | [MAAN](#1009)              |  33.7   |  21.9   |   5.5   |    -    |[`[o-pytorch]`](https://github.com/yyuanad/MAAN)|
| 10 | 2019 | CVPR  | [Liu et al.](#1010)        |  34.0   |  20.9   |   5.7   |  21.2   |[`[o-pytorch]`](https://github.com/Finspire13/CMCS-Temporal-Action-Localization)|
| 13 | 2019 | MM    | [ASSG](#1013)              |  32.3   |  20.1   |   4.0   |    -    |        |
| 15 | 2019 | ICCV  | [TSM](#1015)               |  30.3   |  19.0   |   4.5   |    -    |        |
| 17 | 2019 | ICCV  | [Nguyen et al.](#1017)     |  36.4   |  19.2   |   2.9   |    -    |        |
| 18 | 2020 | AAAI  | [PreTrimNet&dagger;](#1018)|  34.8   |  20.9   |   5.3   |  22.5   |        |
| 19 | 2020 | AAAI  | [BaS-Net](#1019)           |  34.5   |  22.5   |   4.9   |  22.2   |[`[o-pytorch]`](https://github.com/Pilhyeon/BaSNet-pytorch)|
| 28 | 2020 | ECCV  | [A2CL-PT](#1028)           |  36.8   |  22.0   |   5.2   |  22.5   |[`[o-pytorch]`](https://github.com/MichiganCOG/A2CL-PT)|
| 29 | 2020 | ECCV  | [TSCN](#1029)              |  35.3   |  21.4   |   5.3   |  21.7   |        |
| 30 | 2020 | MM    | [ACM-BANet](#1030)         |  37.6   |  24.7   |   6.5   |  24.4   |        |
| 32 | 2021 | AAAI  | [Liu et al.](#1032)        |  35.1   |  23.7   |   5.6   |  23.2   |        |
| 33 | 2021 | AAAI  | [ACSNet](#1033)            |  36.3   |  24.2   |   5.8   |  23.9   |        |
| 35 | 2021 | AAAI  | [Lee et al.](#1035)        |  37.0   |  23.9   |   5.7   |  23.7   |[`[o-pytorch]`](https://github.com/Pilhyeon/WTAL-Uncertainty-Modeling)|
| 39 | 2021 | CVPR  | [AUMN](#1039)              |  38.3   |  23.5   |   5.2   |  23.5   |        |
| 40 | 2021 | CVPR  | [TS-PCA](#1040)            |  37.4   |  23.5   |   5.9   |  23.7   |        |
| 41 | 2021 | CVPR  | [UGCT](#1041)              |  39.1   |  22.4   |   5.8   |  23.8   |        |
| 43 | 2021 | ICCV  | [FAC-Net](#1043)           |  37.6   |  24.2   |   6.0   |  24.0   |[`[o-pytorch]`](https://github.com/LeonHLJ/FAC-Net)|
| 47 | 2022 | CVPR  | [FTCL](#1047)              |  40.0   |  24.3   |   6.4   |  24.8   |[`[o-pytorch]`](https://github.com/MengyuanChen21/CVPR2022-FTCL)|
| 48 | 2022 | CVPR  | [DCC](#1048)               |  38.8   |  24.2   |   5.7   |  24.3   |        |
| 49 | 2022 | CVPR  | [Huang et al.](#1049)      |  40.6   |  24.6   |   5.9   |  25.0   |[`[o-pytorch]`](https://github.com/LeonHLJ/RSKP)|
| 50 | 2022 | CVPR  | [ASM-Loc](#1050)           |  41.0   |  24.9   |   6.2   |  25.1   |[`[o-pytorch]`](https://github.com/boheumd/ASM-Loc)|
| 51 | 2022 | MM    | [DGCNN](#1051)             |  37.2   |  23.8   |   5.8   |  23.9   |        |
| 55 | 2023 | WACV  | [TFE-DCN](#1055)           |  41.4   |  24.8   |   6.4   |  25.3   |[`[o-pytorch]`](https://github.com/jianxiong-zhou/TFE-DCN)|
| 56 | 2023 | CVPR  | [Wang et al.](#1056)       |  41.8   |  25.7   |   6.5   |  26.3   |        |
| 57 | 2023 | CVPR  | [Li et al.](#1057)         |  41.8   |  26.0   |   6.0   |  26.0   |[`[o-pytorch]`](https://github.com/lgzlIlIlI/Boosting-WTAL)|
| 58 | 2023 | CVPR  | [Ren et al.](#1058)        |  41.8   |  25.4   |   5.2   |  25.5   |[`[o-pytorch]`](https://github.com/RenHuan1999/CVPR2023_P-MIL)|
| 59 | 2023 | CVPR  | [Zhou et al.](#1059)       |  43.4   |**28.8** |**9.9**  |**28.8** |[`[o-pytorch]`](https://github.com/zhou745/GauFuse_WSTAL)|
| 61 | 2023 | CVPR  | [PivoTAL](#1061)           |**45.1** |  28.2   |  5.0    |  28.1   |        |

##

### FineAction

| ID | Year | Venue |   Model<br/>(or Authors)   |  @0.5   |  @0.75  |  @0.95  |   AVG   |  code  |
|:--:|:----:|:-----:|:--------------------------:|:-------:|:-------:|:-------:|:-------:|:------:|
| 5  | 2018 | ECCV  | [W-TALC](#1005) (Reprod.)  |  6.18   |  3.15   |  0.83   |  3.45   |[`[o-pytorch]`](https://github.com/sujoyp/wtalc-pytorch)<br/>[`[o-tensorflow]`](https://github.com/sujoyp/wtalc-tensorflow)|
| 35 | 2021 | AAAI  | [Lee et al.](#1035) (Reprod.)|  6.65   |  3.23   |  0.95   |  3.64   |[`[o-pytorch]`](https://github.com/Pilhyeon/WTAL-Uncertainty-Modeling)|
| 37 | 2021 | CVPR  | [ASL](#1037) (Reprod.)     |  6.79   |  2.68   |  0.81   |  3.30   |[`[o-pytorch]`](https://github.com/layer6ai-labs/ASL)|
| 42 | 2021 | ICCV  | [D2-Net](#1042) (Reprod.)  |  6.75   |  3.02   |  0.82   |  3.35   |[`[o-pytorch]`](https://github.com/naraysa/D2-Net)|
| 53 | 2022 | ECCV  | [HAAN](#1053)              |**7.05** |**3.95** |**1.14** |**4.10** |[`[o-pytorch]`](https://github.com/lizhi1104/HAAN)|

##

### FineGym

| ID | Year | Venue |   Model<br/>(or Authors)   |  @0.1   |  @0.2   |  @0.3   |  @0.4   |  @0.5   |   AVG   |  code  |
|:--:|:----:|:-----:|:--------------------------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:------:|
| 5  | 2018 | ECCV  | [W-TALC](#1005) (Reprod.)  |  8.85   |  7.32   |  6.24   |  4.95   |  3.15   |  6.03   |[`[o-pytorch]`](https://github.com/sujoyp/wtalc-pytorch)<br/>[`[o-tensorflow]`](https://github.com/sujoyp/wtalc-tensorflow)|
| 35 | 2021 | AAAI  | [Lee et al.](#1035) (Reprod.)|  9.45   |  8.63   |  5.10   |  4.34   |  3.05   |  6.11   |[`[o-pytorch]`](https://github.com/Pilhyeon/WTAL-Uncertainty-Modeling)|
| 37 | 2021 | CVPR  | [ASL](#1037) (Reprod.)     |  9.33   |  7.92   |  5.45   |  3.67   |  2.24   |  5.74   |[`[o-pytorch]`](https://github.com/layer6ai-labs/ASL)|
| 42 | 2021 | ICCV  | [D2-Net](#1042) (Reprod.)  |  9.46   |  8.67   |  5.21   |  4.22   |  2.65   |  6.04   |[`[o-pytorch]`](https://github.com/naraysa/D2-Net)|
| 53 | 2022 | ECCV  | [HAAN](#1053)              |**10.79**|**9.62** |**7.65** |**6.16** |**4.16** |**7.67** |[`[o-pytorch]`](https://github.com/lizhi1104/HAAN)|

##

## Paper List

1. <span id = "1001">**[UntrimmedNets]**</span> | **CVPR'17** | UntrimmedNets for Weakly Supervised Action Recognition and Detection | [`[pdf]`](https://arxiv.org/pdf/1703.03329.pdf) | [`[o-matlab]`](https://github.com/wanglimin/UntrimmedNet)
2. <span id = "1002">**[Hide-and-seek]**</span> | **ICCV'17** | Hide-and-Seek: Forcing a Network to be Meticulous for Weakly-supervised Object and Action Localization | [`[pdf]`](https://arxiv.org/pdf/1704.04232.pdf) | [`[o-torch]`](https://github.com/kkanshul/Hide-and-Seek)
3. <span id = "1003">**[STPN]**</span> | **CVPR'18** | Weakly Supervised Action Localization by Sparse Temporal Pooling Network | [`[pdf]`](https://arxiv.org/pdf/1712.05080.pdf) | [`[u-tensorflow]`](https://github.com/bellos1203/STPN)
4. <span id = "1004">**[AutoLoc]**</span> | **ECCV'18** | AutoLoc: Weakly-supervised Temporal Action Localization in Untrimmed Videos | [`[pdf]`](https://arxiv.org/pdf/1807.08333.pdf) | [`[o-caffe]`](https://github.com/zhengshou/AutoLoc)
5. <span id = "1005">**[W-TALC]**</span> | **ECCV'18** | W-TALC: Weakly-supervised Temporal Activity Localization and Classification | [`[pdf]`](https://arxiv.org/pdf/1807.10418.pdf) | [`[o-pytorch]`](https://github.com/sujoyp/wtalc-pytorch) | [`[o-tensorflow]`](https://github.com/sujoyp/wtalc-tensorflow)
6. <span id = "1006">**[Zhong et al.]**</span> | **MM'18** | Step-by-step Erasion, One-by-one Collection: A Weakly Supervised Temporal Action Detector | [`[pdf]`](https://arxiv.org/pdf/1807.02929.pdf)
7. <span id = "1007">**[TSR-Net\*]**</span> | **AAAI'19** | Learning Transferable Self-attentive Representations for Action Recognition in Untrimmed Videos with Weak Supervision | [`[pdf]`](https://arxiv.org/pdf/1902.07370.pdf)
8. <span id = "1008">**[STAR&dagger;]**</span> | **AAAI'19** | Segregated Temporal Assembly Recurrent Networks for Weakly Supervised Multiple Action Detection | [`[pdf]`](https://arxiv.org/pdf/1811.07460.pdf)
9. <span id = "1009">**[MAAN]**</span> | **ICLR'19** | Marginalized Average Attentional Network for Weakly-Supervised Learning | [`[pdf]`](https://arxiv.org/pdf/1905.08586.pdf)
10. <span id = "1010">**[Liu et al.]**</span> | **CVPR'19** | Completeness Modeling and Context Separation for Weakly Supervised
Temporal Action Localization | [`[pdf]`](https://openaccess.thecvf.com/content_CVPR_2019/papers/Liu_Completeness_Modeling_and_Context_Separation_for_Weakly_Supervised_Temporal_Action_CVPR_2019_paper.pdf) | [`[o-pytorch]`](https://github.com/Finspire13/CMCS-Temporal-Action-Localization)
11. <span id = "1011">**[Park et al.]**</span> | **ICIP'19** | Graph Regularization Network with Semantic Affinity for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://easy00.github.io/assets/publication/icip19_Jungin_Park.pdf)
12. <span id = "1012">**[ACN]**</span> | **ICIP'19** | Action Coherence Network for Weakly Supervised Temporal Action Localization | [`[pdf]`](https://www.yhzhai.com/publications/Action-Coherence-Network-for-Weakly-Supervised-Temporal-Action-Localization.pdf)
13. <span id = "1013">**[ASSG]**</span> | **MM'19** | Adversarial Seeded Sequence Growing for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/1908.02422.pdf)
14. <span id = "1014">**[CleanNet]**</span> | **ICCV'19** | Weakly Supervised Temporal Action Localization through Contrast based Evaluation Networks | [`[pdf]`](https://openaccess.thecvf.com/content_ICCV_2019/papers/Liu_Weakly_Supervised_Temporal_Action_Localization_Through_Contrast_Based_Evaluation_Networks_ICCV_2019_paper.pdf)
15. <span id = "1015">**[TSM]**</span> | **ICCV'19** | Temporal Structure Mining for Weakly Supervised Action Detection | [`[pdf]`](https://openaccess.thecvf.com/content_ICCV_2019/papers/Yu_Temporal_Structure_Mining_for_Weakly_Supervised_Action_Detection_ICCV_2019_paper.pdf)
16. <span id = "1016">**[3C-Net&dagger;]**</span> | **ICCV'19** | 3C-Net: Category Count and Center Loss for Weakly-Supervised Action Localization | [`[pdf]`](https://arxiv.org/pdf/1908.08216.pdf) | [`[o-pytorch]`](https://github.com/naraysa/3c-net)
17. <span id = "1017">**[Nguyen et al.]**</span> | **ICCV'19** | Weakly-supervised Action Localization with Background Modeling | [`[pdf]`](https://arxiv.org/pdf/1908.06552.pdf)
18. <span id = "1018">**[PreTrimNet&dagger;]**</span> | **AAAI'20** | Multi-Instance Multi-Label Action Recognition and Localization Based on Spatio-Temporal Pre-Trimming for Untrimmed Videos | [`[pdf]`](https://ojs.aaai.org/index.php/AAAI/article/download/6986/6840)
19. <span id = "1019">**[BaS-Net]**</span> | **AAAI'20** | Background Suppression Network for Weakly-supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/1911.09963.pdf) | [`[o-pytorch]`](https://github.com/Pilhyeon/BaSNet-pytorch)
20. <span id = "1020">**[RPN]**</span> | **AAAI'20** | Relational Prototypical Network for Weakly Supervised Temporal Action Localization | [`[pdf]`](http://ir.ia.ac.cn/bitstream/173211/39128/1/AAAI-HuangL.1235.pdf)
21. <span id = "1021">**[WSGN]**</span> | **WACV'20** | Weakly Supervised Gaussian Networks for Action Detection | [`[pdf]`](https://arxiv.org/pdf/1904.07774.pdf)
22. <span id = "1022">**[Islam and Radke]**</span> | **WACV'20** | Weakly Supervised Temporal Action Localization Using Deep Metric Learning | [`[pdf]`](https://arxiv.org/pdf/2001.07793.pdf) | [`[o-pytorch]`](https://github.com/asrafulashiq/wsad)
23. <span id = "1023">**[Rashid et al.]**</span> | **WACV'20** | Action Graphs: Weakly-supervised Action Localization with Graph Convolution Networks | [`[pdf]`](https://arxiv.org/pdf/2002.01449.pdf) | [`[o-pytorch]`](https://github.com/menorashid/action_graphs)
24. <span id = "1024">**[ActionBytes]**</span> | **CVPR'20** | ActionBytes: Learning from Trimmed Videos to Localize Actions | [`[pdf]`](https://openaccess.thecvf.com/content_CVPR_2020/papers/Jain_ActionBytes_Learning_From_Trimmed_Videos_to_Localize_Actions_CVPR_2020_paper.pdf)
25. <span id = "1025">**[DGAM]**</span> | **CVPR'20** | Weakly-Supervised Action Localization by Generative Attention Modeling | [`[pdf]`](https://arxiv.org/pdf/2003.12424.pdf) | [`[o-pytorch]`](https://github.com/bfshi/DGAM-Weakly-Supervised-Action-Localization)
26. <span id = "1026">**[Gong et al.]**</span> | **CVPR'20** | Learning Temporal Co-Attention Models for Unsupervised Video Action Localization | [`[pdf]`](https://openaccess.thecvf.com/content_CVPR_2020/papers/Gong_Learning_Temporal_Co-Attention_Models_for_Unsupervised_Video_Action_Localization_CVPR_2020_paper.pdf) | [`[o-pytorch]`](https://github.com/GGQ1996/action_co_localization/tree/master/ACL_Anet_release)
27. <span id = "1027">**[EM-MIL]**</span> | **ECCV'20** | Weakly-Supervised Action Localization with Expectation-Maximization Multi-Instance Learning | [`[pdf]`](https://arxiv.org/pdf/2004.00163.pdf) | [`[o-pytorch]`](https://github.com/airmachine/EM-MIL-WeaklyActionDetection)
28. <span id = "1028">**[A2CL-PT]**</span> | **ECCV'20** | Adversarial Background-Aware Loss for Weakly-supervised Temporal Activity Localization | [`[pdf]`](https://arxiv.org/pdf/2007.06643.pdf) | [`[o-pytorch]`](https://github.com/MichiganCOG/A2CL-PT)
29. <span id = "1029">**[TSCN]**</span> | **ECCV'20** | Two-Stream Consensus Network for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2010.11594.pdf)
30. <span id = "1030">**[ACM-BANet]**</span> | **MM'20** | Action Completeness Modeling with Background Aware Networks for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://dl.acm.org/doi/pdf/10.1145/3394171.3413687)
31. <span id = "1031">**[RefineLoc]**</span> | **WACV'21** | RefineLoc: Iterative Refinement for Weakly-Supervised Action Localization | [`[pdf]`](https://arxiv.org/pdf/1904.00227.pdf) | [`[o-pytorch]`](https://github.com/HumamAlwassel/RefineLoc)
32. <span id = "1032">**[Liu et al.]**</span> | **AAAI'21** | Weakly Supervised Temporal Action Localization Through Learning Explicit Subspaces for Action and Context | [`[pdf]`](http://gr.xjtu.edu.cn/documents/1809645/1810998/AAAI2021b.pdf/5482f149-3858-d059-f71e-e439dcc8edb2?t=1608017846044)
33. <span id = "1033">**[ACSNet]**</span> | **AAAI'21** | ACSNet: Action-Context Separation Network for Weakly Supervised Temporal Action Localization | [`[pdf]`](http://gr.xjtu.edu.cn/documents/1809645/1810998/AAAI2021a.pdf/651076be-cec7-2f6a-be3c-8da8c03ef12c?t=1608017799289)
34. <span id = "1034">**[HAM-Net]**</span> | **AAAI'21** | A Hybrid Attention Mechanism for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2101.00545.pdf) | [`[o-pytorch]`](https://github.com/asrafulashiq/hamnet)
35. <span id = "1035">**[Lee et al.]**</span> | **AAAI'21** | Weakly-supervised Temporal Action Localization by Uncertainty Modeling | [`[pdf]`](https://arxiv.org/pdf/2006.07006.pdf) | [`[o-pytorch]`](https://github.com/Pilhyeon/WTAL-Uncertainty-Modeling)
36. <span id = "1036">**[Lee et al.&dagger;]**</span> | **ICLR'21** | Cross-attentional Audio-visual Fusion for Weakly-supervised Action Localization | [`[pdf]`](https://openreview.net/pdf?id=hWr3e3r-oH5)
37. <span id = "1037">**[ASL]**</span> | **CVPR'21** | Weakly Supervised Action Selection Learning in Video | [`[pdf]`](http://www.cs.toronto.edu/~mvolkovs/CVPR2021_asl.pdf) | [`[o-pytorch]`](https://github.com/layer6ai-labs/ASL)
38. <span id = "1038">**[CoLA]**</span> | **CVPR'21** | CoLA: Weakly-Supervised Temporal Action Localization with Snippet Contrastive Learning | [`[pdf]`](https://arxiv.org/pdf/2103.16392.pdf) | [`[o-pytorch]`](https://github.com/zhang-can/CoLA)
39. <span id = "1039">**[AUMN]**</span> | **CVPR'21** | Action Unit Memory Network for Weakly Supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2104.14135.pdf)
40. <span id = "1040">**[TS-PCA]**</span> | **CVPR'21** | The Blessings of Unlabeled Background in Untrimmed Videos | [`[pdf]`](https://arxiv.org/pdf/2103.13183.pdf)
41. <span id = "1041">**[UGCT]**</span> | **CVPR'21** | Uncertainty Guided Collaborative Training for Weakly Supervised Temporal Action Detection | [`[pdf]`](https://openaccess.thecvf.com/content/CVPR2021/papers/Yang_Uncertainty_Guided_Collaborative_Training_for_Weakly_Supervised_Temporal_Action_Detection_CVPR_2021_paper.pdf)
42. <span id = "1042">**[D2-Net]**</span> | **ICCV'21** | D2-Net: Weakly-Supervised Action Localization via Discriminative Embeddings
and Denoised Activations | [`[pdf]`](https://arxiv.org/pdf/2012.06440.pdf) | [`[o-pytorch]`](https://github.com/naraysa/D2-Net)
43. <span id = "1043">**[FAC-Net]**</span> | **ICCV'21** | Foreground-Action Consistency Network for Weakly Supervised Temporal Action Localization
 | [`[pdf]`](https://arxiv.org/pdf/2108.06524.pdf) | [`[o-pytorch]`](https://github.com/LeonHLJ/FAC-Net)
44. <span id = "1044">**[CSCL]**</span> | **MM'21** | Weakly-Supervised Temporal Action Localization via Cross-Stream Collaborative Learning | [`[pdf]`](https://dl.acm.org/doi/pdf/10.1145/3474085.3475261)
45. <span id = "1045">**[CO<sub>2</sub>-Net]**</span> | **MM'21** | Cross-modal Consensus Network for Weakly Supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2107.12589.pdf) | [`[o-pytorch]`](https://github.com/harlanhong/MM2021-CO2-Net)
46. <span id = "1046">**[ACGNet]**</span> | **AAAI'22** | ACGNet: Action Complement Graph Network for Weakly-supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2112.10977.pdf)
47. <span id = "1047">**[FTCL]**</span> | **CVPR'22** | Fine-grained Temporal Contrastive Learning for Weakly-supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2203.16800.pdf) | [`[o-pytorch]`](https://github.com/MengyuanChen21/CVPR2022-FTCL)
49. <span id = "1048">**[DCC]**</span> | **CVPR'22** | Exploring Denoised Cross-video Contrast for Weakly-supervised Temporal Action Localization | [`[pdf]`](https://tianyu-yang.com/resources/dcc.pdf)
48. <span id = "1049">**[Huang et al.]**</span> | **CVPR'22** | Weakly Supervised Temporal Action Localization via Representative Snippet Knowledge Propagation | [`[pdf]`](https://arxiv.org/pdf/2203.02925.pdf) | [`[o-pytorch]`](https://github.com/LeonHLJ/RSKP)
50. <span id = "1050">**[ASM-Loc]**</span> | **CVPR'22** | ASM-Loc: Action-aware Segment Modeling for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2203.15187.pdf) | [`[o-pytorch]`](https://github.com/boheumd/ASM-Loc)
51. <span id = "1051">**[DGCNN]**</span> | **MM'22** | Dynamic Graph Modeling for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://dl.acm.org/doi/pdf/10.1145/3503161.3548077)
52. <span id = "1052">**[Li et al.]**</span> | **MM'22** | Forcing the Whole Video as Background: An Adversarial Learning Strategy for Weakly Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2207.06659.pdf)
53. <span id = "1053">**[HAAN]**</span> | **ECCV'22** | Weakly-Supervised Temporal Action Detection for Fine-Grained Videos with Hierarchical Atomic Actions | [`[pdf]`](https://arxiv.org/pdf/2207.11805.pdf) | [`[o-pytorch]`](https://github.com/lizhi1104/HAAN)
54. <span id = "1054">**[DELU]**</span> | **ECCV'22** | Dual-Evidential Learning for Weakly-supervised Temporal Action Localization | [`[pdf]`](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136640190.pdf) | [`[o-pytorch]`](https://github.com/MengyuanChen21/ECCV2022-DELU)
55. <span id = "1055">**[TFE-DCN]**</span> | **WACV'23** | Temporal Feature Enhancement Dilated Convolution Network for Weakly-supervised Temporal Action Localization | [`[pdf]`](https://openaccess.thecvf.com/content/WACV2023/papers/Zhou_Temporal_Feature_Enhancement_Dilated_Convolution_Network_for_Weakly-Supervised_Temporal_Action_WACV_2023_paper.pdf) | [`[o-pytorch]`](https://github.com/jianxiong-zhou/TFE-DCN)
56. <span id = "1056">**[Wang et al.]**</span> | **CVPR'23** | Two-Stream Networks for Weakly-Supervised Temporal Action Localization with Semantic-Aware Mechanisms | [`[pdf]`](https://openaccess.thecvf.com/content/CVPR2023/papers/Wang_Two-Stream_Networks_for_Weakly-Supervised_Temporal_Action_Localization_With_Semantic-Aware_Mechanisms_CVPR_2023_paper.pdf)
57. <span id = "1057">**[Li et al.]**</span> | **CVPR'23** | Boosting Weakly-Supervised Temporal Action Localization with Text Information | [`[pdf]`](https://arxiv.org/pdf/2305.00607.pdf) | [`[o-pytorch]`](https://github.com/lgzlIlIlI/Boosting-WTAL)
58. <span id = "1058">**[Ren et al.]**</span> | **CVPR'23** | Proposal-based Multiple Instance Learning for Weakly-supervised Temporal Action Localization | [`[pdf]`](https://openaccess.thecvf.com/content/CVPR2023/papers/Ren_Proposal-Based_Multiple_Instance_Learning_for_Weakly-Supervised_Temporal_Action_Localization_CVPR_2023_paper.pdf) | [`[o-pytorch]`](https://github.com/RenHuan1999/CVPR2023_P-MIL)
59. <span id = "1059">**[Zhou et al.]**</span> | **CVPR'23** | Improving Weakly Supervised Temporal Action Localization by Bridging Train-Test Gap in Pseudo Labels | [`[pdf]`](https://arxiv.org/pdf/2304.07978.pdf) | [`[o-pytorch]`](https://github.com/zhou745/GauFuse_WSTAL)
60. <span id = "1060">**[Ju et al.&dagger;]**</span> | **CVPR'23** | Distilling Vision-Language Pre-training to Collaborate with Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://arxiv.org/pdf/2212.09335.pdf)
61. <span id = "1061">**[PivoTAL]**</span> | **CVPR'23** | PivoTAL: Prior-Driven Supervision for Weakly-Supervised Temporal Action Localization | [`[pdf]`](https://openaccess.thecvf.com/content/CVPR2023/papers/Rizve_PivoTAL_Prior-Driven_Supervision_for_Weakly-Supervised_Temporal_Action_Localization_CVPR_2023_paper.pdf)

##

## Feedback

If you have any suggestions or find missing papers, please feel free to contact me.

- [e-mail](mailto:lph1114@yonsei.ac.kr)
- [pull request](https://github.com/Pilhyeon/weakly-supervised-temporal-action-localization/pulls)
