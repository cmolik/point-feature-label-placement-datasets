# Point feature label placement datasets
This repository provides datasets for point feature label placement.

## Datasets of Alexander Wolf

__Alexander Wolff__ has provided example point sets used for an experimental comparison of a simulated annealing algorithm, a greedy algorithm, and a rule-based algorithm for the point labeling problem. 

__Example Point Sets__

- DenseMap
- DenseRect
- RegularGrid
- HardGrid
- RandomMap
- RandomRect
- MunichDrillholes
- VariableDensity

__Real-world data stems from the following sources__

- 19461 drill holes in Munich [gzipped file with x-y-coordinates]
- 1041 American cities [file with coordinates and abbreviated names]
- 1158 American cities [file with coordinates and full names]
- 366 German railway stations [file with coordinates and names]
- 357 Tourist shops in Berlin [file with coordinates and names]

## Datasets of Luiz Antonio Nogueira Lorena
__Luiz Antonio Nogueira Lorena__ has provided map labeling datasets

- 25
- 100
- 250
- 500
- 750
- 1000

__Format__     
- line 1 : # of points
- line 2 : # of candidate positions (*)
- line 3 : # of labels in potential conflict with label 1 (degree of vertex 1)
- line 4 : labels in potential conflict with label 1
- line 5 : # of labels in potential conflict with label 2 (degree of vertex 2)
- line 6 : labels in potential conflict with label 2
- ......

(*)  # of labels = line 1  *  line 2
