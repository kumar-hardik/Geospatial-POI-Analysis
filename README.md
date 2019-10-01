# Geospatial Point of Interest Analysis

There's a lot of open data available about the demographics and geography of the planet. But this information is not necessarily supervised in any particular structure from which insights can be drawn.

This project create clusters of distinct commercial centers or markets using points of interest data of a city (the city could be yours). Points of interest (POI) data provides location information of different places along with their defining tags like school, type of outlets, type of building, etc.


## Getting Started

The jupyter notebook is easily rendered over Github so you don't have to do anything specific. But the Folium Maps which are used here will not be rendered here on github, so download all the htlm files from Map folder and open on Chrome Browser or run the notebook locally.

### Getting the Data

Getting an open source map which have all the attributes. 
Open Source Map (https://www.openstreetmap.org/#map=11/28.6518/77.2219) is the open source to get all the information.

You can use overpy (a python frontend for overpass API of OSM) to get OSM data for the desired city.

Now to save the desired POI data, you need to frame a query and export the data. 
You can use overpass-turbo to frame queries. Also Read about the various spatial vector types.

Save or Export the data as geojson file.

Query to extract a point or known as node
```
node[amenity=shop]({{bbox}});
out;
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

