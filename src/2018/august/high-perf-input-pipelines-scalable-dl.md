# High Performance Input Pipelines for Scalable Deep Learning  
**Speaker: Joshua Robinson, Pure Storage**

## Background on Pure Storage

* mass IOT created possibility for full flash / NAND storage, deprecating spinning disk
* transition from disk storage created new problems to solve
* "data centric architecture simplifies everything"

## "ML Use Case": Load performance estimation

* customers want to know what will happen if they increase load on system
* no single metric that explains the "load" of a system
* data is collected on customer's devices, aggregated by purestorage
* approx. 1 trillion data points per day 
* feature examples:
  * controller 
  * write/read bw
  * read/write IO size
  * flash array "fullness"
  * avg. compression rate

## "Scaling" AI

* customer's want to deploy ML models
* "storage is the most important part of your ML system" - Joshua
  * actually data is, but all your data lives in storage!
* 10x data -> halving error rate

### AI Hype

* "AI" has gone through several hype cycles
* falls from popularity when data / compute fail to keep up
* rises in popularity when new hardware / new data enables specific types of models 

### intuition behind deep learning

* classification
  * raw data -> network -> label
  * gpus enabled fast convolution, fast linear algebra for dnns
* regression
  * raw data -> network -> number
* training = backprop = linear algebra

### scaling

* what happens when you go from 1 gpu to n gpus?
* spread batches across gpus, merge gradients, update weights
* how to get batch data to gpus?
  * data bottleneck with massive online training + traditional data storage 
    techniques

### going from image data to tensor data

1. enumerate and shuffle data
1. augment data online
1. copy to gpu

With fast and enough gpus, data ingestion can be a bottleneck.  Any one of these
steps may be!

### benchmarks

Hardware Stack:
* Pure Storage flash (180 TB usable storage)
* Some Rack Server
* 4 Nvidia DGX-1s

Software:  
* tensorflow
* horovod to train across multiple gpus
* dgx-os on nvidia workstatiosn

 
Testing on a single GPU:  
* 216 images / sec with Inception v3.
* 228 images / sec upper bound performance
  * generated random data on the fly
* 225 images / sec with prefetch queue
  * added a queue with pre-fetched / pre-populated data, 

Testing on 32 GPUS (4 DGX-1s):  
* 4143 images / sec, naive Inception v3.
* 7200 iages / sec, linear speedup.
* 6580 images / sec, synthetic data
* 5335 images / sec, + prefetch queue
* 6440 images / sec, + prefetch queue - data augmentation
  * note that data augmentation was performed in the CPU

Insights / Takeaways:  
* TF scheduler is complex and struggles to handle these complex operations
* bottleneck in CPU data augmentation
* took very specific optimizations to images to reach "theoretical upper limit"
* need to 


## P.S. PhD after Rice

* Cybersecurity Startup, R&D prototyping
  * felt a lack of impact
  * company had no intention of implementing prototypes
* Google, Search Infra Team
  * "production ML"
  * steered search alg., deciding whether to index pages 
  * 1000+ engineers on search team
  * many many engineers working on "PhD Hard" problems
  * PhD is great preparation for work in industry
* Pure Storage, SWE
  * left google to work at startup, wanted to see an idea go from whiteboard to
    product
  * product seemed difficult and challenging
* Pure Storage, ?
  * 

#### Overall thoughts

* if you're interested in industry, go to silicon valley
* the types of jobs needing genuine research skills are much more widespread
  than expected
* bay area is very far ahead of the rest of the world 


### Questions

* Why did you go to Pure Storage?
  * If we can build it, people will buy it
  * I don't think we can build it, but I'm down to try
  * deep tech, not marketing
