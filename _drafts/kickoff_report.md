# Summary

## Cat 5 teams

### Pipeline Demo

The idea was to show how we can wrap an existing analytical pipeline within a workflow engine and API to provide a variety of interfaces that users can access, including:

* uploading sensor data to a web interface
* uploading sensor data files programatically in a way that can be automated
* selecting data and opening a terminal, IDE, or notebook to develop new extraction algorithms.

We are currently working on documenting what we have developed so far with an aim at helping end users use the system. I will put your questions on GitHub to make sure that they are addressed in the documentation. 

* links to existing code, documentation

1) ' how can I test this system out? Is the pipeline already set up with some of the PlantCV tools?'

What I showed was a minimal demonstration, and the team and I are currently writing out what we showed. I showed four ways of executing the PlantCV pipeline: 

1. uploading a file triggers the pipeline. Here is an example of the finished product: http://141.142.208.144/clowder/files/5643baa8e4b086fa6db916ca
2. launching a Jupyter notebook, then the analysis can be done at the bash shell. 

### Sharing data and vocabularies

At the meeting participants were unsure of how data can be shared.

Teams have the option of requesting a local instance of the TERRA Refence Computing infrastrucutre. We will release a TERRA network of the BETYdb database starting with a database for simulated test data, one for reference data, one for the Illinois team and one for the Texas A&M team. 

Even more important than the network of databses is a suite of easy methods for finding and using data. BETYdb, for example, exports data as `.csv`, `.json`, and `.xml` as well as through the rOpenSci traits package and url queries such as betydb.org/search?=miscanthus+yield.

It is designed to pull updates to the reference data sets and _optionally_ push any shared data back.
It 

[1]  https://github.com/terraref/computing-pipeline/issues/new
[2] https://gitter.im/terraref/computing-pipeline
