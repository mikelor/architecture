# Data and Analytics Platform 

At a high level the reference architecture can be organized into the follow areas: Ingestion, Management, Storage, Integration, Compute and Analysis, and Consumption. 

## Generic Data Processing Patterns

### Lambda Architecture
A data system is designed to store data. It is also designed to derive information from stored data. The desired information may be the data itself, or it can be computed from stored data. 

Lambda Architecture proposes a simpler, elegant paradigm that is designed to tame complexity while being able to store and effectively process large amounts of data. 

From <http://lambda-architecture.net/>  

#### Overview
![image](./la-overview_small.png)

  1. All **data** entering the system is dispatched to both the batch layer and the speed layer for processing. 
  2. The **batch layer** has two functions: (i) managing the master dataset (an immutable, append-only set of raw data), and (ii) to pre-compute the batch views. 
  3. The **serving layer** indexes the batch views so that they can be queried in low-latency, ad-hoc way. 
  4. The **speed layer** compensates for the high latency of updates to the serving layer and deals with recent data only. 
  5. Any incoming **query** can be answered by merging results from batch views and real-time views. 

The Lambda Architecture emphasizes retaining the input data unchanged.

From <https://www.oreilly.com/ideas/questioning-the-lambda-architecture>  
