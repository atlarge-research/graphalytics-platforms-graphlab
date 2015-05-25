# Graphalytics GraphLab Create platform extension


## Getting started

Please refer to the documentation of the Graphalytics core (`graphalytics` repository) for an introduction to using Graphalytics.


## GraphLab-specific benchmark configuration

The `graphlab` benchmark can run either locally or on Hadoop version 2.4.1 or later (earlier versions have not been attempted) with YARN as resource manager. Before launching the benchmark, ensure GraphLab Create is installed on your system with a valid (free) license key, the python executable is in your PATH and Hadoop is running in either pseudo-distributed or distributed mode (if used). Next, edit the `graphlab`-specific configuration file: `config/graphlab.properties` and change the following settings:

- `graphlab.target`: Set to `local` to run the benchmark on the machine on which Graphalytics is running, or `hadoop` to deploy GraphLab to a Hadoop cluster.
- `graphlab.job.virtual-cores`: Set to the amount of virtual cores to request from your Hadoop deployment.
- `graphlab.job.heap-size`: Set to the amount of heap space (in MB) is required for job execution in the Hadoop environment.

If Hadoop is used for the benchmark, you must also change the following setting: 

 - `hadoop.home`: Set to the root of your Hadoop installation (`$HADOOP_HOME`).

