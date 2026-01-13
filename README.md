# How-to-set-size-of-pie-doughnut-in-Blazor-chart

This article explains how to set the size of pie or doughnut chart in Blazor Chart Component.

**Customizing the size of a pie or doughnut chart**

The [Radius](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_Radius) property determines the size of pie and doughnut series based on the available space in [Blazor Chart](https://www.syncfusion.com/blazor-components/blazor-charts).  It accepts values from 0 to 100%, with the default set at 80%. By default, pie and doughnut series occupy 80% of the available space, taking the minimum of the chart width and height.

The following code example illustrates pie with default size and pie with 50% of available size.

**Index.razor**

```cshtml

@using Syncfusion.Blazor.Charts

<div class="chart-column">
    <div >
        <SfAccumulationChart Title="Pie with default size" Width="500"  >
            <AccumulationChartBorder Width="2" Color="red"></AccumulationChartBorder>
            <AccumulationChartSeriesCollection>
                <AccumulationChartSeries DataSource="@StatisticsDetails" XName="Browser" YName="Users">
                    <AccumulationDataLabelSettings Visible=true></AccumulationDataLabelSettings>
                </AccumulationChartSeries>
            </AccumulationChartSeriesCollection>
            <AccumulationChartLegendSettings Visible="false"></AccumulationChartLegendSettings>
        </SfAccumulationChart>
    </div> 
    <div >
        <SfAccumulationChart Title="Pie with 50% of available size" Width="500">
            <AccumulationChartBorder Width="2" Color="red"></AccumulationChartBorder>
        <AccumulationChartSeriesCollection>
            <AccumulationChartSeries DataSource="@StatisticsDetails" XName="Browser" YName="Users" Radius="50%">
                <AccumulationDataLabelSettings Visible=true></AccumulationDataLabelSettings>
            </AccumulationChartSeries>
        </AccumulationChartSeriesCollection>
        <AccumulationChartLegendSettings Visible="false"></AccumulationChartLegendSettings>
    </SfAccumulationChart>
    </div>
</div>

<style>
    .chart-column {
        display: flex;
        flex-direction: row;
        padding: 10px;
    }        
</style>

@code {
    public class Statistics
    {
        public string Browser { get; set; }
        public double Users { get; set; }
    }

    public List<Statistics> StatisticsDetails = new List<Statistics>
    {
        new Statistics { Browser = "Chrome", Users = 37 },
        new Statistics { Browser = "UC Browser", Users = 17 },
        new Statistics { Browser = "iPhone", Users = 19 },
        new Statistics { Browser = "Others", Users = 4  },
        new Statistics { Browser = "Opera", Users = 11 },
        new Statistics { Browser = "Android", Users = 12 },
    };
}

```

The following screenshot illustrates pie with default size and pie with 50% of available size.

**Output**

![](/pie-and-doughnut-size-customization.png)

**Conclusion**

I hope you enjoyed learning how to customize pie and doughnut size in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!