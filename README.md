# Airflow Image that works on Openshift Clusters

This is a project that has been sourced from [puckel/docker-airflow](https://github.com/puckel/docker-airflow) and changed to work on Openshift Clusters.

#### Changes made from the source repository
* The original docker image when run on Openshift requires root permissions to work because of the way Openshift assigns uid. This repository takes a change from another docker image for Airflow which fixes the issue [https://github.com/adyachok/docker-airflow](https://github.com/adyachok/docker-airflow).
  This repository is not used directly because it is not maintained and puckel/docker-airflow uses the latest version of Airflow.
  The exact piece of code can be found [here](https://github.com/adyachok/docker-airflow/blob/master/script/entrypoint.sh#L70).

* Added prometheus monitoring for Airflow tasks
  This is an additional package introduced [here](https://github.com/epoch8/airflow-exporter).
