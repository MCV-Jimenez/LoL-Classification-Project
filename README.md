# Stellar Classification
![Project Image](https://astrobiology.nasa.gov/uploads/filer_public_thumbnails/filer_public/cf/29/cf294394-800d-4fc4-954d-78dba367de36/large_web.jpg__1240x510_q85_subject_location-620%2C254_subsampling-2.jpg)

---

### Table of Contents

- [Description](#description)
- [Methods Used](#methods-used)
- [References](#references)
- [Author Info](#author-info)

---

## Description
In astronomy, stellar classification is the classification of stars based on their spectral characteristics. The classification scheme of galaxies, quasars, and stars is one of the most fundamental in astronomy. The early cataloguing of stars and their distribution in the sky has led to the understanding that they make up our own galaxy and, following the distinction that Andromeda was a separate galaxy to our own, numerous galaxies began to be surveyed as more powerful telescopes were built. This datasat aims to classificate stars, galaxies, and quasars based on their spectral characteristics.


#### Methods Used
> All code written using Python Libraries
- Pandas for data manipulation: Thankfully this dataset came clean and polished for analysis and machine learning. There are no missing values, inconsistent categories, or incorrect datatypes. 
```
|index|obj\_ID|alpha|delta|u|g|r|i|z|run\_ID|rerun\_ID|cam\_col|field\_ID|spec\_obj_ID|class|redshift|plate|MJD|fiber\_ID|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|1\.2376609613277432e+18|135\.6891066036|32\.4946318397087|23\.87882|22\.2753|20\.39501|19\.16573|18\.79371|3606|301|2|79|6\.543777369295182e+18|GALAXY|0\.6347936|5812|56354|171|
|1|1\.237664879951151e+18|144\.826100550256|31\.2741848944939|24\.77759|22\.83188|22\.58444|21\.16812|21\.61427|4518|301|5|119|1\.1760142036707334e+19|GALAXY|0\.779136|10445|58158|427|
|2|1\.2376609613304302e+18|142\.188789562506|35\.5824441819976|25\.26307|22\.66389|20\.60976|19\.34857|18\.94827|3606|301|2|120|5\.152200256025549e+18|GALAXY|0\.6441945|4576|55592|299|
|3|1\.237663478724298e+18|338\.741037753146|-0\.402827574587482|22\.13682|23\.77656|21\.61162|20\.50454|19\.2501|4192|301|3|214|1\.030107141295442e+19|GALAXY|0\.9323456|9149|58039|775|
|4|1\.237680272041378e+18|345\.282593210935|21\.1838656010284|19\.43718|17\.58028|16\.49747|15\.97711|15\.54461|8102|301|3|137|6\.891864880783317e+18|GALAXY|0\.1161227|6121|56187|842|
```

- Exploratory visualizations: Since every feature in this dataset except the class feature consists of numeric data, I relied heavily on seaborn violin plot visualizations to analyze the data more in depth.
![Alpha   Delta Violin plots](https://user-images.githubusercontent.com/97704503/165169798-d66f0302-c1b0-4e5d-9054-dda79833d545.png)


---

## Reference
>Data: [Stellar Classification](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17)
---

## Author Info

- Email - jimenezmarco3254@gmail.com
- LinkedIn - [Marco Jimenez](https://www.linkedin.com/in/marco-jimenez-50637922b/)

[Back To The Top](#Food-Sales-Predictions)
