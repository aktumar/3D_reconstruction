# 3D reconstruction
Небольшой литературный обзор по 3D реконструкции (Полезные ссылки, обзор связанных статей и результатов, личные заметки). Начало было положено в августе 2020 года. На создание подобного репо вдохновил - [:mage_man:](https://github.com/timzhang642/3D-Machine-Learning), а на исследование - [:mage_man:](https://www.cs.sfu.ca/~furukawa/) :)



## Содержание

- [Обзорные ссылки](#review)
- [Статьи](#papers)
- [Дополнительные ссылки](#links)
  - [Хабр:](#habr)
  - [YouTube:](#youtube)
  - [Stackoveflow:](#stackoveflow)
  - [Разное:](#other)
  - [Платформы:](#platform)



<a name="review" />

## Обзорные ссылки

Общий обзор на исследование, литературный обзор, ссылки на разные тематические статьи других авторов.

- **[[статья](https://arxiv.org/pdf/1906.06543.pdf)] (NOV2019) Image-based 3D Object Reconstruction: State-of-the-Art and Trends in the Deep Learning Era**
- **[[статья](https://arxiv.org/pdf/1906.06113.pdf)] (JUN2019) A Survey on Deep Learning Architectures for Image-based Depth Reconstruction**
  - COM - Обзор на все существующие методы - 2015-2019 года, 149 статьи для literarure view, 88 методов для 3d reconstruction (+ 6-8 методов для human face), математическая формулировка, таксономия: и много другое. 
- **[[статья](https://vision.cs.princeton.edu/projects/2012/3DnotLow/report.pdf)] 3D reconstruction is not just a low-level task: retrospect and survey**
- **[[статья](https://arxiv.org/pdf/1906.06113v1.pdf)] (JUN2019) A Survey on Deep Learning Architectures for Image-based Depth Reconstruction**





- **[[GitHub](https://github.com/Yochengliu/awesome-point-cloud-analysis#---recent-papers-from-2017)] awesome-point-cloud-analysis**
  - COM - 
- **[[GitHub](https://github.com/aktumar/3D-Machine-Learning)] 3D-Machine-Learning**
  - COM - 

<a name="papers" />

## Статьи

Подробный анализ прочитанных статей, краткие выводы.



**[[статья](http://3dshapenets.cs.princeton.edu/paper.pdf)] [[сайт](http://3dshapenets.cs.princeton.edu/)] (2015) 3D ShapeNets: A Deep Representation for Volumetric Shapes**

- IN - 
- OUT - 
- COM - 2015 году трехмерное представление было не так уж популярно в распозновании объектов, однако с появленим недорогих датчиков глубины 2.5D, можно было иметь объемное представление модели

**[[статья](https://arxiv.org/pdf/2012.03927.pdf)] [[сайт](https://pratulsrinivasan.github.io/nerv/)] (DEC2020) NeRV: Neural Reflectance and Visibility Fields for Relighting and View Synthesis**

- IN - набор изображений, с непрерывным известным освещением.
- OUT - трехмерное представление объекта, с возможностью произвольного освещения и смены точки обзора
- COM - 

**[[статья](https://abhishekkar.info/categoryshapes.pdf)] Category-Specific Object Reconstruction from a Single Image**

**[[статья](https://www.dgpf.de/src/tagung/jt2019/proceedings/proceedings/papers/23_3LT2019_Schmohl_Soergel.pdf)] [[сайт](https://www.ifp.uni-stuttgart.de/en/research/remote_sensing/als_point_cloud_classification/)] ALS Klassifizierung mit Submanifold Sparse Convolutional Networks**

- COM - Вокселизация облака точек

**[[статья](https://arxiv.org/pdf/2001.06280v1.pdf)] (JAN2020) Review: deep learning on 3D point clouds**

**[[статья](https://sci-hub.se/10.1145/3150165.3150166)] (2017) Cloud-based collaborative 3D reconstruction using smartphones**  

**[[статья](https://arxiv.org/pdf/1809.03770.pdf)] (SEP2018) 3D Human Body Reconstruction from a Single Image via Volumetric Regression**

**[[статья](https://arxiv.org/pdf/1803.03352v1.pdf)] (MAR2018) Indoor Scene Understanding in 2.5/3D: A Survey**

**[[статья]()] [[код на Lua](https://github.com/Amir-Arsalan/Synthesize3DviaDepthOrSil)] Synthesizing 3D Shapes via Modeling Multi-View Depth Maps and Silhouettes with Deep Generative Networks**

**[[статья](https://arxiv.org/pdf/1804.05469.pdf)] (APR2018) Im2Struct: Recovering 3D Shape Structure from a Single RGB Image**

**[[статья](https://arxiv.org/pdf/1906.05113.pdf)] (APR2020) A Survey of Autonomous Driving: Common Practices and Emerging Technologies**

**[[статья](https://arxiv.org/pdf/2010.04595.pdf)] [[GitHub](https://github.com/alextrevithick/GRF)] (NOV2020) GRF: LEARNING A GENERAL RADIANCE FIELD FOR 3D SCENE REPRESENTATION AND RENDERING**

**[[статья](https://arxiv.org/pdf/2004.00452.pdf)] (APR2020) PIFuHD: Multi-Level Pixel-Aligned Implicit Function for High-Resolution 3D Human Digitization**

**[[статья](https://storage.googleapis.com/immersive-lf-video-siggraph2020/ImmersiveLightFieldVideoWithALayeredMeshRepresentation.pdf)] [[сайт](https://augmentedperception.github.io/deepviewvideo/)] Immersive Light Field Video with a Layered Mesh Representation**

<a name="links" />

## Дополнительные ссылки

<a name="habr" />

### Хабр:

**[[1](https://habr.com/ru/company/top3dshop/blog/511026/)] Обзор программного обеспечения для 3D-сканирования и обработки данных**

<a name="youtube" />

### YouTube:

**[[видео](https://www.youtube.com/watch?v=xEwKarW1ZF4)] (MAY2018) F8: How A.I. and Point Cloud Reconstruction Will Make VR Realistic**

**[[видео](https://www.youtube.com/watch?v=CBpZtnu1Mig)] (JUN2018) DIY 3D Scanner - Fully 3d printed photogrammetry rig**

**[[видео](https://www.youtube.com/watch?v=3Wq3vU6Ea6A)] (FEB2017) 3D printed 3D Scanner ... in action**

**[[видео](https://www.youtube.com/watch?v=bTp1DRfULII)] (MAY2015) Football Stadium 3D Evacuation Simulation**

**[[видео](https://www.youtube.com/watch?v=y9SMd9NwoC0)] (MAR2020) Crowd simulation in Unity3D DOTS. Density & Instance colors**

**[[видео](https://www.youtube.com/watch?v=9SVC7XBhBpk)] (APR2017) Implicit Crowd Simulation**

**[[видео](https://www.youtube.com/watch?v=dR5G5SNI5T4)] (MAY2015) Oasys Software - MassMotion, The World's Most Advanced Crowd Simulation Software**

**[[видео](https://www.youtube.com/watch?v=o1RbLLVwFTA&feature=emb_title)] (MAR2020) Unmanned Aerial Vehicle Path Planning for Exploration Mapping**

**[[видео](https://www.youtube.com/watch?v=-mQ60wNgKrQ&feature=youtu.be)] (NOV2020) The Beirut Port Explosions (English)**

**[[видео](https://www.youtube.com/watch?v=eCDBA_SbxCE)] (JUL2020) 3D Deep Learning with PyTorch3D by Nikhila Ravi**

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

