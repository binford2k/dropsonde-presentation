<!SLIDE >
# What I'm asking from you

* This is totally opt-in only right now.
* `puppet module install puppetlabs/dropsonde`
* Check out the example dataset and contribute some aggregation queries.
* Develop and contribute a metric plugin.
* Doesn't have to be strictly Puppet, just ecosystem:
    * Reid already made a plugin to see the impact of building a better control repo and `Puppetfile` for better r10k deploys.
    * David could see how many people are using the Rocket.chat integration for `voxpupuli/puppet-webhook`.
* `puppet module install puppetlabs/dropsonde`
* Build some tooling that uses the public data.

.callout.info Seriously, install the module and classify your master. It would help a ton.

~~~SECTION:notes~~~

.callout.book `Dropsonde`: an expendable weather reconnaissance device created by the
National Center for Atmospheric Research, designed to be dropped from an aircraft
at altitude over water to measure storm conditions as the device falls to the surface.

~~~ENDSECTION~~~

~~~SECTION:handouts~~~

.callout.book `Dropsonde`: an expendable weather reconnaissance device created by the
National Center for Atmospheric Research, designed to be dropped from an aircraft
at altitude over water to measure storm conditions as the device falls to the surface.

.callout.info Installing Dropsonde is super straightforward. Install the `puppetlabs-dropsonde`
Puppet module and classify your Puppet master with the `dropsonde` class. If you
have multiple compile nodes, just classify the primary Puppet server. This will
install the tool and configure a weekly cron job to submit the reports.

~~~ENDSECTION~~~
