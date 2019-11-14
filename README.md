# GTFS-RT and Logstash Example

[GTFS-RT](https://developers.google.com/transit/gtfs-realtime) is a specification for realtime transit data which includes alerts, vehicle positions, and trip updates.

This example uses Logstash to request realtime updates from public transit in King County, WA, USA.

## Usage

1. Install the logstash-codec-protobuf plugin
```
logstash-plugin install logstash-codec-protobuf
```

2. Requests for realtime updates requires an API key. Please see the [Open Transit Data documentation](https://www.soundtransit.org/help-contacts/business-information/open-transit-data-otd) for information on requesting an API key.

3. You need to set some environment variables when running Logstash. Here's how I do it in the command line.

```
PATHDIR=$(pwd) USER=elastic PASSWORD=my-elasticsearch-password APIKEY=my-api-key logstash --path.settings=$(pwd)
```
