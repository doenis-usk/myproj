{
  "queryType": "timeseries",
  "dataSource": "imagesearch-dsb",
  "granularity": "minute",
  "aggregations": [
    {
      "type" : "approxHistogramFold",
      "name" : "duration_hist",
      "fieldName" : "duration_hist"
    }
  ],
  "postAggregations": [
    {
      "type": "quantile",
      "name": "fifty_percentile",
      "fieldName": "duration_hist",
      "probability": "0.5"
    }
  ],
  "intervals": [ "2020-08-16T13:00:00.000/2020-08-16T13:01:00.000" ]
}
