## Build OpenTelemetry Collector on z/OS
You can build the collector on z/OS from the source by following the steps below:

### Requirements
To build the collector, you need GNU make and go v1.21.11. You can find and install them using the links below:
1. [GNU Make](https://github.com/ZOSOpenTools/makeport)
2. [Go v1.21.11](https://www.ibm.com/docs/en/sdk-go-zos/1.22?topic=go-installing-configuring-pax-edition)

### Compiling the collector
Compile the opentelemetry collector repository using the following commands:
```
git clone https://github.com/open-telemetry/opentelemetry-collector.git
cd opentelemetry-collector
gmake install-tools
gmake otelcorecol
```

This will generate the collector executable in the `bin` directory.

### Configuring the collector
Currently, the collector does not run without turning off metric collection. To disable metric collection, set the metrics level to `none` in the config file. An example config file is shown below:
```
receivers:
  otlp:
    protocols:
      grpc:
      http:

exporters:
  debug:
    verbosity: detailed

service:
  pipelines:
    traces:
      receivers: [otlp]
      exporters: [debug]
  telemetry:
    metrics:
      level: none
```

### Running the collector
Run the collector using the executable and the config file:

` ./bin/<name of the executable> --config=<path to config file>`

Replace '<path to config file>' with the path to your config file.
