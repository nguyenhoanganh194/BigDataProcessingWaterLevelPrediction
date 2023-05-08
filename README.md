# IrelandMarineDataAnalysis
Ireland Marine Data with Spark - Project for 521283S Big Data Processing and Applications, Spring 2023, @unioulu

## dataset
Irish Marine Institute
- [Digital Ocean](https://www.digitalocean.ie/)
- [Dataset Source](https://erddap.marine.ie/erddap/tabledap/allDatasets.csv?&distinct()&orderBy("institution,datasetID,title"))

### Used Subsets
| Dataset ID | Description | Data Link | 
|---|---|---|
| IrishNationalTideGaugeNetwork | Real Time Tide Data | [url](https://erddap.marine.ie/erddap/tabledap/IrishNationalTideGaugeNetwork.subset) |
| IMI-TidePrediction | Predicted Tide Data | [url](https://erddap.marine.ie/erddap/tabledap/IMI-TidePrediction.subset) |
| IWaveBNetwork30Min | Real Time Wave Data (Every 30mn) | [url](https://erddap.marine.ie//erddap/tabledap/IWaveBNetwork30Min.subset) |
| IWaveBNetwork_spectral | Spectral Wave Data (Statistics) | [url](https://erddap.marine.ie//erddap/tabledap/IWaveBNetwork_spectral.subset) |

## How-To Run
### Local Env
To run locally in a python environment:

- Create and activate environment
```bash
conda create -n spark
conda activate spark
```
OR
```bash
python -m venv venv
source ./venv/bin/activate # linux
.\venv\Scripts\activate # windows
```

- Install requirements and run
```bash
pip install -r requirements.xt
jupyter lab
```

### Docker
To run locally in a single node docker instance:

```bash
docker run -it --rm -p 8888:8888 -v "<repo-location>:/home/jovyan/work" jupyter/pyspark-notebook:spark-3.4.0
```
