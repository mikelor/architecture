# Data Lake
A conceptual model that satisfies a basic core requirement for storing large quantities and varieties of data.

The term data lake was [coined by James Dixon](https://jamesdixon.wordpress.com/2010/10/14/pentaho-hadoop-and-data-lakes/), CTO of Pentaho. The standard way to handle reporting and analysis of this data was to identify the most interesting attributes, and to aggregate these into a data mart.

There are several problems with this approach:
  * Only a subset of the attributes are examined, so only pre-determined questions can be answered.
  * The data is aggregated so visibility into the lowest levels is lost

A Data Lake eliminates the restrictions of a typical data warehouse system by providing unlimited space, unrestricted file size, schema on read, and various ways to access data.

A data lake does not replace the need for a data warehouse. Instead they are complementary, we can continue to leverage our existing investments while collecting data we have been ignoring or discarding, and ultimately enable analysts to obtain insights faster.
