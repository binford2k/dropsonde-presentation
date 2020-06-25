<!SLIDE >
# Public dataset
## No access to *individual records* themselves

    @@@ Sql
    -- The top ten most used classes in the ecosystem
    SELECT name, count
    FROM `dataops-puppet-public-data.aggregated.class_usage_count`
    ORDER BY count DESC
    LIMIT 10

.break

    @@@ Json
    [
      { "name": "Resource_api::Agent", "count": "272" },
      { "name": "Account",             "count": "272" },
      { "name": "Ssl::Params",         "count": "272" },
      { "name": "Classification",      "count": "272" },
      { "name": "Os_patching",         "count": "269" },
      { "name": "Ntp",                 "count": "265" },
      { "name": "Ntp::Install",        "count": "265" },
      { "name": "Ntp::Config",         "count": "265" },
      { "name": "Ntp::Service",        "count": "265" },
      { "name": "Zsh::Params",         "count": "265" }
    ]

~~~SECTION:notes~~~

* Let's start from the end here
* This is the data that you (or anyone else) has access to.
* All you need is a Google Cloud account.
* This query shows the ten most used classes currently in the dataset.
* Note that you cannot see any actual records themselves, so you cannot see
  the complete set of classes that any site is using.
* All you see is a lot of pre-computed sums, counts, and other data aggregations.
* The actual data is currently super limited right now -- only alpha/beta testers have reported in.

~~~ENDSECTION~~~

~~~SECTION:handouts~~~

You'll need a [Google Cloud](https://cloud.google.com) account and then you can access the
[dataset](https://console.cloud.google.com/bigquery?p=dataops-puppet-public-data&d=aggregated)
with your browser via the BigQuery Console. Then you can run any queries you'd like.

~~~ENDSECTION~~~
