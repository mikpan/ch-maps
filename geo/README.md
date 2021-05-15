# Filter Bern municipalities
Based on the knowledge that canton Bern has KANTONSNUM = 2, use the the following jq script:
```
cat municipalities.geojson| jq '.features = ([.features[] | select(.properties.KANTONSNUM == 2)])' -c > be.municipalities.geojson
```