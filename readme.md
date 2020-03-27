Transforms the data from [CSSEGISandData/COVID-19](https://github.com/CSSEGISandData/COVID-19) into a json file. Available at [https://pomber.github.io/covid19/timeseries.json](https://pomber.github.io/covid19/timeseries.json). Updated three times a day using GitHub Actions.

The json contains the number of Coronavirus confirmed cases, deaths, and recovered cases for every country and every day since 2020-1-22:

```
{
  "Thailand": [
    {
      "date": "2020-1-22",
      "confirmed": 2,
      "deaths": 0,
      "recovered": 0
    },
    {
      "date": "2020-1-23",
      "confirmed": 3,
      "deaths": 0,
      "recovered": 0
    },
    ...
  ],
  ...
}
```

For example, if you want to use it from a web site: 
```js
fetch("https://pomber.github.io/covid19/timeseries.json")
  .then(response => response.json())
  .then(data => {
    data["Argentina"].forEach(({ date, confirmed, recovered, deaths }) =>
      console.log(`${date} active cases: ${confirmed - recovered - deaths}`)
    )
  })
```

### Projects using this dataset
- [Mobile Friendly COVID-19 Report](http://corona-status.live/) ([repo](https://github.com/ameerthehacker/corona-status)): Coronavirus daily report in a mobile friendly website (PWA)
- [COVID-19 Daily Report](https://icebob.info/covid19/) ([repo](https://github.com/icebob/covid19)): Coronavirus daily report, updated hourly
- [COVID-19 GLOBAL Report](https://mdusmanansari.github.io/COVID-19-Global-Report/) ([repo](https://github.com/mdusmanansari/COVID-19-Global-Report/))
- [covid-charts](https://jeetiss.github.io/covid-charts/) ([repo](https://github.com/jeetiss/covid-charts)): chart widget with Coronavirus stats for specified country
- [COVID-19 GraphQL API](https://covid19-graphql.now.sh/) ([repo](https://github.com/rlindskog/covid19-graphql))
- [COVID-19 Global Chart](https://gabrielcesar.github.io/covid/) ([repo](https://github.com/gabrielcesar/covid)): Chart GeoMap with last status by country.
- [COVID-19 Stats](https://corona.netflex.dev/) ([repo](https://github.com/thomas-alrek/covid-19-stats)): A simple mobile friendly dashboard visualizing the latest stats of the COVID-19 outbreak.
- [Corona.log](https://corona-log.now.sh/) ([repo](https://github.com/biewxw/corona.log)): A simple COVID-19 data checker per region
- [COVID-19 Trends and Growth Rate](https://github.com/dariocazzani/COVID-19-trends): A Python implementation of growth rate and other trend analysis
- [Are we dead yet](https://paroj.github.io/arewedeadyet/) ([repo](https://github.com/paroj/arewedeadyet)): Live graphs of confirmed, infected and infection rate. Outbreak normalised for comparison.
- [COVID-19 How Bad Is It](https://faizalazman.github.io/) ([repo](https://github.com/faizalazman/faizalazman.github.io)): Live graphs with latest news involving Covid-19,
- [epidemic-simulator](https://github.com/RemiTheWarrior/epidemic-simulator): Mathematical model using Macroscopic Rate Equations for simulating the future of the epidemic
- [COVID-19 Sri Lanka Tracker](https://covid-19-sl.netlify.com/) ([repo](https://github.com/dhanushkac/covid-19-sl-tracker)): Live Updates of COVID-19 Patients in Sri Lanka
- [COVID-19 Countries Trends & Comparison](https://energ.ee/corona-virus) ([repo](https://github.com/energee/corona-virus)): Country comparison of COVID-19 cases, with per-capita and growth views.

[+ Add yours](https://github.com/pomber/covid19/edit/master/readme.md)
