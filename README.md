# Sustainability-Analytics

Analysis of tourism patterns in Luzern, Switzerland, with a focus on sustainability metrics and environmental impact.

## Tourism in Luzern Project

This repository contains an RMarkdown analysis of tourism in Luzern, providing insights into visitor patterns, seasonal trends, and sustainability metrics.

### Contents

- **Tourism_Luzern.Rmd** - Main RMarkdown report analyzing tourism in Luzern

### Features

The RMarkdown document includes:

- **Tourism Trends Analysis**: Visitor arrivals, seasonal patterns, and year-over-year comparisons
- **Accommodation Statistics**: Hotel occupancy rates and visitor nights
- **Sustainability Metrics**: CO2 emissions, waste generation, and public transport usage
- **Visualizations**: Interactive charts and graphs for data exploration
- **Recommendations**: Data-driven insights for sustainable tourism management

### Requirements

To run the RMarkdown file, you need:

- R (version 4.0 or higher recommended)
- RStudio (optional but recommended)
- Required R packages:
  ```r
  install.packages(c("tidyverse", "lubridate", "knitr", "rmarkdown"))
  ```

### Usage

1. Open `Tourism_Luzern.Rmd` in RStudio
2. Click "Knit" button to generate the report
3. Choose output format (HTML or PDF)

Alternatively, from R console:
```r
rmarkdown::render("Tourism_Luzern.Rmd")
```

### Sample Data

The RMarkdown file includes sample data generation for demonstration purposes. For actual analysis, replace the sample data with real tourism statistics from:

- Swiss Federal Statistical Office (BFS)
- Luzern Tourism Board
- Hotel association statistics
- Visitor surveys

### Output

The report generates:
- Comprehensive HTML or PDF document
- Visualizations of tourism trends
- Statistical summaries and tables
- Sustainability insights and recommendations

### Contributing

Feel free to contribute by:
- Adding real data sources
- Enhancing visualizations
- Including additional sustainability metrics
- Improving analysis methods

### Contact

For questions or suggestions, please open an issue on GitHub.
