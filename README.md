# Sleep Data Analysis

This project performs an exploratory data analysis on sleep data exported from Apple Health.

## Goals

The main goals of this analysis are to:
- Explore the distribution and duration of different sleep stages.
- Analyze daily total sleep duration and identify potential outliers.
- Investigate monthly and seasonal sleep patterns.
- Examine the consistency of bedtime and the timing of key sleep stages (Deep and REM).
- Explore potential correlations between sleep duration and other health metrics like heart rate, step count, and active energy burned.

## Data Overview

The data used in this project is sourced from an Apple Health export. It includes records related to sleep analysis, heart rate, step count, active energy burned, resting heart rate, and heart rate variability (SDNN).

**Please note:** The original `export.xml` file containing personal health data is **not** included in this repository for privacy reasons.

## Key Findings

Based on the exploratory data analysis of the Apple Watch sleep data from 2024 onwards, here is a summary of the key findings:

*   **Sleep Stage Distribution:** The analysis of my sleep stage counts and average durations shows the proportion of time I spent in different sleep stages (Core, REM, Deep, Awake, In Bed). I observed the average duration for each stage, with 'In Bed' having the longest average duration, followed by Core, REM, Deep, and Awake.
*   **Daily Sleep Duration:** Visualizing my daily total sleep duration (excluding 'In Bed') revealed the overall trend and variability in my sleep time from night to night.
*   **Outlier Detection:** The box plot and histogram of my daily sleep duration helped in understanding the distribution of my sleep times and identifying potential outliers, which represent unusually short or long sleep nights for me.
*   **Monthly and Seasonal Patterns:** Analyzing the monthly average duration of my sleep stages and comparing my sleep patterns between summer and winter provided insights into potential seasonal influences on my sleep.
*   **Sleep Consistency:** Visualizing the distribution of my bedtime with an adjusted timeline showed the consistency of my sleep starting times.
*   **Timing of Sleep Stages:** The adjusted timeline histograms for Deep and REM sleep start times illustrated when these crucial sleep stages typically began during my sleep sessions.
*   **Correlations with Other Factors:** The expanded correlation heatmap showed the linear relationships between my daily sleep duration and other health metrics like my average heart rate, total step count, total active energy burned, average resting heart rate, and average HRV SDNN. I observed relatively weak linear correlations between my sleep duration and these activity/physiological metrics in this dataset.

These findings provide a good foundation for understanding my sleep patterns and how they relate to other aspects of my health data. Further analysis could delve deeper into specific periods, investigate the identified outliers, or explore non-linear relationships between the factors.

## How to View and Run the Analysis

You can explore this analysis in a few ways:

1.  **View on GitHub:** The most straightforward way is to view the `Sleep_Data_Analysis.ipynb` notebook directly on GitHub. The rendered notebook will show the code, outputs, and visualizations.
2.  **Open in Google Colab:** Click the "Open in Colab" badge at the top of the notebook file on GitHub to open and run the notebook interactively in Google Colab.
3.  **Run Locally with Jupyter Notebook:**
    *   Clone this repository to your local machine.
    *   Make sure you have Jupyter Notebook installed (`pip install notebook`).
    *   Install the required dependencies (see Dependencies below).
    *   Place your `export.xml` file (if you have one) in the project directory.
    *   Open a terminal in the project directory and run `jupyter notebook`.
    *   Open the `Sleep_Data_Analysis.ipynb` file in your browser.

## Dependencies

The required dependencies for this project are listed in the `requirements.txt` file. You can install them using pip:

```bash
pip install -r requirements.txt
```
