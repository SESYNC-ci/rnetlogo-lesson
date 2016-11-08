---
---
  
Load a model (file extension .nlogo) with `NLLoadModel()` by specifying the location of the file. 

NetLogo comes with a collection of sample models including "Fire.nlogo". 
  

~~~r
model.path <- file.path("models", "Sample Models", "Earth Science","Fire.nlogo")
NLLoadModel(file.path(nl.path, model.path))
~~~
{:.input}

Read about the Fire model and how it works [here](http://ccl.northwestern.edu/netlogo/models/Fire).