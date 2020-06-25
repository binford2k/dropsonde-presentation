<!SLIDE >
# Rangefinder

    @@@ console
    [~/Projects/puppetlabs-concat]$ rangefinder manifests/fragment.pp
    [concat::fragment] is a _type_
    ==================================
    The enclosing module is declared in 173 of 575 indexed public Puppetfiles

    Breaking changes to this file WILL impact these modules:
      * nightfly-ssh_keys (https://github.com/nightfly19/puppet-ssh_keys.git)
      * viirya-mit_krb5 (git://github.com/viirya/puppet-mit_krb5.git)
      * rjpearce-opendkim (https://github.com/rjpearce/puppet-opendkim)
      * shadow-tor (git://github.com/LeShadow/puppet-tor.git)
    [...]

    Breaking changes to this file MAY impact these modules:
      * empi89-quagga (UNKNOWN)
      * unyonsys-keepalived (UNKNOWN)
      * Flameeyes-udevnet (UNKNOWN)
      * ricbra-ratbox (git://github.com/ricbra/puppet-ratbox.git)
    [...]

.callout.lightbulb Identify the public Forge modules using parts of your code.

~~~SECTION:notes~~~

* Rangefinder is a tool I've been working on for a while.
* You just run it on a file and it figures out what that file defines and then tells you what Forge modules use it.
* In other words, if you break that file, who will be impacted?
* If you run it against a whole module, it iterates everything in the module.

~~~ENDSECTION~~~

~~~SECTION:handouts~~~

https://github.com/puppetlabs/puppet-community-rangefinder

~~~ENDSECTION~~~
