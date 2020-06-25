<!SLIDE >
# Aggregating data

Data is generated via SQL queries:

    @@@ Sql
    -- Generate an aggregate table of all classes used and their counts.
    SELECT classes.name, classes.count
    FROM `bto-dataops-datalake-prod.dujour.community_metrics`,
        UNNEST(classes) as classes
    GROUP BY classes.name, classes.count

![aggregation](/_images/aggregation.png)

~~~SECTION:notes~~~

* Each week, a bunch of little SQL queries run to generate that data.
* They take the real data and strip anything identifiable.
* Count, sum, etc. and generate metrics ready to be used.
* Every query generates a table.
* There are not a lot yet, but we'll be adding them as we learn useful ways to dissect the data.
* In case you've been admiring the wonderful imagery in this deck up until now, yes, this
  OmniGraffle thing is how sophisticated my own images are.

~~~ENDSECTION~~~

~~~SECTION:handouts~~~

https://github.com/puppetlabs/dropsonde-aggregation

~~~ENDSECTION~~~
