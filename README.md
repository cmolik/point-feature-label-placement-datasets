# Point feature label placement datasets
This repository provides datasets for point feature label placement.

## Datasets for Rapid Labels

Pavlovec and Čmolík provided datasets for their greedy point-feature label placement algorithm, which runs on a GPU. In their approach, users can specify regions where important features that cannot be overlapped by labels are located. The regions where important features are located are provided as an additional input to the algorithm in the form of an image, together with the positions and names of the point features, and a background image over which the labels are positioned.

- [ConnectedScatterplot](Rapid%20Labels/ConnectedScatterplot), [zip file](Rapid%20Labels/ConnectedScatterplot.zip)
- [USAirports](Rapid%20Labels/USAirports), [zip file](Rapid%20Labels/USAirports.zip)


## Datasets for Reinforced Labels 

Bobák et al. provided datasets for testing their point-feature label placement algorithm leveraging reinforcement learning.

__Example Point Sets__

- [Compact](Reinforced%20Labels/compact), [zip file](Reinforced%20Labels/compact.zip)
- [Volume](Reinforced%20Labels/volume), [zip fie](Reinforced%20Labels/volume.zip)

__Real-world data stems from the following sources__

- [City_150](Reinforced%20Labels/city_150), [zip file](Reinforced%20Labels/city_150.zip)
- [IATA_Airports_250](Reinforced%20Labels/iata_airports_250), [zip file](Reinforced%20Labels/iata_airports_250.zip)

__Format__

Each dataset is represented by a JSON file with two main sections. The first section contains information about the final image's resolution and an optional link to the background image. The second section contains a sequence of point features. For each point feature, there is information about its coordinates in the final image, the label width and height, the label text, and the font family, style and size.

## Datasets of Alexander Wolf

__Alexander Wolff__ has provided example point sets used for an experimental comparison of a simulated annealing algorithm, a greedy algorithm, and a rule-based algorithm for the point labeling problem. The page is accessible only via [web.archive.org](https://web.archive.org/web/20220620004211/https://i11www.iti.kit.edu/~awolff/map-labeling/general/); therefore, we provide mirrors of the data files below. 

__Example Point Sets__

- [DenseMap](Alexander%20Wolff/DenseMap.tar.gz)
- [DenseRect](Alexander%20Wolff/DenseRect.tar.gz)
- [RegularGrid](Alexander%20Wolff/RegularGrid.tar.gz)
- [HardGrid](Alexander%20Wolff/HardGrid.tar.gz)
- [RandomMap](Alexander%20Wolff/RandomMap.tar.gz)
- [RandomRect](Alexander%20Wolff/RandomRect.tar.gz)
- [MunichDrillholes](Alexander%20Wolff/MunichDrillholes.tar.gz)
- [VariableDensity](Alexander%20Wolff/VariableDensity.tar.gz)

__Real-world data stems from the following sources__

- 19461 drill holes in Munich [gzipped file with x-y-coordinates](Alexander%20Wolff/munich_drill_19461.xy.gz)
- 1041 American cities [file with coordinates and abbreviated names](Alexander%20Wolff/us_abbrev_1041.xyn)
- 1158 American cities [file with coordinates and full names](Alexander%20Wolff/us_cities_1158.xyn)
- 366 German railway stations [file with coordinates and names](Alexander%20Wolff/german_railway_366.xyn)
- 357 Tourist shops in Berlin [file with coordinates and names](Alexander%20Wolff/berlin_shops_357.xyn)

## Datasets of Luiz Antonio Nogueira Lorena
__Luiz Antonio Nogueira Lorena__ has provided map labeling datasets. The page is accessible only via [web.archive.org](https://web.archive.org/web/20251209080024/http://www.lac.inpe.br/~lorena/instancias.html). We provide mirrors of the data files below. 

- [25](Luiz%20Antonio%20Nogueira%20Lorena/d25.zip)
- [100](Luiz%20Antonio%20Nogueira%20Lorena/d100.zip)
- [250](Luiz%20Antonio%20Nogueira%20Lorena/d250.zip)
- [500](Luiz%20Antonio%20Nogueira%20Lorena/d500.zip)
- [750](Luiz%20Antonio%20Nogueira%20Lorena/d750.zip)
- [1000](Luiz%20Antonio%20Nogueira%20Lorena/d1000.zip)

__Format__     
- line 1: # of points
- line 2: # of candidate positions (*)
- line 3: # of labels in potential conflict with label 1 (degree of vertex 1)
- line 4: labels in potential conflict with label 1
- line 5: # of labels in potential conflict with label 2 (degree of vertex 2)
- line 6: labels in potential conflict with label 2
- ......

(*)  # of labels = line 1  *  line 2
