Set compaction threshold for `pulsar/system/__mqtt_event` topic.

```bash
./bin/pulsar-admin topicPolicies set-compaction-threshold pulsar/system/__mqtt_event -t 200m
./bin/pulsar-admin topicPolicies get-compaction-threshold pulsar/system/__mqtt_event
```

Trim or truncate pulsar/system/__mqtt_event to release storage.

```bash
./bin/pulsar-admin topics trim-topic pulsar/system/__mqtt_event
./bin/pulsar-admin topics truncate pulsar/system/__mqtt_event
```

Delete `healthcheck` topics to release storage.

```bash
./bin/pulsar-admin topics delete persistent://pulsar/test-pulsar-cluster-1/pulsar-broker1:8080/healthcheck
./bin/pulsar-admin topics delete persistent://pulsar/test-pulsar-cluster-1/pulsar-broker2:8080/healthcheck
```
