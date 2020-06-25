<!SLIDE >
# Plugin hook design

* Plugins are implemented as hooks.
    * `description`
    * `schema`
    * `example`
    * `run`
* Some hooks are optional
    * `initialize`
    * `setup`
    * `cleanup`

~~~SECTION:notes~~~

* description describes what the plugin does
* schema describes the data that the plugin returns
* example provides a representative example of what the metric data could look like.
* run actually evaluates the metric and returns real data
* the optional hooks, initialize/setup/cleanup, just provide ways to separate out the code into cleaner stages

~~~ENDSECTION~~~
