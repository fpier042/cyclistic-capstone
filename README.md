# Cyclistic Bike-Share Analysis

**Converting Casual Riders to Annual Members: A Data-Driven Strategy**

---

## Overview

This capstone project analyzes 3.8 million bike trips from Chicago's Cyclistic bike-share program (Jan-Aug 2024) to answer a critical business question: **How do annual members and casual riders use Cyclistic bikes differently?**

The analysis reveals distinct behavioral patterns that inform three strategic recommendations projected to convert 105,000+ casual riders to annual members.

---

## Key Findings

### Behavioral Differences Discovered:

1. **Trip Duration**: Casual riders take **2.4x longer trips** (22.7 vs 12.8 minutes)
   - Indicates leisure/recreational usage vs efficient commuting
   
2. **Temporal Patterns**: Casual riders show **38.3% weekend usage** (vs 24.4% for members)
   - Clear leisure behavior pattern vs commuter pattern

3. **Seasonal Trends**: **13x growth** in casual ridership from January to August
   - Reveals massive summer conversion opportunity window

### Business Impact:

Based on 8 months of data analysis, three targeted conversion strategies are projected to convert **5-10% of summer casual riders**, representing **105,000-210,000 new annual members**.

---

## Data Sources

**Dataset**: Divvy System Data (representing fictional Cyclistic bike-share)
- **Time Period**: January - August 2024 (8 months)
- **Records Analyzed**: 3,799,262 trips after cleaning
- **Raw Data Size**: ~970 MB across 8 monthly files
- **Processed Data**: 812 MB CSV / 183 MB Parquet
- **License**: Public dataset, Motivate International Inc.

**Data Reliability**:
- First-party operational data
- 76.5% retention rate after rigorous quality controls
- Complete seasonal coverage including peak summer period

**Note**: Raw data files are not included in this repository due to size constraints. Data can be obtained from [Divvy System Data](https://divvy-tripdata.s3.amazonaws.com/index.html).

---

## Methodology

This project follows the **Google Data Analytics 6-phase framework**:

### 1. ASK
- **Business Question**: How do annual members and casual riders use Cyclistic bikes differently?
- **Stakeholder**: Lily Moreno, Director of Marketing
- **Goal**: Develop data-driven conversion strategies

### 2. PREPARE
- Downloaded 12 months of trip data (Jan-Dec 2024)
- Verified data integrity and reliability (ROCCC framework)
- Identified 8 clean months suitable for analysis
- Organized project structure and documentation

### 3. PROCESS
- **Tool Selection**: Python with pandas (dataset size: 3.8M records)
- **Data Cleaning**: Duration filters, geographic bounds, duplicate removal
- **Feature Engineering**: Created temporal variables (hour, day_of_week, is_weekend)
- **Quality Assurance**: 76.5% retention rate with comprehensive validation

### 4. ANALYZE
- **Descriptive Statistics**: Mean, median, mode for key metrics
- **Comparative Analysis**: Member vs casual behavioral patterns
- **Statistical Testing**: t-tests for significance (p < 0.001)
- **Temporal Analysis**: Hourly, daily, weekly, and seasonal patterns
- **Geographic Analysis**: Station preferences and usage density

### 5. SHARE
- Created 6 high-quality visualizations (300 DPI)
- Developed professional HTML presentation
- Generated executive-ready insights and recommendations
- Published portfolio showcase

### 6. ACT
- Three strategic recommendations with implementation roadmap
- Success metrics and KPIs defined
- Phased rollout timeline (May-September)
- Expected ROI: 105K-210K new members

---

## Tools & Technologies

**Data Processing & Analysis**:
- Python 3.x
- pandas - Data manipulation and analysis
- NumPy - Numerical computations

**Visualization**:
- matplotlib - Statistical visualizations
- seaborn - Advanced plotting

**Development Environment**:
- Google Colab - Cloud-based Jupyter notebooks
- Google Drive - Data storage and collaboration

**Version Control**:
- Git/GitHub - Code repository and documentation

---

## Repository Structure

```
cyclistic-capstone/
├── notebooks/
│   ├── 01_data_processing_cyclistic.ipynb
│   └── 02_descriptive_statistics_and_user_behavior.ipynb
├── visualizations/
│   ├── 01_executive_dashboard.png
│   ├── 02_trip_duration_comparison.png
│   ├── 03_temporal_patterns.png
│   ├── 04_seasonal_opportunity.png
│   ├── 05_geographic_insights.png
│   └── 06_key_metrics_comparison.png
├── reports/
│   └── cyclistic_presentation.html
├── documentation/
│   ├── data_cleaning_process.md
│   ├── analysis_methodology.md
│   └── data_dictionary.md
├── README.md
└── requirements.txt
```

---

## Key Results

### Business Recommendations:

**1. Summer Conversion Blitz**
- **Strategy**: Launch intensive membership campaigns during June-August
- **Data Support**: 13x seasonal growth, July peak (765K trips)
- **Target**: 2.1M summer casual trips
- **Tactics**: Targeted digital ads, early-bird discounts, conversion booths

**2. Weekend Warrior Membership**
- **Strategy**: Create weekend-focused membership tier
- **Data Support**: 38.3% weekend usage by casual riders
- **Target**: 1.09M weekend casual trips
- **Tactics**: Weekend-only pricing, attraction partnerships, leisure messaging

**3. Location-Based Conversion Hubs**
- **Strategy**: Deploy conversion resources at high-casual-activity stations
- **Data Support**: Geographic clustering of casual vs member preferences
- **Target**: Top 20% of stations account for 89.1% of trips
- **Tactics**: On-site kiosks, street teams, instant trial memberships

### Expected Impact:

**Conservative Scenario (5% conversion)**:
- New annual members: 105,000
- Revenue opportunity: Significant membership growth
- Implementation timeline: May-September 2024

**Optimistic Scenario (10% conversion)**:
- New annual members: 210,000
- Market share gain: Substantial
- Long-term value: High member retention

---

## Installation & Usage

### Prerequisites:
```bash
Python 3.7+
pandas
numpy
matplotlib
seaborn
jupyter
```

### Setup:
```bash
# Clone the repository
git clone https://github.com/fpier042/cyclistic-capstone.git
cd cyclistic-capstone

# Install required packages
pip install -r requirements.txt

# Launch Jupyter notebooks
jupyter notebook
```

### Running the Analysis:
1. Open `01_data_processing_cyclistic.ipynb` to see data cleaning process
2. Open `02_descriptive_statistics_and_user_behavior.ipynb` for complete analysis
3. View `reports/cyclistic_presentation.html` for executive summary

---

## Visualizations

### Sample Insights:

**Trip Duration Comparison**:
Casual riders average 22.7 minutes per trip vs 12.8 minutes for members, indicating leisure vs commute behavior.

**Seasonal Growth Pattern**:
Casual ridership grows 13x from January (29K trips) to July peak (375K trips), revealing prime conversion window.

**Temporal Usage Patterns**:
Weekend usage: Casual (38.3%) vs Members (24.4%), confirming distinct leisure vs commuter segments.

*View all 6 visualizations in the `/visualizations` folder.*

---

## Challenges & Solutions

### Challenge 1: Data Corruption
**Problem**: September-December 2024 files contained corrupted timestamps  
**Solution**: Focused analysis on 8 clean months (Jan-Aug), which still captured complete seasonal transition including critical summer peak period

### Challenge 2: Dataset Scale
**Problem**: 3.8M records too large for spreadsheet tools  
**Solution**: Used Python with pandas, implementing chunked processing for memory efficiency

### Challenge 3: Scope Adaptation
**Problem**: Balancing complete annual coverage with data quality  
**Solution**: Prioritized clean data over coverage; 8 months provided sufficient statistical power for robust business recommendations

---

## Documentation

**Comprehensive documentation available**:
- [Data Cleaning Process](documentation/data_cleaning_process.md) - Detailed cleaning methodology and quality metrics
- [Analysis Methodology](documentation/analysis_methodology.md) - Statistical approach and validation
- [Data Dictionary](documentation/data_dictionary.md) - Complete variable reference
- [Project Progress Log](documentation/project_progress_log.md) - Development timeline and decisions

---

## Project Links

- **Live Portfolio**: [View Project Showcase](https://sites.google.com/view/my-data-portfolio-feltonpierre/capstone-project)
- **Interactive Presentation**: [HTML Presentation](#) *(to be hosted)*
- **LinkedIn**: [Project Post](#) *(optional)*

---

## Lessons Learned

**Technical Skills Developed**:
- Large-scale data processing with pandas
- Statistical analysis and hypothesis testing
- Professional data visualization for business audiences
- End-to-end data analysis project execution

**Business Acumen Gained**:
- Translating data insights into business strategy
- Stakeholder-focused communication
- ROI-driven recommendation development
- Implementation planning and success metrics

**Problem-Solving Experience**:
- Handling real-world data quality issues
- Adapting project scope while maintaining value
- Balancing technical depth with business clarity

---

## Future Enhancements

Potential extensions of this analysis:
- Geographic heat mapping with interactive visualizations
- Predictive modeling for conversion likelihood
- A/B testing framework for campaign optimization
- Real-time dashboard for ongoing monitoring
- Weather correlation analysis for seasonal patterns

---

## Contact

**Felton Pierre**
- Portfolio: [https://sites.google.com/view/my-data-portfolio-feltonpierre](https://sites.google.com/view/my-data-portfolio-feltonpierre)
- GitHub: [@fpier042](https://github.com/fpier042)
- LinkedIn: [Your LinkedIn](#)
- Email: [Your Email]

---

## Acknowledgments

- **Google Data Analytics Professional Certificate** for the capstone framework
- **Motivate International Inc.** for providing the Divvy System Data
- **Coursera** for the educational platform

---

## License

This project is available under the MIT License. The underlying Divvy data is provided by Motivate International Inc. under their data license agreement.

---

**Project Status**: Complete  
**Last Updated**: October 2024  
**Version**: 1.0

---

*This project demonstrates end-to-end data analysis capabilities including data cleaning, statistical analysis, visualization, and business strategy development.*
