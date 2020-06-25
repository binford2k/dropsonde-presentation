<!SLIDE >
# Schema hook
## Describes data that the plugin is allowed to return.

* Returns a BigQuery schema.
* JSON format with an array of row definitions

.break

    @@@ Ruby
    def self.schema
      [
        {
          "description": "The number of environments",
          "mode": "NULLABLE",
          "name": "environment_count",
          "type": "INTEGER"
        }
      ]
    end

.callout.info See full schema of all plugins with `dropsonde dev schema`
