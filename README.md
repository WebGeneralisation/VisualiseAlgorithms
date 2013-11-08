VisualiseAlgorithms
===================

This is a project that enables you to demonstrate, what an algorithm does, by visualising single processing steps.

### Introduction
Therefore, we've got a JSON-specification, that describes you how to define a corresponding 'DemoFile'.

* Basic Object: **"DemoCollection"**, which contains:
	- type
	- properties
	- features
* Features are an array of: **"DemoFeatures"**, where each contains:
	- type
	- properties
	- stage
	- geometries
* The Syntax of the geometries of a "DemoFeature"-object is adapted to the [GeoJSON-specification](http://geojson.org/geojson-spec.html), consisting of:
	- "FeatureCollection", which contains an array of...
	- "Features", where each contains:
		* properties
		* geometry, consisting of:
			- (geometry-) type
			- coordinates


```JSON
{
	"type": "DemoCollection", 
	"properties": {
		"title":"Enter a title",
		"description":"Enter a short description"
	}, 
	"features": [
		{
			"type": "DemoFeature", 
			"properties": {}, 
			"stage": 0,
			"geometries": 
			{
				"type":"FeatureCollection",
				"features":
				[
					{
						"type":"Feature",
						"properties":{},
						"geometry":
						{
							"type": "Polygon", 
							"coordinates": [...]
						}
					},
					{
						"type":"Feature",
						"properties":{},
						"geometry":
						{
							"type": "LineString", 
							"coordinates": [...]
						}
					}
				]
			} 
		}, 
		{
			"type": "DemoFeature", 
			"properties": {}, 
			"stage": 1,
			"geometries": 
			{
				"type":"FeatureCollection",
				"features":
				[
					{
						"type":"Feature",
						"properties":{},
						"geometry":
						{
							"type": "Polygon", 
							"coordinates": [...]
						}
					},
					{
						"type":"Feature",
						"properties":{},
						"geometry":
						{
							"type": "LineString", 
							"coordinates": [...]
						}
					}
				]
			} 
		}
	]
}
```