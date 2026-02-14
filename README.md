# Road Accident Analysis 🚗📊

A comprehensive data analysis project focused on analyzing road accident patterns across major Indian states from 2010 to 2022. This project provides insights into accident trends, severity, vehicle types involved, and state-wise comparisons to help understand road safety patterns.

## 📋 Project Overview

This project analyzes road accident data from six major Indian states (Uttar Pradesh, Maharashtra, Tamil Nadu, Karnataka, West Bengal, and Rajasthan) spanning 13 years (2010-2022). The analysis includes various metrics such as:

- Total number of accidents
- Persons killed and injured
- Major vehicle types involved in accidents
- Severity index calculations
- Year-over-year trends
- State-wise comparisons

## 📊 Dataset Information

### Data Files

1. **road_accidents_sample.csv**: Raw accident data containing:
   - `Year`: Year of the accident (2010-2022)
   - `State/UT`: State or Union Territory name
   - `Total Accidents`: Total number of accidents reported
   - `Persons Killed`: Number of fatalities
   - `Persons Injured`: Number of people injured
   - `Major Vehicle Type`: Primary vehicle type involved (Two-wheeler, Four-wheeler, Heavy Vehicle, Others)

2. **road_accidents_processed.csv**: Processed data with additional calculated metrics:
   - All columns from the sample data
   - `Severity Index`: Calculated metric indicating accident severity

### Data Coverage

- **Time Period**: 2010-2022 (13 years)
- **States Covered**: 6 major states
  - Uttar Pradesh
  - Maharashtra
  - Tamil Nadu
  - Karnataka
  - West Bengal
  - Rajasthan
- **Total Records**: 78 data points
- **Vehicle Categories**: 
  - Two-wheelers
  - Four-wheelers
  - Heavy Vehicles
  - Others

## 🎯 Key Features

- **Temporal Analysis**: Year-wise trend analysis of accidents, fatalities, and injuries
- **Geographical Analysis**: State-wise comparison and patterns
- **Vehicle Type Analysis**: Distribution of accidents by vehicle type
- **Severity Assessment**: Calculated severity index for each incident
- **Visual Reports**: Comprehensive PDF report with visualizations and insights

## 📁 Repository Structure

```
Road-Accident-Analysis/
├── README.md                              # Project documentation (this file)
├── Road_Accident_Report_Shreyansh.pdf    # Detailed analysis report with visualizations
├── road_accidents_sample.csv              # Raw accident data
├── road_accidents_processed.csv           # Processed data with severity index
└── .ipynb_checkpoints/                    # Jupyter notebook checkpoints
```

## 🔍 Analysis Highlights

Based on the dataset, the analysis provides insights into:

1. **Accident Trends**: Understanding how road accidents have evolved over the 13-year period
2. **High-Risk States**: Identifying states with higher accident rates
3. **Vehicle-Related Patterns**: Analyzing which vehicle types are most frequently involved in accidents
4. **Severity Metrics**: Calculating and comparing accident severity across different parameters
5. **Casualty Analysis**: Examining the relationship between accidents and casualties (deaths and injuries)

## 📈 Severity Index

The processed dataset includes a calculated **Severity Index** that helps quantify the severity of accidents based on:
- Number of persons killed
- Number of persons injured
- Total accidents

This metric enables comparative analysis across different states and time periods.

## 🛠️ Technologies Used

- **Data Analysis**: Python (implied from .ipynb_checkpoints)
- **Data Storage**: CSV format
- **Visualization**: Included in the PDF report
- **Documentation**: Markdown, PDF

## 📖 Usage

### Prerequisites

To work with this project, you'll need:
- Python 3.x
- Jupyter Notebook (for interactive analysis)
- Common data analysis libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn (optional, for advanced visualizations)

### Getting Started

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ShreyanshMishra1202/Road-Accident-Analysis.git
   cd Road-Accident-Analysis
   ```

2. **Load the data**:
   ```python
   import pandas as pd
   
   # Load raw data
   raw_data = pd.read_csv('road_accidents_sample.csv')
   
   # Load processed data with severity index
   processed_data = pd.read_csv('road_accidents_processed.csv')
   ```

3. **Explore the analysis**:
   - Review the `Road_Accident_Report_Shreyansh.pdf` for detailed findings
   - Use the CSV files for your own custom analysis

### Sample Analysis

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the processed data
df = pd.read_csv('road_accidents_processed.csv')

# Example: Analyze accidents by state
state_summary = df.groupby('State/UT').agg({
    'Total Accidents': 'sum',
    'Persons Killed': 'sum',
    'Persons Injured': 'sum'
}).sort_values('Total Accidents', ascending=False)

print(state_summary)

# Example: Year-wise trend
yearly_trend = df.groupby('Year').agg({
    'Total Accidents': 'sum',
    'Persons Killed': 'sum',
    'Persons Injured': 'sum'
})

yearly_trend.plot(kind='line', figsize=(12, 6))
plt.title('Yearly Trend of Road Accidents')
plt.xlabel('Year')
plt.ylabel('Count')
plt.legend(['Total Accidents', 'Persons Killed', 'Persons Injured'])
plt.grid(True)
plt.show()
```

## 📊 Key Insights

The analysis reveals several important findings:

1. **State-wise Patterns**: Different states show varying accident patterns and severity levels
2. **Vehicle Type Distribution**: Two-wheelers, four-wheelers, and heavy vehicles contribute differently to accident statistics
3. **Temporal Trends**: Accident patterns show variations across the 13-year period
4. **Severity Variations**: The severity index ranges from approximately 2.0 to 8.0, indicating significant variation in accident impact

## 🎓 Applications

This analysis can be useful for:

- **Policy Makers**: Understanding road safety challenges and formulating targeted interventions
- **Research**: Academic research on road safety and accident prevention
- **Urban Planning**: Infrastructure development and road safety improvements
- **Insurance**: Risk assessment and premium calculations
- **Public Awareness**: Educational campaigns about road safety

## 🤝 Contributing

Contributions are welcome! If you'd like to improve the analysis or add new features:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new analysis'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Create a Pull Request

## 👤 Author

**Shreyansh Mishra**
- GitHub: [@ShreyanshMishra1202](https://github.com/ShreyanshMishra1202)

## 📄 License

This project is available for educational and research purposes. Please provide appropriate attribution when using this data or analysis.

## 📞 Contact

For questions, suggestions, or collaboration opportunities, please:
- Open an issue in this repository
- Contact through GitHub

## 🙏 Acknowledgments

- Data sources and methodologies used in this analysis
- Open-source community for tools and libraries
- All contributors and supporters of road safety research

---

**Note**: This analysis is based on sample data for the specified states and time period. For comprehensive national-level analysis, additional data sources may be required.

## 📚 Additional Resources

For more detailed analysis and visualizations, please refer to:
- `Road_Accident_Report_Shreyansh.pdf` - Comprehensive report with visualizations and detailed findings

---
