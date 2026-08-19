# Point feature label placement implementations and datasets
This repository provides links to available implementations of point feature label placement methods and datasets on which the methods can be evaluated.

# Implementations

[Mapnik](https://github.com/mapnik/mapnik) is an open-source toolkit written in C++ (with Python and Node APIs) for rendering high-quality, beautiful maps. It is best known as the primary rendering engine used by OpenStreetMap. It also contains a label placement engine.

[QGis](https://www.qgis.org/) is an open-source geographic information system that contains a label placement engine. 

Bobák et al. have provided their implementation of the Reinforced Labels [^BoCmCa24] at [https://github.com/PetrBo/reinforced-labels](https://github.com/PetrBo/reinforced-labels). 

Pavlovec and Čmolík have provided a Java implementation of Rapid Labels [^PaCm22] at [https://github.com/cmolik/rapid-labels](https://github.com/cmolik/rapid-labels). The project is using Maven, all required libraries are downloaded automatically. 

Martin Luboshik has provided a Java implementation of Particle-based Labeling [^LuSchCo08] at [https://sourceforge.net/projects/fpf-labeling/](https://sourceforge.net/projects/fpf-labeling/).

Ladislav Čmolík has provided a Java implementation where simple examples (without Lagrangean decomposition) are solved with ILP at [https://github.com/cmolik/ilp_labeling](https://github.com/cmolik/ilp_labeling). The same label configuration is addressed with different primary objectives (Label Number Maximization, Conflict-Free Label Maximization, and Label Conflict Minimization). Choco solver is used as the ILP solver. The project is using Maven, and all required libraries are downloaded automatically. 

[OpenLL](https://openll.org/) is a C++ library for high-quality text rendering on the GPU.

# Datasets

## Datasets for Rapid Labels

Pavlovec and Čmolík provided datasets for their greedy point-feature label placement algorithm [^PaCm22], which runs on a GPU. In their approach, users can specify regions where important features that cannot overlap with labels are located. The regions where important features are located are provided as an additional input to the algorithm as an image, along with the positions and names of the point features and a background image on which the labels are positioned.

- [ConnectedScatterplot](Rapid%20Labels/ConnectedScatterplot), [zip file](Rapid%20Labels/ConnectedScatterplot.zip)
- [USAirports](Rapid%20Labels/USAirports), [zip file](Rapid%20Labels/USAirports.zip)


## Datasets for Reinforced Labels 

Bobák et al. provided datasets for testing their point-feature label placement algorithm [^BoCmCa24], which leverages reinforcement learning.

__Example Point Sets__

- [Compact](Reinforced%20Labels/compact), [zip file](Reinforced%20Labels/compact.zip)
- [Volume](Reinforced%20Labels/volume), [zip fie](Reinforced%20Labels/volume.zip)

__Real-world data__

- [City_150](Reinforced%20Labels/city_150), [zip file](Reinforced%20Labels/city_150.zip)
- [IATA_Airports_250](Reinforced%20Labels/iata_airports_250), [zip file](Reinforced%20Labels/iata_airports_250.zip)

__Format__

Each dataset is represented by a JSON file with two main sections. The first section contains information about the final image's resolution and an optional link to the background image. The second section contains a sequence of point features. For each point feature, there is information about its coordinates in the final image, the label width and height, the label text, and the font family, style, and size.

## Datasets of Alexander Wolf

__Alexander Wolff__ has provided example point sets used for an experimental comparison of a simulated annealing algorithm, a greedy algorithm, and a rule-based algorithm for the point labeling problem by Wagner and
Wolff [^WaWo98]. The page is accessible only via [web.archive.org](https://web.archive.org/web/20220620004211/https://i11www.iti.kit.edu/~awolff/map-labeling/general/); therefore, we provide mirrors of the data files below. 

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
__Luiz Antonio Nogueira Lorena__ has provided map labeling datasets used for evaluation by Yamamoto and Lorena [^YaLo05] and Ribeiro and Lorena [^RiLo08]. The page is accessible only via [web.archive.org](https://web.archive.org/web/20251209080024/http://www.lac.inpe.br/~lorena/instancias.html). We provide mirrors of the data files below. 

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

### References
[^BoCmCa24]: Bobák, P, Čmolík, L, Čadík, M. Reinforced labels: Multi-agent deep reinforcement learning for point-feature label placement. IEEE Transactions on Visualization and Computer Graphics 2024;30(9):5908–5922. doi:[10.1109/TVCG.2023.3313729](https://doi.org/10.1109/TVCG.2023.3313729).
[^LuSchCo08]: Luboschik, M, Schumann, H, Cords, H. Particle-based labeling: Fast point-feature labeling without obscuring other visual features. IEEE Transactions on Visualization and Computer Graphics 2008;14(6):1237–1244. doi:[10.1109/TVCG.2008.152](https://doi.org/10.1109/TVCG.2008.152).
[^PaCm22]: Pavlovec, V, Čmolík, L. Rapid labels: Point-feature labeling on GPU. IEEE Transactions on Visualization and Computer Graphics 2022;28(1):604–613. doi:[10.1109/TVCG.2021.3114854](https://doi.org/10.1109/TVCG.2021.3114854).
[^RiLo08]: Ribeiro, GM, Lorena, LAN. Lagrangean relaxation with clusters for point-feature cartographic label placement problems. Computers and Operations Research 2008;35:2129–2140. doi:[10.1016/j.cor.2006.09.024](https://doi.org/10.1016/j.cor.2006.09.024).
[^WaWo98]: Wagner, F, Wolff, A. A combinatorial framework for map labeling. In: International Symposium on Graph Drawing. Springer; 1998, p. 316–331. doi:[10.1007/3-540-37623-2_24](https://doi.org/10.1007/3-540-37623-2_24)
[^YaLo05]: Yamamoto, M, Lorena, LA. A constructive genetic approach to point-feature cartographic label placement. In: Metaheuristics: Progress as real problem solvers. Springer; 2005, p. 287–302. doi:[10.1007/0-387-25383-1_13](https://doi.org/10.1007/0-387-25383-1_13)
