# 3D reconstruction
Небольшое исследование 3D реконструкции (Полезные ссылки, обзор связанных статей и результатов, личные заметки). Начало было положено в августе 2020 года. На создание подобного репо вдохновил - [:mage_man:](https://github.com/timzhang642/3D-Machine-Learning), а на исследование - [:mage_man:](https://www.cs.sfu.ca/~furukawa/) :)​

> Справка:
>
> :mag_right: - WHAT? - Разобрать в ближайшее время
>
> :heavy_division_sign: - Ссылка на формулы из статьи
>
> :thought_balloon: - Объемные заметки
>
> /-...-/ - Переменная или формула

## Содержание

- [Статьи](#papers)
  - [Обзорные](#review)
  - [Датасеты](#dataset)
  - [Теория](#theory)
- [Дополнительные ссылки](#links)
  - [Хабр:](#habr)
  - [GitHub:](#github)
  - [YouTube:](#youtube)
  - [Stackoveflow:](#stackoveflow)
  - [Разное:](#other)
  - [Платформы:](#platform)



<a name="papers" />

## Статьи

Подробный анализ прочитанных статей, краткие выводы.



<a name="review" />

### Обзорные

Общий обзор на исследование, литературный обзор, ссылки на разные тематические статьи других авторов.

- **[[статья](https://arxiv.org/pdf/1906.06543.pdf)] (NOV2019) Image-based 3D Object Reconstruction: State-of-the-Art and Trends in the Deep Learning Era**





- **[[статья](https://arxiv.org/pdf/1906.06113.pdf)] (JUN2019) A Survey on Deep Learning Architectures for Image-based Depth Reconstruction**
  - COM - Обзор на все существующие методы - 2015-2019 года, 149 статьи для literarure view, 88 методов для 3d reconstruction (+ 6-8 методов для human face), математическая формулировка, таксономия: и много другое. 





- **[[статья](https://vision.cs.princeton.edu/projects/2012/3DnotLow/report.pdf)] 3D reconstruction is not just a low-level task: retrospect and survey**





- **[[статья](https://arxiv.org/pdf/1906.06113v1.pdf)] (JUN2019) A Survey on Deep Learning Architectures for Image-based Depth Reconstruction**

<a name="dataset" />

### Датасеты

**[[статья](https://arxiv.org/pdf/1709.06158.pdf)] (SEP2017) Matterport3D: Learning from RGB-D Data in Indoor Environments [[сайт](https://niessner.github.io/Matterport/)] [[код](https://github.com/niessner/Matterport)]**

<a name="theory"/>

### Теория

#### 2015

**[[статья](https://abhishekkar.info/categoryshapes.pdf)] Category-Specific Object Reconstruction from a Single Image**

**[[статья](http://3dshapenets.cs.princeton.edu/paper.pdf)] 3D ShapeNets: A Deep Representation for Volumetric Shapes [[сайт](http://3dshapenets.cs.princeton.edu/)] [[:heavy_division_sign:](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/formulations.md#form1)] [[:thought_balloon:](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/notes/3D_ShapeNets.md)]**

#### 2016

#### 2017

**[[статья](https://sci-hub.se/10.1145/3150165.3150166)] Cloud-based collaborative 3D reconstruction using smartphones**  

**[[статья](https://openaccess.thecvf.com/content_cvpr_2017/papers/Soltani_Synthesizing_3D_Shapes_CVPR_2017_paper.pdf)] Synthesizing 3D Shapes via Modeling Multi-View Depth Maps and Silhouettes with Deep Generative Networks [[код на Lua](https://github.com/Amir-Arsalan/Synthesize3DviaDepthOrSil)]**

#### 2018

**[[статья](https://arxiv.org/pdf/1803.03352v1.pdf)] Indoor Scene Understanding in 2.5/3D: A Survey**

**[[статья](https://arxiv.org/pdf/1804.05469.pdf)] Im2Struct: Recovering 3D Shape Structure from a Single RGB Image**

**[[статья](https://arxiv.org/pdf/1809.03770.pdf)] 3D Human Body Reconstruction from a Single Image via Volumetric Regression**

#### 2019

**[[статья](https://www.dgpf.de/src/tagung/jt2019/proceedings/proceedings/papers/23_3LT2019_Schmohl_Soergel.pdf)] ALS Klassifizierung mit Submanifold Sparse Convolutional Networks [[сайт](https://www.ifp.uni-stuttgart.de/en/research/remote_sensing/als_point_cloud_classification/)]**

- COM - Вокселизация облака точек

**[[статья](https://arxiv.org/pdf/1812.03828.pdf)] Occupancy Networks: Learning 3D Reconstruction in Function Space [[видео](https://www.youtube.com/watch?v=9r9TDr2Aq5A)]**

**[[статья](https://arxiv.org/pdf/1905.07259.pdf)] Texture Fields: Learning Texture Representations in Function Space [[видео](https://www.youtube.com/watch?v=9r9TDr2Aq5A)]**

**[[статья](http://www.cvlibs.net/publications/Niemeyer2019ICCV.pdf)] Occupancy Flow: 4D Reconstruction by Learning Particle Dynamics [[видео](https://www.youtube.com/watch?v=9r9TDr2Aq5A)]**

#### 2020

**[[статья](https://arxiv.org/pdf/2001.06280v1.pdf)] Review: deep learning on 3D point clouds**

**[[статья](https://arxiv.org/pdf/2003.09754.pdf)] Learning 3D Part Assembly from a Single Image [[сайт](https://cs.stanford.edu/~kaichun/impartass/)] [[код на Python](https://github.com/AntheaLi/3DPartAssembly)]** 

**[[статья](https://arxiv.org/pdf/1906.05113.pdf)] A Survey of Autonomous Driving: Common Practices and Emerging Technologies**

**[[статья](https://arxiv.org/pdf/2004.00452.pdf)] PIFuHD: Multi-Level Pixel-Aligned Implicit Function for High-Resolution 3D Human Digitization**

**[[статья](https://storage.googleapis.com/immersive-lf-video-siggraph2020/ImmersiveLightFieldVideoWithALayeredMeshRepresentation.pdf)] Immersive Light Field Video with a Layered Mesh Representation [[сайт](https://augmentedperception.github.io/deepviewvideo/)]**

**[[статья](https://arxiv.org/pdf/2010.04595.pdf)] GRF: LEARNING A GENERAL RADIANCE FIELD FOR 3D SCENE REPRESENTATION AND RENDERING [[GitHub](https://github.com/alextrevithick/GRF)]**

**[[статья](https://arxiv.org/pdf/2012.03927.pdf)] NeRV: Neural Reflectance and Visibility Fields for Relighting and View Synthesis [[сайт](https://pratulsrinivasan.github.io/nerv/)]**

- IN - набор изображений, с непрерывным известным освещением.





- OUT - трехмерное представление объекта, с возможностью произвольного освещения и смены точки обзора





- COM - 

**[[статья](https://arxiv.org/pdf/1912.07372.pdf)] Differentiable Volumetric Rendering: Learning Implicit 3D Representations without 3D Supervision [[видео](https://www.youtube.com/watch?v=9r9TDr2Aq5A)]**

<a name="links" />

## Дополнительные ссылки

<a name="habr" />

### Хабр:

**[[1](https://habr.com/ru/company/top3dshop/blog/511026/)] Обзор программного обеспечения для 3D-сканирования и обработки данных**

**[[2](https://habr.com/ru/post/446872/)] Изучаем OpenCV на StereoPi: карта глубин по видео [[GitHub](https://github.com/realizator/stereopi-tutorial)]**

**[[3](https://habr.com/ru/post/458458/)] Камеры глубины — тихая революция (когда роботы будут видеть) Часть 2**



<a name="github" />

### GitHub:

**[[GitHub](https://github.com/Yochengliu/awesome-point-cloud-analysis#---recent-papers-from-2017)] awesome-point-cloud-analysis**

- COM - 

**[[GitHub](https://github.com/aktumar/3D-Machine-Learning)] 3D-Machine-Learning**

- COM - 

<a name="youtube" />

### YouTube:

**[[видео](https://www.youtube.com/watch?v=bTp1DRfULII)] (MAY2015) Football Stadium 3D Evacuation Simulation**

**[[видео](https://www.youtube.com/watch?v=dR5G5SNI5T4)] (MAY2015) Oasys Software - MassMotion, The World's Most Advanced Crowd Simulation Software**





**[[видео](https://www.youtube.com/watch?v=3Wq3vU6Ea6A)] (FEB2017) 3D printed 3D Scanner ... in action**

**[[видео](https://www.youtube.com/watch?v=9SVC7XBhBpk)] (APR2017) Implicit Crowd Simulation**





**[[видео](https://www.youtube.com/watch?v=xEwKarW1ZF4)] (MAY2018) F8: How A.I. and Point Cloud Reconstruction Will Make VR Realistic**

**[[видео](https://www.youtube.com/watch?v=CBpZtnu1Mig)] (JUN2018) DIY 3D Scanner - Fully 3d printed photogrammetry rig**





**[[видео](https://www.youtube.com/watch?v=y9SMd9NwoC0)] (MAR2020) Crowd simulation in Unity3D DOTS. Density & Instance colors**

**[[видео](https://www.youtube.com/watch?v=o1RbLLVwFTA&feature=emb_title)] (MAR2020) Unmanned Aerial Vehicle Path Planning for Exploration Mapping**

**[[видео](https://www.youtube.com/watch?v=eCDBA_SbxCE)] (JUL2020) 3D Deep Learning with PyTorch3D by Nikhila Ravi**

**[[видео](https://youtu.be/9r9TDr2Aq5A)] (JUN2020) Learning 3D Reconstruction in Function Space (Long Version)**

<a name="8" />

- COM1 - Исследование нейронных неявных представлений. То что я знала до этого (воксели и облака точек) - плюс сетка(меш) - является традиционной концепцией трехмерного представления явным образом.

- COM2 - *What is a good output representation?*

  `Voxels`:

  - Discretization of 3D space into regular grid
  - Easy to process with neural networks
  - Cubic memory O(n^3) - limited resolurion
  - Manhattan world bias [[12](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#8)]

  `Points`: 

  - Discretization of surface into 3D points
  - Does not model connectivaly / topology
  - Limited number of points
  - Global shape description

  `Meshes`:

  - Discretization into vertices and faces
  - Limited number of vertices / granularity 
  - Requires class-specific template - or -
  - Leads to self-intersections

- COM3 - *About work in video*:

  `Purpose`:

  - Implicit representation - NO discretization
  - Arbitrary topology & resolution
  - Low memory footprint
  - Not restricted to specific class

  `Key idea`:

  - Do not represent 3D shape explicitly
  - Instead, consider surface implicitly as decision boundary of a non-linear classifier
  - [0, 1] - outside/inside

  `Network architecture`:

  - Encoder - 

**[[видео](https://www.youtube.com/watch?v=-mQ60wNgKrQ&feature=youtu.be)] (NOV2020) The Beirut Port Explosions (English)**

<a name="stackoveflow" />

### Stackoveflow:

**[[1](https://stackoverflow.com/questions/7705377/3d-reconstruction-how-to-create-3d-model-from-2d-image)]:** 

<a name="other" />

### Разное:

**[[сайт](https://machinelearningmastery.com/a-gentle-introduction-to-pix2pix-generative-adversarial-network/)] A Gentle Introduction to Pix2Pix Generative Adversarial Network**

- COM - Про систему GAN

<a name="platform" />

### Платформы:

**[Agisoft Metashape](https://www.agisoft.com/)**

