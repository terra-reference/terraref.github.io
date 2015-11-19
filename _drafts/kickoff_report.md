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

## Sharing data and vocabularies

At the meeting participants were unsure of how data can be shared.

## Free Will + Opinionated Plea

Each of the six funded projects has defined their required degree of data sharing in close collaboration with the ARPA-E TERRA project team. I get to design and deploy an unprecedented open-access dataset - please tell me how you want to use it.

Does everyone have to share data? Ultimately this is up to ARPA-E to decide. I hope that teams will share their data. I encourage at most within two years of collection. There will be enough data to support plenty of research, and most teams seem to have vastly overlapping data as well as a few 'tricks' up their sleve. For one, Steve Kresovitch and the robotics team  at CMU (check out their berry measurment and mapping system! ..link..). Keep the 'secret' sauce and please share the 95% of the rest of your data. Or at least the basics like height, biomass, and leaf area index!

We can reduce the impediments to large scale synthetic research through shared conventions. The most important feature to adopt is shared vocabularies. Converting across data models can be challenging, we can't eliminate this task but 

Teams have the option of requesting a local instance of the TERRA Refence Computing infrastrucutre. We will release a TERRA network of the BETYdb database starting with a database for simulated test data, one for reference data, one for the Illinois team and one for the Texas A&M team. 

Even more important than the network of databses is a suite of easy methods for finding and using data. BETYdb, for example, exports data as `.csv`, `.json`, and `.xml` as well as through the rOpenSci traits package and url queries such as [`betydb.org/search?=miscanthus+yield`](https://betydb.org/search?=miscanthus+yield).

[1]  https://github.com/terraref/computing-pipeline/issues/new
[2] https://gitter.im/terraref/computing-pipeline
