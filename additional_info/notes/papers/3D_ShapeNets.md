```
ShapeNets: A Deep Representation for Volumetric Shapes

COM1: Компьютерное зрение
COM2: Трехмерное представление
COM3: 3D ShapeNets
COM4: Датасет - ModelNet
COM5: Related works

COM6: Подходы применяемые для 2D формы
COM7: Convolutional Deep Belief Network (CDBN)
COM8: View-based 2.5D Object Recognition
COM9: Next-Best-View
COM10: Воксели

COM11: Эксперимент

```



<a name="1" />

- **COM1** - **Компьютерное зрение** было создано 50 лет назад (:mag_right:). Раньше трехмерное представление было не так уж популярно в распознавании объектов. Но появление датчиков глубины в 2.5D дали толчок на использование карт глубины (depth map) в распознавании объектов, такие как Sliding Shapes [[1](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#1)]. Такие датчики давали точную глубину, что сыграло важную роль для трехмерного представления в распознавании. Ну и в результате стало важно иметь трехмерное представление в современных системах компьютерного зрения. Впрочем и тут возникают другие проблемы, например, как выглядит невидимая часть модели?  Человек уже, как правило, имеет предварительное знание об определенных предметах. К примеру, ему не обязательно видеть, как выглядит обратная сторона вазы/машины и т.д., как выглядит здание, прикрытое растущим деревом, как выглядит человек со спины.. 



<a name="2" />

- **COM2** - Оказывается существует множество теории о **трехмерном представлений** (3D representation), однако все ограничивается распознаванием отдельных экземпляров, к примеру сопоставление ключевых точек на основе `метода ближайших соседей`. Даже при таком раскладе трехмерное представление не использовалось в современных методах распознавания, в силу того что геометрическое представление было не точным. В статье также говорится о синтезе форм и восстановлении [[2-4](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#2)] - что они ограничиваются сборкой на основе деталей (part-based assembly), да и удовольствие это дорогое. Но что касается вопроса трехмерного представления, то судя по описанию, им нужен управляемый данными способ изучения сложных распределенных форм из необработанных трехмерных данных по категориям и позициям объектов. А также автоматизированное обнаружение иерархического композиционного представления частей. (Ничего не понятно, но очень интересно :D - шутка - уйдет на разбор темы :mag_right:)



<a name="3" />

- **COM3** - **3D ShapeNets** поддерживает распознавание образов по карте глубины 2.5D и просматривать планирование распознавания объектов, изучает распределение сложных трехмерных форм по разным категориям объектов и произвольным позициям на основе необработанных - CAD data. (We demonstrate the strength of our model at capturing complex object shapes by drawing samples from the model :mag_right:) 3D ShapeNets хорошо обобщается на данные реального мира из набора данных глубины NYU [[5](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#3)].

  <p align="center"><img width="50%" src="https://github.com/aktumar/3D_reconstruction/blob/main/media/3D_ShapeNets.png" /></p>

  IN - Карта глубины объекта, которая в свою очередь проходит предварительное преобразование в трехмерное представление

  OUT - Распознавание категории объекта

  OUT - Составление полной трехмерной формы

  OUT - Предсказание самого оптимального следующего ракурса, в случае непонятного первоначального вида и недостающих частей

  OUT - Интегрирование картинок с новых ракурсов совместно с остальными :mag_right:

  

  

  Каждое трехмерное представление (через воксели) имеет двоичный вид: 1 - воксель находится внутри поверхности сетки, 0 - воксель находится вне сетки. У авторов эти сетки ограничены размером 30х30х30.

  

<a name="9"/>

- **COM4** - Для обучения собственной модели 3D ShapeNets был создан большой **датасет под названием ModelNet** (a large-scale object dataset of 3D computer graphics CAD models). В статье говорится что данное трехмерное представление позволяет повысить производительность по сравнению с современными технологиями (точнее современными они были 2015 годах, ведь сейчас считается что трехмерное представление (voxel) уже не так актуально - Возможно :mag_right:) 

  Альтернатива - [[13](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#9)], но с меньшим количеством данных, 3D CAD models из 3D Warehouse, Yobi3D search engine indexing 261 CAD model websites, SUN database [[14](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#9)] (660 категорий, 20 экземпляров на категорию), Princeton Shape Benchmark [[15](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#9)]. After downloading, we remove miscategorized models using Amazon Mechanical Turk.

  Затем авторы вручную проверили каждую 3D-модель и удалили нерелевантные объекты из каждой модели САПР (например, пол, миниатюрное изображение, человека, стоящего рядом с объектом и т.д.), чтобы каждая модель сетки содержала только один объект, принадлежащий помеченной категории. Они также отказались от нереалистичных (чрезмерно упрощенных моделей или содержащих только изображения объекта) и повторяющихся моделей. Новый набор данных ModelNet содержит 151 128 3D-моделей САПР (660 категорий объектов).
  
  <p align="center"><img width="80%" src="https://github.com/aktumar/3D_reconstruction/blob/main/media/3D_ShapeNets_5.png" /></p>



<a name="4" />

- **COM5** - В статье описываются исследования (**related works**) по теме - 3D CAD model collections [[2-4](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#2)]. В этих работах в основном  используется `подход на основе сборки для построения моделей из деформируемых деталей`. Но в этом подходе есть недостаток - ограничение определенным классом форм (соответствие поверхности). В нашем же случае, мы должны подстраиваться под разные трехмерные представления, не зависимо от того, есть ли для него соответствующий класс. Да и представление каждой детали по отдельности довольно трудоемкая и затратная работа. Есть другие `подходы основанные на гладкой интерполяции или экстраполяции`, которые позволяют устранить только небольшие дыры или недостатки [[6-7](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#4)]. Методы, `основанные на шаблонах` [[4](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#2)], могут справиться с большими поверхностными повреждениями, но ограничены качеством доступных шаблонов, и не могут обеспечивать различные семантические интерпретации реконструкций. 



<a name="5" />

- **COM6** - Для сравнения в статье говорится, что многие **подходы применяемые для двумерной формы** (например, рукопись, распознавание лица и т.д.) могут стать отличной базой для восстановления трехмерной формы. Авторы статьи первые, кто начал работу над созданием трехмерных моделей глубокого обучения. Для возможности работы с большим количеством вокселей они применили технику свертки, как в [[8](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#5)]. Также их модель похожа на работы [[8-9](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#5)], которые создают дискриминантные сверточные нейронные сети для 2.5D глубокого обучения, чтобы моделировать изображения и карту глубины. 

  Для сравнения существует DBN (Deep Belief Networks), представляющий мощный класс вероятностных моделей, **но для 2D изображений**. По сути здесь происходит некая адаптация модели с 2D на 3D (с пикселей на воксели), но со сменой измерения можно столкнуться с кучей других проблем. Можно испугаться достаточно большого объема данных, как никак трехмерное представление, однако для сравнения воксельная сетка размером 30х30х30 будет иметь такой же размер что и изображение размера 165х165. Но вопрос в другом, достаточно ли такого количества вокселей, для того чтобы определить принадлежность объекта к какому нибудь классу. Если использовать DBN уже для трехмерного представления. то обучение окажется трудоемкой и неэффективной. 





- **COM7** - Поэтому в статье предлагается представить геометрическую трехмерную модель как вероятностное распределение двоичных переменных на трехмерной воксельной сетке, используя - **Convolutional Deep Belief Network** (CDBN) (Визуализация, управляемая данными:mag_right: - да и уровни представлены довольно таки интересно, от простых до самых сложных по форме объектов: разработка самих авторов CDBN - лучше почитать по-подробнее).

  <p align="center"><img width="30%" src="https://github.com/aktumar/3D_reconstruction/blob/main/media/3D_ShapeNets_2.png" /></p>

  Этот рисунок иллюстрирует архитектуру 3D ShapeNets, а трехмерная фигура представлена в виде сетки 24х24х24 (with 3 extra cells of padding in both directions to reduce the convolution border artifacts :mag_right:) (K softmax variables :mag_right:).

  1) Первый слой состоит из 48 фильтров (размер 6, шаг 2)

  2) Второй слой состоит из 160 фильтров (размер 5, шаг 2) - каждый фильтр имеет 48х5х5х5 параметров :mag_right:
  
  3) Третий слой состоит из 512 фильтров (размер 4, шаг 1)
  
  4) Четвертый уровень - стандартный полностью подключенный RBM (Restricted Boltzmann machine :mag_right:) с 1200 скрытыми элементами

  5) Пятый уровень - слой с 4000 скрытыми элементами. В качестве входных данных принимает комбинацию полиномиальных переменных-меток и переменных свойств Бернулли. 

  <a name="7" />
  
  П.С. Каждый фильтр свертки связан характеристическими каналами предыдущего слоя. Как только нижний уровень изучен, веса фиксируются, и скрытые активации передаются на следующий уровень в качестве входных данных. (`Wake sleep algorithm` [[11](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#7)])
  
  - В фазе пробуждения они распространяют данные снизу вверх и используют активации для сбора *положительного* обучающего сигнала
  - В фазе сна они поддерживают постоянную цепочку на самом верхнем уровне и распространяют данные сверху вниз для сбора `отрицательного` обучающего сигнала
  
  П.С.С. The top layer forms an associative memory DBN as indicated by the bi-directional arrows, while all the other layer connections are directed top-down.
  
  П.С.С.С. Первые 4 слоя обучаются с использованием `стандартной контрастной дивергенции`, а последний - `быстрой постоянной контрастной дивергенции (FPCD)`.
  
  П.С.С.С.С. Во время предварительного обучения первого слоя они собирают обучающий сигнал только в непустых рецептивных полях, так как пустые могут отвлекать обучение, а игнорирование пустых сигналов помогает модели обучаться более значимым фильтрам. Также для первого уровня они добавили регуляризацию разряженности, чтобы ограничить среднюю активацию скрытых единиц небольшой константой. 
  
  
  
  В отличие от обычных сверточных моделей глубокого обучения, авторы не используют какую-либо форму объединения в скрытых слоях. (Однако, по их мнению, объединение могло бы улучшить свойства инвариантности для распознавания :mag_right:)
  
  
  
- **COM8** - После обучения CDBN, модель изучает joint distribution /-p(x,y)-/, где x - воксельные данные, y - метки категории объекта /-y ∈ {1, · · ·, K}-/. По сути модель обучается на трехмерных фигурах, но она способна также распознавать объекты на картах глубины 2.5D (например датчики RGB-D). В статье это называют **View-based 2.5D Object Recognition**.

  <p align="center"><img width="100%" src="https://github.com/aktumar/3D_reconstruction/blob/main/media/3D_ShapeNets_3.png" /></p>

  1. Иллюстрация физического объекта в трехмерном пространстве
  2. Одно изображение глубины со спинки стула
  3. Профиль среза и воксели (поверхностные воксели - красным/-x_0-/, окклюзивные воксели - синим/-x_u-/)
  4. Результат

  То есть карта глубины 2.5D сначала преобразуется в объемное представление, классифицируется в воксели (free space, front or behind the visible surface), где free space и фронт часть наблюдаются при обучении/-x_0-/, а закрытые воксели считаются недостающими данными /-x_u-/. Оценка распознавания категорий объекта - /-p(y|x_0)-/ - (Понять математику, здесь мясо, posterior distribution :mag_right: - 5 стр). 

  

  <a name="10" />

  В качестве базового подхода мы используем сопоставление `k-ближайших соседей` в нашем пространстве вокселей с низким разрешением. Карты глубины тестирования преобразуются в представление вокселей и сравниваются с каждой из обучающих выборок. В качестве более сложной базовой линии с высоким разрешением мы сопоставляем облако точек тестирования с каждой из наших 3D-моделей сетки, используя метод `Iterated Closest Point` [[16](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#10)], и используем 10 лучших совпадений для голосования за метки.

  

  

  Мы также сравниваем наш результат с [[8](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#5)], которая представляет собой современную модель глубокого обучения, применяемую к данным RGB-D.

  

  <a name="6" />

- **COM9** - В статье затрагивается проблема **Next-Best-View** [[7](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#4)] - планирование просмотра на основе текущего наблюдения - можно увидеть ссылки на другие работы с различными вариантами решения (к примеру, большинство работ `основывается на цветовой информации изображения`, но их проблема в том что они работают исключительно с двумерным представлением. Почитать про: распознавание на уровне экземпляра без внутриклассовой дисперсии - instance-level recognition with no intra-class variance :mag_right:; на точном уровне вокселов - precise voxel level :mag_right:). Датчик распознавания активных объектов [[10](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#6)] может перемещаться к новым точкам обзора, в отличие от распознавания статических объектов.

  Можно выбрать множество форм для генерации гипотез фактической модели, и визуализировать каждую гипотезу для получения карт глубины c разных точек наблюдения. Поскольку фактическая форма частично неизвестна, эта область галлюцинируется из модели. 

  <p align="center"><img width="50%" src="https://github.com/aktumar/3D_reconstruction/blob/main/media/3D_ShapeNets_4.png" /></p>

  IN - Наблюдаемые воксели /-x_0-/ неизвестного объекта.
  
  OUT - Список возможных перемещений камеры в пространстве /-{V^i}-/, где выбирается более подходящий вариант для уменьшения неопределенности распознавания. При этом имея все те же /-x_0-/, от этого достоверность не растет. (Формула на 5 стр.) (Энтропия :mag_right:) После выбора лучшего варианта они физически перемещают камеру на новую позицию и снимают другую поверхность объекта с этого вида. Поверхности объектов из всех предыдущих видов объединяются вместе в виде нового наблюдения /-x_0-/. (information theory - :mag_right:)
  





- **COM10** - В трехмерной области **воксели** способствуют снижению неопределенности распознавания 





- **COM11** - Для **эксперимента** были использованы 40 категорий (100 уникальных экземпляров в каждой категорий) из ModelNet. Затем они  дополняли данные, поворачивая каждую модель на 30 градусов (:mag_right:), получив 12 поз. На обучение и настройку ушло около 2 дней. Характеристика стационарного компьютера: Intel XEON E5-2690 CPU и NVIDIA K40c GPU. 



```
ShapeNets: A Deep Representation for Volumetric Shapes

1. Introduction
2. Related Work
3. 3D ShapeNets
4. 2.5D Recognition and Reconstruction
   4.1. View-based Sampling
   4.2. Next-Best-View Prediction
5. ModelNet: A Large-scale 3D CAD Dataset
6. Experiments
   6.1. 3D Shape Classification and Retrieval
   6.2. View-based 2.5D Recognition
   6.3. Next-Best-View Prediction
7. Conclusion
   References
```
