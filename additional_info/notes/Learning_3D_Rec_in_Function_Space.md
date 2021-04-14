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

