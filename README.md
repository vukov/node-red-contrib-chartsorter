# node-red-contrib-chartsorter

This subflow takes the output of line chart and reorders the series elements according to a given configuration of topics. This allows to overcome the shortcomming, that the first data at the chart gets visualized in the first color of the chart. This prohibits a static assignment of line chart colors to input topics to the chart (as discussed here[^1] and [^2] ). 
The output of the subflow shall be fed back into the chart to force the sequence of the series as configured, no matter which topic came first (see the figure below). 

![demoflow](/doc/demoflow.png)

In case of a correct ordered series nothing needs to happen and fed back. As a result of this subflow, 
the configured topics of the subflow forces the chart data to be in that order and so the color setting in the chart implicitly sticks to the topic data. 

The second status outlet dumps a message about the Chartsroters behaviour. 

# Usage

Double-click on the subflow Chartsorter and enter the sequence of the desired series in the `topics` environment variable. The topics are separated by a comma, e.g., `last hour,last 3 hours,last 6 hours`. Careful with the commas there should be no space around them.

## Installation

Copy the content of the `flow.json` file into the clipboard and import it into your node-red setting.

## Related work 

[^1]: [Node-red-discourse - Chart line color](https://discourse.nodered.org/t/chart-line-color/13427)
[^2]: [Dashboard chart - change line colour dependent on value](https://flows.nodered.org/flow/a78ac10821112eb07fb8be8957a9f7cb)




