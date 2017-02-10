# hpc-explo
Exploration of HPC technologies

## scispark_zeppelin
[Scispark](https://github.com/SciSpark/SciSpark) is a project extending Apache Spark.
`scispark_zeppelin` contains zeppelin notebooks to explore climate data manipulation.

To install Scispark follow the installation instructions from the [wiki page](https://github.com/SciSpark/SciSpark/wiki/2.-Installation) up to the zeppelin installation.

Note: some examples below may need more memory ressources than the default one. To make sure you do not have memory limitations issues, it is suggested you add the following lines to your `zeppelin-env.sh` :

```
export SPARK_SUBMIT_OPTIONS=--driver-memory 8G --executor-memory 8G
```

You can view zeppelin notebooks with the [zeppelin viewer](https://www.zeppelinhub.com/viewer)

### Notebooks

#### 2C7RBBP9H
Calculate and plot Canadian year precipitation average for 1950 and 1951

**Data**

The notebook needs the following files

* `nrcan_canada_daily_pr_1950.nc`
* `nrcan_canada_daily_pr_1951.nc`

http://outarde.crim.ca:8083/thredds/dodsC/birdhouse/data/nrcan/nrcan_canada_daily/

You will need a list of path to netCDF files in the format
```
/path/to/nrcan_canada_daily_pr_1950.nc
/path/to/nrcan_canada_daily_pr_1951.nc
```
Once the file is created, change the definition of the variable `dataListPath` in the notebook with its path.
