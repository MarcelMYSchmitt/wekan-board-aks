We've got two ways of deploying our mongodb.

First one is a simple mongodb container for a 'breakthrough'. It's just a simple container without no high availaibility.
If the container crashes all the data gets lost. 

Second one is as a stateful mongodb with azure storage inside of the kubernetes cluster.
There you can define how many instances of your mongodb you want to host. 