<!SLIDE >
# Run hook
## Generates and returns data for the metric

* Returns an array of rows of data.
* Can return any data that the Puppet Server node can generate.
* Use PuppetDB, codebase, etc.
* Must match schema or plugin fails.

.break

    @@@ Ruby
    def self.run
      [
        :environment_count => Puppet.lookup(:environments).list.count,
      ]
    end
