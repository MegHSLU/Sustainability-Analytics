# How to Use the Tourism in Luzern RMarkdown

## Quick Start

### Prerequisites

Make sure you have R installed on your system. The required packages are:
- tidyverse
- lubridate
- knitr
- rmarkdown

### Installation

Install the required packages in R:

```r
install.packages(c("tidyverse", "lubridate", "knitr", "rmarkdown"))
```

Or on Ubuntu/Debian systems:

```bash
sudo apt-get install r-cran-tidyverse r-cran-lubridate r-cran-knitr r-cran-rmarkdown
```

## Generating the Report

### Option 1: Using RStudio (Recommended)

1. Open `Tourism_Luzern.Rmd` in RStudio
2. Click the "Knit" button at the top of the editor
3. Select "Knit to HTML" or "Knit to PDF"
4. The report will be generated and automatically opened in your browser/viewer

### Option 2: Using R Command Line

Open R and run:

```r
rmarkdown::render("Tourism_Luzern.Rmd")
```

Or specify the output format:

```r
# For HTML output
rmarkdown::render("Tourism_Luzern.Rmd", output_format = "html_document")

# For PDF output (requires LaTeX)
rmarkdown::render("Tourism_Luzern.Rmd", output_format = "pdf_document")
```

### Option 3: Using Terminal/Command Line

```bash
R -e "rmarkdown::render('Tourism_Luzern.Rmd')"
```

## What the Report Contains

The generated report includes:

### 1. Executive Summary
A brief overview of the analysis objectives and key findings.

### 2. Introduction
- Background on tourism in Luzern
- Analysis objectives
- Importance of sustainable tourism

### 3. Data Overview
- Data sources and description
- Sample data generation (for demonstration)
- Data structure and variables

### 4. Tourism Trends Analysis
- **Overall visitor trends**: Time series visualization of total visitors
- **Domestic vs. International**: Breakdown of visitor origins
- **Seasonal patterns**: Monthly analysis showing peak and off-peak periods

### 5. Hotel and Accommodation Analysis
- Hotel occupancy rates over time
- Relationship between visitors and hotel nights
- Accommodation statistics

### 6. Sustainability Metrics
- **Environmental Impact**: CO2 emissions and waste generation
- **Public Transport Usage**: Percentage of tourists using public transportation
- **Environmental Efficiency**: Impact per visitor metrics

### 7. Year-over-Year Comparison
- Annual visitor statistics
- Growth rates and trends
- Performance metrics

### 8. Key Insights and Recommendations
- Key findings summary
- Sustainability recommendations
- Data-driven suggestions for tourism management

### 9. Appendices
- Data sources and references
- Technical information (R session info)
- Optional data export code

## Output Format

### HTML Output (Default)
- Interactive document with table of contents
- Responsive design that works on all devices
- Embedded charts and visualizations
- Can be opened in any web browser
- File: `Tourism_Luzern.html`

### PDF Output
- Print-ready document
- Professional formatting
- Suitable for reports and presentations
- Requires LaTeX installation
- File: `Tourism_Luzern.pdf`

## Customization

### Using Your Own Data

To use real tourism data instead of the sample data:

1. Open `Tourism_Luzern.Rmd`
2. Find the "Sample Data Creation" section (around line 77)
3. Replace the sample data code with your own data loading code:

```r
# Example: Load data from CSV
tourism_data <- read_csv("your_tourism_data.csv")

# Or from Excel
# library(readxl)
# tourism_data <- read_excel("your_tourism_data.xlsx")
```

4. Ensure your data has the required columns:
   - date
   - total_visitors
   - domestic_visitors
   - international_visitors
   - hotel_nights
   - occupancy_rate
   - public_transport_usage
   - co2_emissions_tons
   - waste_generated_tons

### Modifying Visualizations

All charts are created using ggplot2. To customize:

1. Find the relevant code chunk in the RMarkdown file
2. Modify colors, themes, or plot types as needed
3. Re-knit the document to see changes

### Adding New Sections

To add new analysis sections:

1. Create a new markdown header: `## Your Section Title`
2. Add a new R code chunk: ` ```{r your-chunk-name}`
3. Write your analysis code
4. Close the chunk: ` ``` `
5. Re-knit the document

## Troubleshooting

### Common Issues

**Issue: "Package X is not installed"**
- Solution: Install the required packages using `install.packages("package_name")`

**Issue: "Pandoc not found"**
- Solution: Install Pandoc from https://pandoc.org/ or install RStudio which includes Pandoc

**Issue: "LaTeX not found" (for PDF output)**
- Solution: Install TinyTeX: `tinytex::install_tinytex()` or install a full LaTeX distribution

**Issue: Charts not displaying**
- Solution: Ensure all required packages are loaded and data is properly formatted

## Tips

1. **Code Folding**: The HTML output includes code folding - click "Code" buttons to show/hide R code
2. **Table of Contents**: Use the floating TOC on the left to navigate between sections
3. **Reproducibility**: The report includes R session info for reproducibility
4. **Data Export**: Uncomment the export code in Appendix C to save processed data

## Further Help

For more information on RMarkdown:
- Official guide: https://rmarkdown.rstudio.com/
- RMarkdown book: https://bookdown.org/yihui/rmarkdown/
- RStudio cheatsheet: https://www.rstudio.com/resources/cheatsheets/

## Example Output Structure

When you knit the document, you'll see:

```
Tourism in Luzern: A Sustainability Analytics Perspective
├── Executive Summary
├── 1. Introduction
│   ├── 1.1 Background
│   └── 1.2 Objectives
├── 2. Data Overview
│   └── 2.1 Sample Data Creation
├── 3. Tourism Trends Analysis
│   ├── 3.1 Overall Visitor Trends
│   ├── 3.2 Domestic vs. International Visitors
│   └── 3.3 Seasonal Patterns
├── 4. Hotel and Accommodation Analysis
│   ├── 4.1 Hotel Occupancy Trends
│   └── 4.2 Relationship: Visitors vs. Hotel Nights
├── 5. Sustainability Metrics
│   ├── 5.1 Environmental Impact
│   ├── 5.2 Public Transport Usage
│   └── 5.3 Environmental Efficiency
├── 6. Year-over-Year Comparison
├── 7. Key Insights and Recommendations
│   ├── 7.1 Key Findings
│   └── 7.2 Sustainability Recommendations
├── 8. Conclusions
└── Appendix
    ├── A. Data Sources and References
    ├── B. Technical Information
    └── C. Data Export
```

Enjoy analyzing tourism in Luzern! 🏔️📊
