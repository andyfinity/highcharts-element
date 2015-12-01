# Highcharts element #

This is a simple helper element to easily chart any data. This element only depends on Polymer and Highcharts, and it **does not depend on jQuery** or any other JS library. Therefore it has a smaller memory footprint than comperable Highcharts elements.

If you are already importing jQuery into your project and are using it elsewhere, please consider using one of the many other charting libraries available to Polymer.

## Usage ##

Simply pass in the options array just as you would with a regular Highcharts chart.

    <highcharts-element options="[[options]]"></highcharts-element>

Or if you want a bit more advanced functionality, you can ask for the chart object back and register some event callbacks.

    <highcharts-element options="[[options]]" chart="{{chart}}" on-load="handlerFunction"></highcharts-element>

The complete list of events are as follows:

Name | Description
-----|--------------
`chart-add-series` | A series is added to the chart
`chart-after-print` | After a chart has been printed (through the context menu item or `Chart.print` method)
`chart-before-print` | Before a chart is printed (through the context menu item or `Chart.print` method)
`chart-click` | User clicked on the background
`chart-drill-down` | A drilldown point is clicked
`chart-drill-up` | Drilling up from a drill-down point
`chart-load` | Chart has finished loading
`chart-redraw` | Chart is redrawn (after an axis, series, or point is modified)
`chart-selection` | An area of the chart has been selected
`series-after-animate` | Series has finished being painted
`series-checkbox-click` | Checkbox next to the series' name in the legend is clicked
`series-click` | User clicked on the series
`series-hide` | Series is hidden after chart was generated
`series-legend-item-click` | Legend item belonging to the series is clicked
`series-mouse-out` | Mouse leaves the graph
`series-mouse-over` | Mouse enters the graph
`series-show` | Series is shown after chart was generated
`point-click` | User clicked a point
`point-mouse-out` | Mouse leaves the area close to a point
`point-mouse-over` | Mouse enters the area close to a point
`point-remove` | Point is removed using the `.remove()` method
`point-select` | Point is selected programmatically or on click
`point-unselect` | Point is unselected programmatically or on click
`point-update` | Point is updated using the `.update()` method

There are also a couple of styling mix-ins available for use:

Custom property | Description | Default
----------------|-------------|----------
`--highcharts-container` | Mixin applied to the element holding the chart | [`{...}`](http://api.highcharts.com/highcharts#chart.style)
`--highcharts-tooltip` | Mixin applied to the tooltips that appear when hovering | [`{...}`](http://api.highcharts.com/highcharts#tooltip.style)

## Limitations and future work ##

* Only uses the built-in Highcharts JS library. Future work will allow for use of any JS library that is also supported by Highcharts.
* This code is somewhat untested, so futue work will involve more thorough testing.

## Documentation ##

API documentation and demos are provided in the repo.

## License ##

Right now this is licensed under the Apache 2.0 license, mainly because it was on the top of the list. If anyone has any reason why I should change it, let me know.
