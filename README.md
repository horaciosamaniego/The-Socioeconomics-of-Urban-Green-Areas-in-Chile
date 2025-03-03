# The-Socioeconomics-of-Urban-Green-Areas-in-Chile

Greeness (NDVI) and Socioeconomics of Green Urban Areas in Chile 

bioArXiv

## Description of the data and file structure

Data contains all Green Urban Areas of the six major urban cities in Chile. It shows the mean NDVI, ISMT (Socioeconoimic stratification) and on'hour slot entropy of visitation across the ISMT quartiles.

> ==> Table_entropy.csv <==
> Columns are one-hour slots
> ID: GUA identifier

> ==> Table_parks.csv <==
> CITY: The Urban Area
> ID: GUA identifier
> NAME: Name of the GUA, if available
> COORD: UTM 19S WGS  1984 geographic coordinates
> QUALITY_INDEX: Index extracted from Flores 2019 for each GUA
> ISMT: Socioeconomic Statification Value
> ISMT_LEVEL: ISMT Quartile (0<= Q1 <0.25 Low, 0.25<= Q2 < 0.5 Medium Low, 0.5<= Q3 <0.75 Medium High, Q4 >= 0.75 High)

## Materials and Methods (extracted from the paper)

2. Materials and Methods

This study analyzes the six largest urban areas in Chile, which are located between 23°S and 41°S (see Fig. 1). These cities—the largest conurbations spanning different climatic regions (Di Castri et al., 1976; Flores A, 2019)—include Antofagasta, Coquimbo-La Serena, Valpara´ıso, Santiago, Concepci´on, and Puerto Montt.

We use the official database of parks and green areas developed by the Chilean Institute of Statistics, which provides data on surface area, quality, and other attributes of public green spaces across municipalities (Flores A, 2019). The quality of public parks is assessed using a Quality Index (QI) designed to rank parks based on the services they provide. This index evaluates five infrastructural components: general maintenance, type of vegetation, universal accessibility, safety, and diversity of facilities. In this study, the Quality Index is employed to analyze daily usage patterns of these public spaces.

Greenness is characterized using remote sensing imagery and quantified with the Normalized Difference Vegetation Index (NDVI), which calculates vegetation density as the ratio between the near-infrared and red bands of the electromagnetic spectrum. Higher NDVI values generally correspond to a greater fraction of photosynthetically active radiation, indicating greener, more vigorous vegetation and denser plant cover (Pettorelli et al., 2005). NDVI was computed from the Landsat 8 catalog via the Google Earth Engine platform (Gorelick et al., 2017) and is widely used to study vegetation cover in urban areas (Jenerette et al., 2011; Stefanov and Netzband, 2005). Each public park was further classified into low, medium, or high greenness categories based on its mean NDVI value relative to the citywide terciles.

Socioeconomic levels were classified using the Sociomaterial Territorial Index (ISMT), derived from the 2017 Census of Population and Housing (Observatorio de Ciudades UC, 2022). The ISMT considers the educational level of the household head, housing quality (wall, roof, and floor condition), overcrowding (persons per bedroom), and cohabitation (number of family groups per dwelling) (CASEN, 2017). Each park was assigned the ISMT value of its corresponding census zone. For parks spanning multiple zones, a weighted average ISMT was calculated based on the relative area within each zone.

To assess the activity space related to public parks, we analyzed the frequency of visits to areas surrounding these spaces. As a proxy for urban mobility, we used the eXtended Call Detail Records (XDR) from MOVISTAR, a major mobile phone provider in Chile (see Dannemann et al., 2018; Lenormand and Samaniego, 2023, for similar procedures). The dataset covers four weeks in March, May, and October 2015 and was selected to represent typical weeks without extraordinary events that might disrupt normal social and economic patterns. Each record was geolocated to a specific antenna. Like traditional Call Detail Records, XDR tracks all data activity from mobile phones connecting to nearby antennas, thereby enabling us to map individual movements throughout the city (Blondel et al., 2015).

Each city was divided into Voronoi cells to pinpoint users’ activities geographically. We then estimated the number of individuals connecting to antennas associated with public parks in one-hour intervals. Furthermore, we inferred each individual’s socioeconomic status based on their presumed residence, following the approach of Vanhoof et al. (2018). Presumed residences were defined as the most frequently visited locations between PM and 7 AM, with at least five records during that period. Individuals without a determinable residence were excluded from the analysis. The data provider anonymized all records to ensure user privacy.

We categorized individuals’ socioeconomic status into four groups—low, medium low, medium high, and high—based on their ISMT quartiles within each city (Table 1). A similar procedure was applied to each park, assigning an ISMT quartile accordingly. This classification enabled us to label all public parks and individuals according to their respective socioeconomic groups.

We estimated the number of antennas near parks by identifying the overlap between Voronoi cells and public parks. Although this method does not precisely determine whether individuals are using park facilities, it enables analysis of a large dataset that accounts for the socioeconomic stratification of individuals passing by or near green urban areas.

This approach is feasible because mobile phones connect to antennas (or “ping”) multiple times when accessing the internet (e.g., when retrieving messages), with each ping linked to the specific location of the corresponding antenna at that time.

Sankey flow diagrams were employed to qualitatively assess the association between parks’ socioeconomic status, greenness, and the Quality Index (Lupton and Allwood, 2017). Analysis of variance (ANOVA) was used to assess the effect of the classified socioeconomic status of public parks on their average greenness. The most significant differences were identified using a Tukey post-hoc test (Quinn and Keough, 2002).

We used entropy (H) as an indicator of social mixing-a measure often associated with social segregation (Massey et al., 1996; Lenormand et al., 2020; Batty, 2020). For each city, H was computed across the four socioeconomic quartiles on an hourly basis, enabling the construction of a time series that tracks changes in social mixing among public park visitors. This 24-hour time series was then analyzed for parks across different greenness terciles and ISMT quartiles. A simple Chi-square test was applied to evaluate whether socioeconomic levels were evenly distributed across greenness categories.

Finally, a cluster analysis was performed using Euclidean distances on the H time series of public parks larger than 0.5 ha. This analysis evaluated whether parks exhibiting similar temporal changes in H also shared comparable Quality Index (QI), socioeconomic status (as measured by ISMT), and greenness (NDVI). The resulting dendrograms were arbitrarily pruned to yield the four most relevant clusters.
