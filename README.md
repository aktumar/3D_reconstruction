# 3D reconstruction
Небольшой литературный обзор по 3D реконструкции (Полезные ссылки, обзор связанных статей и результатов, личные заметки). Начало было положено в августе 2020 года. На создание подобного репо вдохновил - [:mage_man:](https://github.com/timzhang642/3D-Machine-Learning), а на исследование - [:mage_man:](https://www.cs.sfu.ca/~furukawa/) :)



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

**[[статья](http://3dshapenets.cs.princeton.edu/paper.pdf)] [[сайт](http://3dshapenets.cs.princeton.edu/)] (MAY2015) 3D ShapeNets: A Deep Representation for Volumetric Shapes**

<a name="1" />

- COM - Компьютерное зрение было создано 50 лет назад(?). Раньше трехмерное представление было не так уж популярно в распознавании объектов. Но появление датчиков глубины в 2.5D дали толчок на использование карт глубины (depth map) в распознавании объектов, такие как Sliding Shapes [[1](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#1)]. Такие датчики давали точную глубину, что сыграло важную роль для трехмерного представления в распознавании. Ну и в результате стало важно иметь трехмерное представление в современных системах компьютерного зрения. Впрочем и тут возникают другие проблемы, например, как выглядит невидимая часть модели?  Человек уже, как правило, имеет предварительное знание об определенных предметах. К примеру, ему не обязательно видеть, как выглядит обратная сторона вазы/машины и т.д., как выглядит здание, прикрытое растущим деревом, как выглядит человек со спины.. 





- COM1 - Оказывается существует множество теории о трехмерном представлений (3D representation), однако все ограничивается распознаванием отдельных экземпляров, к примеру сопоставление ключевых точек на основе `метода ближайших соседей`. Даже при таком раскладе трехмерное представление не использовалось в современных методах распознавания, в силу того что геометрическое представление было не точным.



<a name="2" />

- COM2 - В статье также говорится о синтезе форм и восстановлении [[2-4](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#2)] - что они ограничиваются сборкой на основе деталей (part-based assembly), да и удовольствие это дорогое. Но что касается вопроса трехмерного представления, то судя по описанию, им нужен управляемый данными способ изучения сложных распределенных форм из необработанных трехмерных данных по категориям и позициям объектов. А также автоматизированное обнаружение иерархического композиционного представления частей. (Ничего не понятно, но очень интересно :D - шутка - уйдет на разбор темы)

<p align="center"><img width="50%" src="https://github.com/aktumar/3D_reconstruction/blob/main/media/3D_ShapeNets:_A_Deep_Representation_for_Volumetric_Shapes.png" /></p>





- COM3 - В статье предлагается представить геометрическую трехмерную модель как распределение вероятностей двоичных переменных на трехмерной воксельной сетке, используя - Convolutional Deep Belief Network. 3D ShapeNets поддерживает распознавание образов по карте глубины 2.5D и просматривать планирование распознавания объектов, изучает распределение сложных трехмерных форм по разным категориям объектов и произвольным позициям на основе необработанных - CAD data. А также модель может автоматический обнаруживать иерархические представления композиционных частей.





- COM4 - Для обучения собственной модели 3D ShapeNets был создан большой датасет под названием ModelNet (a large-scale 3D CAD model dataset). В статье говорится что данное трехмерное представление позволяет повысить производительность по сравнению с современными технологиями (точнее современными они были 2015 годах, ведь сейчас считается что трехмерное представление уже не так актуально - Возможно(?))

**[[статья](https://arxiv.org/pdf/1709.06158.pdf)] [[сайт](https://niessner.github.io/Matterport/)] [[код](https://github.com/niessner/Matterport)] (SEP2017) Matterport3D: Learning from RGB-D Data in Indoor Environments**

<a name="theory"/>

### Теория

#### 2015

**[[статья](https://abhishekkar.info/categoryshapes.pdf)] (MAY2015) Category-Specific Object Reconstruction from a Single Image**

#### 2016

#### 2017

**[[статья](https://sci-hub.se/10.1145/3150165.3150166)] (2017) Cloud-based collaborative 3D reconstruction using smartphones**  

**[[статья](https://openaccess.thecvf.com/content_cvpr_2017/papers/Soltani_Synthesizing_3D_Shapes_CVPR_2017_paper.pdf)] (2017) Synthesizing 3D Shapes via Modeling Multi-View Depth Maps and Silhouettes with Deep Generative Networks [[код на Lua](https://github.com/Amir-Arsalan/Synthesize3DviaDepthOrSil)]**

#### 2018

**[[статья](https://arxiv.org/pdf/1803.03352v1.pdf)] (MAR2018) Indoor Scene Understanding in 2.5/3D: A Survey**

**[[статья](https://arxiv.org/pdf/1804.05469.pdf)] (APR2018) Im2Struct: Recovering 3D Shape Structure from a Single RGB Image**

**[[статья](https://arxiv.org/pdf/1809.03770.pdf)] (SEP2018) 3D Human Body Reconstruction from a Single Image via Volumetric Regression**

#### 2019

**[[статья](https://www.dgpf.de/src/tagung/jt2019/proceedings/proceedings/papers/23_3LT2019_Schmohl_Soergel.pdf)] (2019) ALS Klassifizierung mit Submanifold Sparse Convolutional Networks [[сайт](https://www.ifp.uni-stuttgart.de/en/research/remote_sensing/als_point_cloud_classification/)]**

- COM - Вокселизация облака точек

#### 2020

**[[статья](https://arxiv.org/pdf/2001.06280v1.pdf)] (JAN2020) Review: deep learning on 3D point clouds**

**[[статья](https://arxiv.org/pdf/2003.09754.pdf)] (MAR2020) Learning 3D Part Assembly from a Single Image [[сайт](https://cs.stanford.edu/~kaichun/impartass/)] [[код на Python](https://github.com/AntheaLi/3DPartAssembly)]** 

**[[статья](https://arxiv.org/pdf/1906.05113.pdf)] (APR2020) A Survey of Autonomous Driving: Common Practices and Emerging Technologies**

**[[статья](https://arxiv.org/pdf/2004.00452.pdf)] (APR2020) PIFuHD: Multi-Level Pixel-Aligned Implicit Function for High-Resolution 3D Human Digitization**

**[[статья](https://storage.googleapis.com/immersive-lf-video-siggraph2020/ImmersiveLightFieldVideoWithALayeredMeshRepresentation.pdf)] (JUL2020) Immersive Light Field Video with a Layered Mesh Representation [[сайт](https://augmentedperception.github.io/deepviewvideo/)]**

**[[статья](https://arxiv.org/pdf/2010.04595.pdf)] (NOV2020) GRF: LEARNING A GENERAL RADIANCE FIELD FOR 3D SCENE REPRESENTATION AND RENDERING [[GitHub](https://github.com/alextrevithick/GRF)]**

**[[статья](https://arxiv.org/pdf/2012.03927.pdf)] [[сайт](https://pratulsrinivasan.github.io/nerv/)] (DEC2020) NeRV: Neural Reflectance and Visibility Fields for Relighting and View Synthesis**

- IN - набор изображений, с непрерывным известным освещением.





- OUT - трехмерное представление объекта, с возможностью произвольного освещения и смены точки обзора





- COM - 

<a name="links" />

## Дополнительные ссылки

<a name="habr" />

### Хабр:

**[[1](https://habr.com/ru/company/top3dshop/blog/511026/)] Обзор программного обеспечения для 3D-сканирования и обработки данных**

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

