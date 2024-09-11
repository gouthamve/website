---
title: "The weirdest PromQL you’ll ever see: PromQL for Reporting, Analytics, and Business Intelligence"
---

## The weirdest PromQL you’ll ever see: PromQL for Reporting, Analytics, and Business Intelligence

Prometheus is fantastic at managing high-frequency data. But what if you have an analytics use case? Sometimes we just want to lower the frequency; to see daily, weekly or monthly data and find long-term trends or growth rates.

We might want to consider any of these use cases per day, week, or month, such as:

* Activity: requests or transactions
* Usage or consumption for billing or auditing
* Count of events: alerts or incidents, for example.

Why use Prometheus rather than more traditional analytics tools for this? By querying Prometheus directly we can avoid creating/maintaining a data-pipelines, avoid data exports and staleness problems, and lean on the power of the Prometheus ecosystem: For example, we can create overviews for management, plan ahead, and alert on our reports.

Yet querying Prometheus by calendar-month in particular can be surprisingly tricky. PromQL doesn’t support using 1M in subqueries because month-lengths vary.

In this talk I’ll:

* Take you on a journey, discovering ways that the time dimension can be aggregated when querying Prometheus by using:
  * The `offset` keyword
  * Joins and the `absent()` function
  * Union and intersection operators `or` and `and`
* Navigate a PromQL gotcha along the way, using a subquery
* Conclude by showing two different ways we can render monthly data FTW:
  * Render a saw-tooth cumulative counter which resets to zero every month-start
  * Use `day_of_month()` to then derive a single value per calendar month.

After this talk you will be able to query for daily, weekly or monthly data directly from Prometheus. As a result, you’ll be able to spot longer term trends or growth rates. And you’ll be able to compare with data from your other sources, for correlation or auditing purposes.


### Speakers
[Sam Jewell](../../speakers/sam-jewell)

<img src="https://sessionize.com/image/52fb-400o400o1-ECQMwRp99qX1scHwVVgjYE.jpg" style="width: 100px; border-radius: 50%" alt="Sam Jewell Profile Picture"/>

