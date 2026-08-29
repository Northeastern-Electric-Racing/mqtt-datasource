# MQTT data source for Grafana

Stream real-time MQTT messages into Grafana dashboards.

> **Note:** This plugin streams live data only and doesn't store historical messages.

## Documentation

For the plugin documentation, visit the [plugin documentation website](https://grafana.com/docs/plugins/grafana-mqtt-datasource/latest/).

## Contributing

Instructions for plugin setup, testing, and contributing can be found in [CONTRIBUTING.md](CONTRIBUTING.md).

## NER

Added support for the Odyssey protobuf.  Used:
```
protoc -I=. --go_out=. --go_opt=paths=source_relative ./pkg/protoc/serverdata.proto
```
Built and uploaded the zip:
```
npm installl
npm run build
mage
mv dist/ grafana-mqtt-datasource
zip grafana-mqtt-datasource-1.2.0.zip grafana-mqtt-datasource -r
```
Upload the zip to releases.
