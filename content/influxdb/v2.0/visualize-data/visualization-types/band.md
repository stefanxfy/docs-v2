---
title: Band visualization
list_title: Band
list_image: /img/influxdb/2-0-visualizations-Band-example.png
description:
weight: 206
menu:
  influxdb_2_0:
    name: Band
    parent: Visualization types
---

The **Band** visualization displays the upper and lower boundaries for groups of data over time.

{{< img-hd src="/img/influxdb/2-0-visualizations-Band-example.png" alt="Band example" />}}

To view a band chart, select the **Band** option from the visualization dropdown in the upper left.

## Band behavior

Like a line graph, the band visualization shows how values change over time. Additionally, it displays upper and lower "bands" for the measurements.

For example, in the band chart above, the lines represent the mean `usage_system` values for the `cpu` measurement for `cpu0` and `cpu1`. The upper and lower limits of the bands are defined by the `max` and `min` aggregate functions, respectively.

## Band controls

To view **Band** controls, click **{{< icon "gear" >}} Customize** next to the visualization dropdown.

###### Data
- **X Column**: Select a column to display on the x-axis.
- **Y Column**: Select a column to display on the y-axis.
- **Time Format**: Select the time format. Options include:
    - `YYYY-MM-DD HH:mm:ss ZZ`
    - `DD/MM/YYYY HH:mm:ss.sss`
    - `MM/DD/YYYY HH:mm:ss.sss`
    - `MM/DD/YYYY HH:mm:ss.SSS`
    - `YYYY/MM/DD HH:mm:ss`
    - `hh:mm a`
    - `HH:mm`
    - `HH:mm:ss`
    - `HH:mm:ss.sss`
    - `MMMM D, YYYY HH:mm:ss`
    - `dddd, MMMM D, YYYY HH:mm:ss`

###### Aggregate functions
- **Upper Column Name**: Aggregate function to display for upper bounds of data.
- **Main Column Name**: Aggregate function to display for main graph line.
- **Lower Column Name**: Aggregate function to display for lower bounds of data.

###### Options
- **Interpolation**:
  - **Line**: Display a time series in a line graph.
  - **Smooth**: Display a time series in a line graph with smooth point interpolation.
  - **Step**: Display a time series in a staircase graph.
- **Line Colors**: Select a color scheme to use for your graph.
- **Hover Dimension**: Select the data to display in the tooltip when you hover over the graph:
  - **auto** or **X Axis**: Show all points with the same x value along the y-axis.
  - **Y Axis**: Show all points with the same y value along the x-axis.
  - **X & Y Axis**: Show only the point being currently hovered over.

###### Y Axis
- **Y Axis Label**: Label for the y-axis.
- **Y Value Unit Prefix**:
  - **None**: No prefix.
  - **SI**: International System of Units (SI) or metric prefix.
  - **Binary**: Binary multiple prefix.
- **Y Axis Prefix**: Prefix to be added to y-value.
- **Y Axis Suffix**: Suffix to be added to y-value.
- **Y Axis Domain**: The y-axis value range.
  - **Auto**: Automatically determine the value range based on values in the data set.
  - **Custom**: Manually specify the minimum y-axis value, maximum y-axis value, or range by including both.
      - **Min**: Minimum y-axis value.
      - **Max**: Maximum y-axis value.
