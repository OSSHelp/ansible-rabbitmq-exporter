# rabbitmq-exporter

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/rabbitmq-exporter/status.svg)](https://drone.osshelp.ru/ansible/rabbitmq-exporter)

Simple role which installs RabbitMQ Exporter.

## Usage (example)

```yaml
  - role: rabbitmq
    rabbitmq_plugins: "rabbitmq_management"
  - role: rabbitmq-exporter
```

## Available parameters

No parameters needed usually.

### Main

| Param | Description |
| -------- | -------- |
| `rabbitmq_exporter_version`| RabbitMQ Exporter version. Defaut: `0.29.0` |
| `rabbitmq_exporter_rabbit_url`| Default: `http://localhost:15672` |
| `rabbitmq_exporter_rabbit_user`| Default: `guest` |
| `rabbitmq_exporter_rabbit_password`| Default: `guest` |
| `rabbitmq_exporter_publish_port`| Default: `9090` |
| `rabbitmq_exporter_output_format`| Default: `JSON` |
| `rabbitmq_exporter_log_level`| Default: `info` |
| `rabbitmq_exporter_rabbit_exporters` | Default: `exchange,node,overview,queue,connections` |

### Misc

Additional parameters which can be overridden, but usually it is not needed.

| Param | Description |
| -------- | -------- |
| `rabbitmq_exporter_binary_url`| Default: `https://oss.help/builds/pub/rabbitmq_exporter/{{ rabbitmq_exporter_version }}/rabbitmq_exporter` |
| `rabbitmq_exporter_sum` | Default: `sha256:https://oss.help/builds/pub/rabbitmq_exporter/{{ rabbitmq_exporter_version }}/SHA256SUMS` |
| `rabbitmq_exporter_service_name` | Default: `rabbitmq_exporter`

## Useful links

- [Source](https://github.com/kbudde/rabbitmq_exporter)
- [Our article](https://oss.help/kb1960)

## TODO

- ...

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
