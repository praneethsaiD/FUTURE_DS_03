# College Event Feedback Analysis - Task 3

## Project Overview

This repository contains the solution for **Future Interns Data Science & Analytics Task 3: College Event Feedback Analysis**. The primary goal of this project was to analyze student feedback data from college events to understand satisfaction levels and identify areas for improvement. By leveraging Power BI, this project aims to transform raw survey responses into actionable insights for event organizers and campus management.

## Key Deliverables

* Cleaned Student Feedback Data (CSV format)
* Interactive College Event Feedback Dashboard (Power BI .pbix file)
* Summary of Key Insights and Recommendations based on rating analysis.

## Data Source

The analysis was performed on the `Student_Satisfaction_Survey.csv` dataset, which contains structured feedback on various college events and courses. This dataset includes numerical ratings (from 1 to 5) and associated metadata for different questions and courses.

The cleaned version of this data, `cleaned_student_feedback_data.csv` [cite: cleaned_student_feedback_data.csv], is available in this repository.

**Note on Textual Feedback:**
It's important to note that the provided `Student_Satisfaction_Survey.csv` dataset primarily contains numerical ratings and survey question text, but **does not include free-form student comments or open-ended textual feedback**. Therefore, the Natural Language Processing (NLP) and sentiment analysis components mentioned in the original task description (which rely on analyzing text comments) were not applicable to this specific dataset. The analysis in this project focuses exclusively on the quantitative rating data.

## Understanding Key Metrics & Data Structure

The dataset includes the following key columns relevant to the analysis:

* **`Question_Text`**: The specific survey question asked.
* **`Rating_Count_1` to `Rating_Count_5`**: Counts of how many times each rating (1 to 5) was selected for a given question and course.
* **`Total_Feedback_Given`**: The total number of responses received for a particular question-course combination.
* **`Average_Rating`**: The calculated average rating for each question-course combination (derived from the original dataset).
* **`Course_Name`**: The specific course or event name.
* **`Basic_Course_Category`**: A broader category for the course/event.

## Data Cleaning and Preparation (Using Power BI's Power Query)

The raw `Student_Satisfaction_Survey.csv` dataset was prepared for analysis directly within Power BI Desktop using its Power Query Editor. The key steps performed include:

* **Data Type Assignment:** Ensured all numerical columns (`Total_Feedback_Given`, `Rating_Count_1` to `Rating_Count_5`, `Average_Rating`) were correctly set as numeric data types (Whole Number or Decimal Number). Text columns were set as Text.
* **Column Renaming:** Renamed columns for clarity and consistency (e.g., `Total Feedback Given` to `Total_Feedback_Given`, `Questions` to `Question_Text`, etc.).
* **Average Rating Parsing:** While the Python script already created `Average_Rating`, if starting directly in Power BI, this would involve parsing the original `Average/ Percentage` column to extract the numerical average.
* **Data Validation:** Verified consistency between `Total_Feedback_Given` and the sum of `Rating_Count_1` to `Rating_Count_5`.

## Analysis Performed & Key Insights

The interactive Power BI dashboard provides a clear overview of student satisfaction:

1.  **Overall Satisfaction Levels:**
    * A high-level view of the `Overall_Average_Rating` across all feedback, indicating general student satisfaction.
    * Distribution of ratings (e.g., percentage of 5-star ratings) to show overall sentiment.

2.  **Satisfaction by Question:**
    * Identified the highest and lowest-rated questions, pinpointing specific areas of strength and weakness in events/courses.
    * *Example Insight: Questions related to 'teacher communication' or 'syllabus coverage' showed areas for potential improvement.*

3.  **Course/Event Performance:**
    * Comparison of average ratings across different `Course_Name` and `Basic_Course_Category` to highlight top-performing and underperforming courses/events.
    * *Example Insight: The 'FY B.VOC FOOD TECHNOLOGY' courses consistently received high satisfaction scores in specific areas.*

4.  **Rating Distribution:**
    * Visualizations showing the spread of 1-5 star ratings for various questions or courses, providing a deeper understanding beyond just the average.

## Tools Used

* **Power BI Desktop:** Used extensively for:
    * Data loading and transformation (Power Query Editor).
    * Creating measures and calculated columns (DAX).
    * Designing and building the interactive dashboard visuals.
* **Microsoft Excel:** (Potentially for initial CSV viewing before Power BI import).

## How to Access and Use the Dashboard

1.  **Clone the Repository:**
    ```bash
https://github.com/praneethsaiD/FUTURE_DS_03/blob/main/TASK%203.pbix

2.  **Open Power BI Dashboard:**
    * Ensure you have Power BI Desktop installed (download from [Power BI website](https://powerbi.microsoft.com/en-us/downloads/)).
    * Open the `.pbix` file

3.  **Explore the Dashboard:**
    * The dashboard features interactive filters (slicers) for `Course_Name` and `Basic_Course_Category`, allowing for dynamic data exploration.
    * Hover over visuals for detailed tooltips and deeper insights.

## Future Enhancements

* **Integrate Textual Feedback:** If future datasets include open-ended comments, Natural Language Processing (NLP) techniques (e.g., sentiment analysis with TextBlob/VADER, topic modeling) could be applied to extract qualitative insights and create word clouds of common themes/complaints.
* **Time-Series Analysis:** If event dates were available, analyze satisfaction trends over time.
* **Correlation with Event Type:** Further explore correlations between feedback and specific event characteristics (e.g., workshop, seminar, cultural fest).
* **User-Level Analysis:** If individual student IDs were present and linked across events, analyze individual student satisfaction journeys.

## Contact

Feel free to reach out if you have any questions or feedback!

* **Your Name:** Donthireddy Praneeth Sai Durga Reddy
* **LinkedIn:** www.linkedin.com/in/donthireddy-praneeth-sai-durga-reddy
* **Email:** praneethsaidurgareddy@gmail.com
