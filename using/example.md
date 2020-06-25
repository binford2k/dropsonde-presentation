<!SLIDE >
# Interesting queries

* Dataset includes:
    * Forge module metadata
    * Static analysis of Forge modules
    * GitHub repositories that look like Puppet modules
    * Aggregated telemetry data
* Combine them as you will.

Example: a list of the modules on the Forge that define custom native types:

    @@@ Sql
    SELECT DISTINCT g.repo_name, f.slug
    FROM `dataops-puppet-public-data.community.github_ruby_files` g
    JOIN `dataops-puppet-public-data.community.forge_modules` f
        ON g.repo_name = REGEXP_EXTRACT(f.source, r'^(?:https?:\/\/github.com\/)?(.*?)(?:.git)?$')
    WHERE STARTS_WITH(g.path, 'lib/puppet/type')
    LIMIT 1000
