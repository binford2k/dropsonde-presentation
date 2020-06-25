<!SLIDE >
# Example hook
## Representative example of sample data

* Provide one element of randomized representative data.
* Used to generate a dataset that's shaped like the real dataset.
* Must match the `schema` or plugin fails.
* Used for developers to generate aggregation queries.

.break

    @@@ Ruby
    def self.example
      [
        :environment_count => rand(1..100),
      ]
    end

~~~SECTION:notes~~~

* Available as `dataops-puppet-public-data:community.community_metrics`

~~~ENDSECTION~~~

~~~SECTION:handouts~~~

* Available as `dataops-puppet-public-data:community.community_metrics`

~~~ENDSECTION~~~
