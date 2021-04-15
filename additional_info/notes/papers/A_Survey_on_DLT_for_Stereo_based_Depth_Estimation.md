```
A Survey on Deep Learning Techniques for Stereo-based Depth Estimation


```

<a name="1" />

- **COM1** - В период с 2014 по 2019 год в области "Глубокого обучения для оценки глубины на основе стерео" **было опубликовано** более 150 статей. Можно сказать, что данная область, как и "Трехмерная реконструкция на основе изображений с использованием CNN" начиная с 2015 года вызывает большой интерес, а новые методы/подходы демонстрируют значительный скачок в производительности, что позволяет работать с такими приложениями как: автономное вождение, дополненная реальность. (JUN2020) еще существует проблема: текстурированных областей, больших однородных областей и окклюзий. 

<a name="2" />

- **COM2** - Методы **стереопоставления** тесно связаны с бинокулярной системой человека - способностью одновременно четко видеть изображение предмета обоими глазами. Также, его называют стереоскопическим. Физиологический механизм зрения, называемый *фузии*, что означает слияние зрительных образов, возникающих отдельно в каждом глазу в единое сочетанное зрительное восприятие.

<a name="3" />

- **COM3** - **Оценка глубины** цветных изображений (как и 3D реконструкция в других статьях этого авторов) - это давняя некорректно поставленная проблема, которая десятилетиями изучалась сообществами *компьютерного зрения*, *графики* и *машинного обучения*. Идея оценки глубины на основе стерео - сопоставление созданных вручную функций на нескольких изображениях.

   

<a name="4" />

- **COM4** - 

<a name="5" />

- **COM5** - 

<a name="6" />

- **COM6** - 

<a name="7" />

- **COM7** - 

<a name="8" />

- **COM8** - 

<a name="9" />

- **COM9** - 

<a name="10" />

- **COM10** - 



```
A Survey on Deep Learning Techniques for Stereo-based Depth Estimation

1. Introduction
2. Scope and Taxonomy
3. Datasets
	(1) Dataset size
	(2) Spatial and depth resolutions
	(3) Euclidean vs. ordinal depth
	(4) Domain gap
4. Depth by stereo matching
	4.1 Learning feature extraction and matching
		4.1.1 The basic network architecture
		4.1.2 Network architecture variants
		4.1.3 Training procedures
	4.2 Regularization and disparity estimation
5 End-to-end depth from stereo
	5.1 Feature learning
	5.2 Cost volume construction
		5.2.1 3D cost volumes
		5.2.2 4D cost volumes
		5.2.3 Hybrid 3D-4D cost volumes
	5.3 Disparity computation
	5.4 Variants
		5.4.1 Learning to infer high resolution disparity maps
		5.4.2 Learning for completion and denoising
		5.4.3 Learning for realtime processing
	5.5 Learning confidence maps
		5.5.1 Confidence from left-right consistency check
		5.5.2 Confidence from a single raw disparity map
		5.5.3 Confidence map from matching densities
		5.5.4 Local vs. global reasoning
		5.5.5 Combining multiple estimators
6 Learning multiview stereo
	6.1 Volumetric representations
	6.2 Plane-Sweep Volume representations
7 Training end-to-end stereo methods
	7.1 Supervision methods
		7.1.1 3D supervision methods
		7.1.2 Self-supervised methods
		7.1.3 Weakly supervised methods
	7.2 Incorporating additional cues
	7.3 Domain adaptation and transfer learning
		7.3.1 Adaptation by fine-tuning
		7.3.2 Adaptation by data transformation
	7.4 Learning the network architecture
8 Discussion and comparison
	8.1 Evaluation protocol
	8.2 Computation time and memory footprint
	8.3 Reconstruction accuracy
9 Future research directions
10 Conclusion
```
