# Customize Pie and Doughnut Chart Size in Syncfusion Blazor Charts

## Overview

This sample demonstrates how to customize the rendered size of pie and doughnut charts using the `Radius` property in the Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) component. The example uses an accumulation chart bound to browser usage statistics and configures a custom radius to control how much space the chart occupies within the available rendering area.

Adjusting the radius is useful when designing responsive dashboards, displaying multiple charts on a single page, or creating layouts that require additional space for legends, labels, and surrounding UI elements. The sample provides a simple implementation that illustrates how chart size can be controlled without modifying the underlying data source.

## Key Features

- Uses `SfAccumulationChart` to render a pie chart visualization.
- Configures `AccumulationChartSeries` with:
  - `DataSource="@StatisticsDetails"`
  - `XName="Browser"`
  - `YName="Users"`
  - `Radius="50%"`
- Demonstrates how the `Radius` property controls the size of pie and doughnut series based on the available chart area.
- Enables data labels using `AccumulationDataLabelSettings Visible="true"`.
- Displays a chart legend using `AccumulationChartLegendSettings Visible="true"`.
- Binds chart data using a local `Statistics` data model containing browser names and user counts.
- Uses percentage-based radius values for responsive chart sizing.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the project file:

   `SizeOfPieOrDoughnutChart/SizeOfPieOrDoughnutChart.csproj`

3. Restore NuGet packages.
4. Build the project.
5. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone or download this repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project directory:

```bash
cd SizeOfPieOrDoughnutChart
```

5. Restore NuGet packages:

```bash
dotnet restore
```

6. Run the application:

```bash
dotnet run
```

7. Open the local URL displayed in the console output.

## Project Structure

`SizeOfPieOrDoughnutChart/Pages/Index.razor` - Demonstrates the accumulation chart configuration and uses the `Radius="50%"` property to control chart size.

`SizeOfPieOrDoughnutChart/SizeOfPieOrDoughnutChart.csproj` - Project configuration containing framework and package reference information.

`pie-and-doughnut-size-customization.png` — Screenshot showing the rendered chart output.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Refer to the official documentation for the `Radius` property in accumulation charts: https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_Radius

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.