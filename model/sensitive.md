<!SLIDE >
# Private dataset
## So about that sensitive data...

![No trespassing](/_images/no_tresspassing.png)

* Telemetry reports are not terribly sensitive, but they are fingerprintable.
* So we store them only in a secured dataset.
* Limited access, only myself and our BigQuery admin team.

.callout.info Our own developers who want to use collected metrics data
have to do it via aggregation queries just like you would.

