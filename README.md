# node-red-contrib-chartsorter

This subflow takes the output of chart and reorders the series elements according to a given configuration. This allows for a static assignment of line chart color to input topics to the chart. 
The output of the subflow shall be fed back into the chart to force the sequence of the series as configured, no matter which topic came first. 
In case of a correct ordered sequence nothing needs to happen and fed back.
![demoflow](/doc/demoflow.png)

As a result of this subflow, the configured topics of the subflow, force the chart data to be in that order and so the color setting in the chart implicitly sticks to the topic sequences. 

# Usage

Double-click on the subflow and enter the sequence of the topics in the `topics environment` variable. The topics are separated by a comma, e.g., `last hour,last 3 hours,last 6 hours`.

## Installation

Copy the content of the `flow.json` file into the cliplborad an import it into your nore-red flow.

## Related work 

* [Noderes - Chart line color](https://discourse.nodered.org/t/chart-line-color/13427)
* [Dashboard chart - change line colour dependent on value](https://flows.nodered.org/flow/a78ac10821112eb07fb8be8957a9f7cb)




