# Geospatial Point of Interest Analysis

There's a lot of open data available about the demographics and geography of the planet. But this information is not necessarily supervised in any particular structure from which insights can be drawn.

This project create clusters of distinct commercial centers or markets using points of interest data of a city (the city could be yours). Points of interest (POI) data provides location information of different places along with their defining tags like hotels, type of shops, type of amenities, etc.


## Getting Started

The jupyter notebook is easily rendered over Github so you don't have to do anything specific. But the Folium Maps which are used here will not be rendered here on github, so download all the 'htlm' files from Map folder and open on Chrome Browser or run the notebook locally.

### Getting the Data

Getting an open source map which have all the attributes. 
Open Source Map (OSM): (https://www.openstreetmap.org/#map=11/28.6518/77.2219) is the open source to get all the information.

You can use overpy (a python frontend for overpass API of OSM) to get OSM data for the desired city.

Now to save the desired POI data, you need to frame a query and export the data. 
You can use overpass-turbo to frame queries. Also Read about the various spatial vector types.

Save or Export the data as geojson file.

Query to extract a point or known as node, here below a shop.
```
node[amenity=shop]({{bbox}});
out;
```

### Reading the Data And Visualization

Use the Geopandas library, a python library based on pandas to work with geospatial data.

#### Folium Library

A python library built upon leaflet, which is a Java Script based web library.
It provides enough customization and options to play with interactive web map.

#### Visualization

Import a map of North Delhi by providing the geo-coordinates and arguments

![alt text](https://github.com/kumar-hardik/Geospatial-POI-Analysis/blob/master/Maps/Plain%20map.PNG)

Using the data, plot the coordinates of the POIs over the map area

![alt text](https://github.com/kumar-hardik/Geospatial-POI-Analysis/blob/master/Maps/points.PNG)

Now add the heat map plugin to see the density of the POIs

![alt text](https://github.com/kumar-hardik/Geospatial-POI-Analysis/blob/master/Maps/density.PNG)

Using the MarkerCluster plugin of Folium, cluster the points into groups

![alt text](https://github.com/kumar-hardik/Geospatial-POI-Analysis/blob/master/Maps/POI%20clustering.PNG)


### Clustering with Machine Learning

In Data Science and Machine Learning, KMeans and DBScan are two of the most popular clustering(unsupervised) algorithms.

Density clustering algorithms use the concept of reachability i.e. how many neighbors has a point within a radius. DBScan is more lovely because it doesn’t need parameter, k, which is the number of clusters we are trying to find, which KMeans needs. When you don’t know the number of clusters hidden in the dataset and there’s no way to visualize your dataset, it’s a good decision to use DBScan. DBSCAN produces a varying number of clusters, based on the input data.


## What's Left or Future Prospects

* Ploting the DBSCSN cluster into Folium Maps
* Apart from Node, including Way and Relation data type and perform similar analysis and clustering.


