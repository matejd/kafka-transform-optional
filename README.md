# Optional
A Kafka Single Message Transform (SMT) that marks a field as optional (schema modification).

https://kafka.apache.org/documentation/#connect_transforms

## Config

SMT expects the following configuration values:
- `field.name` (field which schema will be changed)

Schema of the configured field will be changed e.g. from `INT64` to `OPTIONAL_INT64`.

Example configuration:

```
"transforms": "optional",
"transforms.optional.type": "com.github.matejd.kafka.connect.transform.Optional$Value",
"transforms.optional.field.name": "timestamp_seconds"
```
