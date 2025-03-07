# **Hiring Process Analysis - Power BI Dashboard**

![Dashboard Preview](insert_image_link_here)

## **📌 Project Overview**
This Power BI dashboard provides a detailed analysis of the hiring process, helping HR professionals and business leaders make data-driven decisions. It visualizes key hiring metrics such as total hires, rejections, hiring conversion rates, salary distributions, and gender-based hiring trends.

## **🎯 Key Features & Insights**
- **Total Hires vs. Rejections**: Trend analysis to track hiring success over time.
- **Department-wise Hiring Breakdown**: Gender distribution of hires across departments.
- **Salary Insights**: Salary percentiles and variations by job role.
- **Hiring Efficiency**: Overall conversion rate to measure hiring effectiveness.

## **📊 Tools & Technologies Used**
- **Power BI** – Data visualization and DAX measures
- **Excel** – Data cleaning and preprocessing
- **DAX (Data Analysis Expressions)** – Custom measures and calculated columns

## **📂 Project Files**
- `hiring_analysis_cleaned.xlsx` - Cleaned and structured dataset
- `Hiring_Dashboard.pbix` - Power BI file with all visuals and DAX measures
- `README.md` - Project documentation

## **📈 Power BI Visuals Used**
- **KPI Cards** – Total Hires, Total Rejections, Hiring Conversion Rate
- **Bar Chart** – Department-wise hiring breakdown by gender
- **Scatter Plot** – Salary percentiles by job role and department
- **Line Chart** – Total hires vs. rejections over time

## **📢 How to Use the Dashboard**
1. **Download the Power BI file (`.pbix`)** from this repository.
2. Open it using **Power BI Desktop**.
3. Explore interactive visuals, filter data, and derive key insights!

## **💡 Key DAX Measures Used**
```DAX
Hiring Conversion Rate = 
DIVIDE([Total Hires], [Total Hires] + [Total Rejections]) * 100

Salary Variance = 
VAR DeptAvg = CALCULATE(AVERAGE('Hire'[Offered Salary]), ALLEXCEPT('Hire', 'Hire'[Department]))
RETURN 'Hire'[Offered Salary] - DeptAvg

Salary Percentiles = 
RANKX(
    FILTER('Hire', 'Hire'[Post Name] = SELECTEDVALUE('Hire'[Post Name])),
    'Hire'[Offered Salary], , DESC, DENSE
)
```

## **📎 Additional Enhancements**
- Applied **gradient background** for an appealing UI.
- Used **data labels & tooltips** for better insights.
- Optimized **data model** for smooth performance.

## **🔗 Connect & Feedback**
I'm always looking to improve! Feel free to **connect with me on LinkedIn** and share your thoughts. 🚀  
📌 **LinkedIn:** [Insert your LinkedIn link here]  
📌 **GitHub Repo:** [Insert this repo link]

---

### ⭐ If you find this project useful, don’t forget to **star this repository** on GitHub!
