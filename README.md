VisualiseAlgorithms
===================

This is a project that enables you to demonstrate, what an algorithm does, by visualising single processing steps.

### Introduction
Therefore, we've got a JSON-specification, that describes you how to define a corresponding 'DemoFile':

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
			"geometries": [
				{
					"type": "Polygon", 
					"properties": {}, 
					"coordinates": [...]
				}, 
				{
					"type": "LineString", 
					"coordinates": [...]
				}
			] 
		}, 
		{
			"type": "DemoFeature", 
			"properties": {}, 
			"stage": 1,
			"geometries": [
				{
					"type": "Polygon", 
					"properties": {}, 
					"coordinates": [...]
				}, 
				{
					"type": "LineString", 
					"coordinates": [...]
				}
			] 
		}
	]
}
```