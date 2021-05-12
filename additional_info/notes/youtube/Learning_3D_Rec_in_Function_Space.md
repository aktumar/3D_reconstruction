- COM1 - Исследование нейронных неявных представлений. То что я знала до этого (воксели и облака точек) - плюс сетка(меш) - является традиционной концепцией трехмерного представления явным образом.

  ```mermaid
  graph LR;    
  A[Трехмерное представлние]--> B[Неявным образом];    
  A-->C[Явным образом];    
  C-->D[Воксели];
  C-->E[Облака точек];
  C-->F[Сетка-меш];
  D-->G(Дискретизация пространства в регулярную сетку<br> Легко обрабатывать с помощью нейронных сетей <br>Кубическая память - ограниченное разрешение <br>);
  E-->H(Дискретизация пространства в точки <br>Не моделирует топологию <br>Ограниченное количество точек <br>Глобальное описание)
  F-->I(Дискретизация на вершины и грани<br>Ограниченное количество вершин<br>Нужен шаблон конкретного класса<br>Проблема самопересечения)
  
  B-->J(Нет дискретизации<br>Произвольная топология<br>Маленький объем<br>Не ограничивается классом)
  ```





- COM2 - *Traditional 3D Reconstruction Pipeline*

  Input Images → Camera poses → Dense Correspondences → 3D reconsruction → Depth Map Fusion → Depth Maps





- COM3 - *What is a good output representation?*

  <p align="center"><img width="100%" src="https://github.com/aktumar/3D_reconstruction/blob/main/media/Learning_3D_Rec_in_Function_Space.png" /></p>

  | Voxels                                                       | Points                                   | Meshes                                   |
  | ------------------------------------------------------------ | ---------------------------------------- | ---------------------------------------- |
  | Discretization of 3D space into regular grid                 | Discretization of surface into 3D points | Discretization into vertices and faces   |
  | Easy to process with neural networks                         | Does not model connectivaly / topology   | Limited number of vertices / granularity |
  | Cubic memory O(n^3) - limited resolurion                     | Limited number of points                 | Requires class-specific template - or -  |
  | Manhattan world bias [[12](https://github.com/aktumar/3D_reconstruction/blob/main/additional_info/references.md#8)] | Global shape description                 | Leads to self-intersections              |





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

