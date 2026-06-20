# Skill Graph Clustering & Learner Segmentation using Unsupervised Learning

## AI/ML Developer Task 11

### Submitted By
AI/ML Developer

### Project Overview

This project presents an Artificial Intelligence driven framework for identifying skill gaps, learner segmentation, future skill prediction, and personalized recommendation generation using machine learning techniques.

The framework combines:

- K-Means Clustering
- Association Rule Mining
- Random Forest Regression

to create a comprehensive educational analytics system.

The objective is to transform educational data into actionable insights that improve learning outcomes and support educational decision making.

---

# Executive Summary

The rapid growth of digital education platforms has generated large volumes of learner data. Every assessment, assignment submission, login activity, and skill development exercise contributes valuable information regarding learner behavior and educational performance.

Despite the availability of such data, many educational institutions struggle to utilize it effectively.

Traditional educational systems often rely on standardized learning approaches where every learner receives the same content regardless of proficiency level, learning pace, or educational requirements.

This project addresses these limitations through the application of machine learning.

The proposed framework performs:

- Skill Gap Analysis
- Learner Segmentation
- Future Skill Prediction
- Personalized Recommendation Generation

The resulting system enables educational institutions to:

- Identify struggling learners
- Detect skill deficiencies
- Personalize learning pathways
- Improve educational outcomes

---

# Business Problem

Educational institutions face several challenges.

## Challenge 1: Lack of Personalization

Students possess different:

- Learning speeds
- Educational backgrounds
- Skill levels
- Career goals

Traditional systems frequently ignore these differences.

Consequences include:

- Reduced engagement
- Slower learning
- Poor retention

---

## Challenge 2: Delayed Intervention

Learners are often identified as at-risk only after performance declines significantly.

Consequences include:

- Poor academic performance
- Increased dropout rates
- Reduced confidence

---

## Challenge 3: Hidden Learning Patterns

Educational datasets contain valuable information regarding:

- Skill relationships
- Learning pathways
- Success indicators

Without advanced analytics these patterns remain undiscovered.

---

## Challenge 4: Resource Allocation

Support resources are frequently distributed uniformly despite varying learner requirements.

This reduces efficiency and limits educational impact.

---

# Dataset Overview

The dataset was designed to simulate realistic learner behavior.

## Dataset Statistics

| Metric | Value |
|----------|----------|
| Students | 150 |
| Skills | 25 |
| Records | 3750 |
| Categories | 6 |

---

## Dataset Features

### Student_ID

Unique learner identifier.

Purpose:

- Student tracking
- Recommendation assignment
- Cluster membership monitoring

---

### Skill_Name

Represents the skill being evaluated.

Examples:

- Python
- SQL
- Machine Learning
- Deep Learning
- Cybersecurity

---

### Skill_Score

Measures current learner proficiency.

Range:

40–100

Purpose:

- Skill evaluation
- Prediction target
- Recommendation generation

---

### Assessment_Score

Represents examination performance.

Purpose:

- Knowledge evaluation
- Learning outcome measurement

---

### Learning_Hours

Measures learner effort.

Purpose:

- Engagement analysis
- Efficiency calculation

---

### Assignment_Completion_Rate

Measures coursework consistency.

Purpose:

- Engagement monitoring
- Performance evaluation

---

### Login_Frequency

Represents platform participation.

Purpose:

- Engagement analysis
- Behavioral monitoring

---

### Skill_Category

Groups skills into educational domains.

Examples:

- Programming
- AI
- Analytics
- Cloud
- Engineering

---

### Proficiency_Level

Categorizes learners into:

- Beginner
- Intermediate
- Advanced

---

# Data Preprocessing

Raw educational data frequently contains inconsistencies.

Preprocessing improves data quality and machine learning performance.

The following steps were applied:

1. Missing Value Handling
2. Duplicate Removal
3. Feature Encoding
4. Feature Scaling
5. Outlier Analysis

---

## Missing Value Handling

Missing values negatively affect machine learning performance.

Median imputation was selected because:

- Resistant to outliers
- Preserves distribution
- Improves robustness

---

## Duplicate Removal

Duplicate observations introduce bias.

Benefits of removal:

- Improved accuracy
- Reduced distortion
- Better generalization

---

## Feature Encoding

Categorical variables cannot be processed directly by machine learning algorithms.

Label Encoding was applied to:

- Skill_Name
- Skill_Category
- Proficiency_Level

---

## Feature Scaling

StandardScaler was applied.

Benefits:

- Balanced feature influence
- Better clustering
- Improved convergence

---

# Feature Engineering

Feature engineering creates additional educational insights.

Three engineered variables were generated.

---

## Engagement Score

Combines:

- Login Frequency
- Assignment Completion
- Course Completion

Purpose:

Measure overall participation.

---

## Learning Efficiency

Formula:

Learning Efficiency = Assessment Score / Learning Hours

Purpose:

Evaluate learning productivity.

---

## Skill Gap Index

Formula:

Skill Gap Index = Assessment Score − Skill Score

Purpose:

Identify learning deficiencies.

---

# Summary

The preprocessing and feature engineering stages establish a reliable foundation for machine learning analysis and educational insight generation.

# Exploratory Data Analysis (EDA)

## Introduction

Exploratory Data Analysis (EDA) was performed to understand learner behavior, identify educational patterns, evaluate skill distributions, and discover insights that support machine learning development.

The primary objectives were:

- Understand learner performance
- Identify skill deficiencies
- Analyze engagement patterns
- Discover educational trends
- Support model development

EDA transforms raw educational data into meaningful information that can support educational decision-making.

---

# Skill Distribution Analysis

## Objective

The objective of this analysis is to evaluate learner proficiency across all skills and identify educational strengths and weaknesses.

---

## Skill Distribution Visualization

<div align="center">
<img src="skill_distribution.png" width="850">
</div>

---

## Analysis

The Skill Distribution chart displays the average proficiency achieved for each skill within the learner population.

Several observations emerge from the analysis.

### High Proficiency Skills

Skills demonstrating higher average proficiency represent educational strengths.

Examples include:

- Communication
- Problem Solving
- SQL
- Excel

Possible reasons include:

- Frequent exposure
- Practical application
- Strong curriculum alignment

Students generally demonstrate confidence when working with these skills.

---

### Medium Proficiency Skills

Several skills demonstrate moderate performance.

Examples:

- Statistics
- Power BI
- Data Visualization
- Cloud Fundamentals

These skills often require additional reinforcement and practical exposure.

Recommended interventions include:

- Hands-on projects
- Industry case studies
- Interactive learning activities

---

### Low Proficiency Skills

Several advanced skills demonstrate lower proficiency.

Examples:

- Deep Learning
- Cybersecurity
- Computer Vision
- Data Engineering

Potential causes include:

- Technical complexity
- Prerequisite requirements
- Limited practical experience

Educational institutions should prioritize support for these areas.

---

## Educational Significance

Skill distribution analysis enables institutions to:

- Evaluate curriculum effectiveness
- Identify educational strengths
- Detect learning deficiencies
- Improve resource allocation

---

# Skill Gap Analysis

## Introduction

Skill Gap Analysis evaluates discrepancies between learner proficiency and expected performance.

The objective is to identify educational deficiencies and intervention opportunities.

---

## Skill Gap Heatmap

<div align="center">
<img src="skill_gap_heatmap.png" width="850">
</div>

---

## Interpretation

The heatmap visualizes learning deficiencies across students and skills.

Color intensity reflects the magnitude of skill gaps.

### Red Regions

Red regions indicate:

- Significant deficiencies
- High intervention priority
- Increased educational risk

These learners require immediate support.

---

### Blue Regions

Blue regions indicate:

- Strong proficiency
- Lower educational risk
- Consistent performance

These learners may benefit from advanced educational opportunities.

---

## Learner Risk Categories

### Low Risk

Characteristics:

- Strong proficiency
- Consistent engagement
- Small learning gaps

---

### Medium Risk

Characteristics:

- Moderate deficiencies
- Variable performance

---

### High Risk

Characteristics:

- Large learning gaps
- Lower engagement
- Higher intervention requirements

---

## Educational Benefits

Skill Gap Analysis supports:

- Personalized learning
- Early intervention
- Curriculum improvement
- Learner monitoring

---

# Learner Segmentation using K-Means Clustering

## Introduction

Educational populations are diverse.

Different learners demonstrate different:

- Learning styles
- Engagement patterns
- Skill profiles

K-Means Clustering was implemented to identify groups of learners with similar characteristics.

---

## Features Used

The clustering model utilized:

- Skill Score
- Assessment Score
- Learning Hours
- Engagement Score
- Assignment Completion Rate
- Login Frequency
- Learning Efficiency

These variables collectively represent educational performance and behavior.

---

## Determining Optimal Clusters

The Elbow Method was used to determine the optimal number of clusters.

Results indicated:

### Optimal Clusters = 3

The resulting clusters naturally correspond to:

1. Beginner Learners
2. Intermediate Learners
3. Advanced Learners

---

## Cluster Visualization

<div align="center">
<img src="cluster_visualization.png" width="850">
</div>

---

## PCA-Based Interpretation

Principal Component Analysis (PCA) was used to reduce dimensionality and visualize learner groups.

The visualization demonstrates clear separation among clusters, indicating successful learner segmentation.

---

# Cluster Profile Analysis

## Cluster 0 – Beginner Learners

Characteristics:

- Lower proficiency
- Lower engagement
- Larger skill gaps

Challenges:

- Weak foundations
- Lower confidence
- Increased support requirements

Recommendations:

- Foundational courses
- Additional mentoring
- Frequent assessments

---

## Cluster 1 – Intermediate Learners

Characteristics:

- Moderate proficiency
- Stable engagement
- Consistent learning progress

Challenges:

- Learning plateau
- Need for specialization

Recommendations:

- Project-based learning
- Industry case studies
- Advanced coursework

---

## Cluster 2 – Advanced Learners

Characteristics:

- High proficiency
- Strong engagement
- Excellent performance

Challenges:

- Need for greater challenge
- Specialization decisions

Recommendations:

- Research projects
- Leadership opportunities
- Advanced certifications

---

# Correlation Analysis

## Objective

Correlation analysis evaluates relationships among educational variables.

The goal is to identify factors influencing learner success.

---

## Correlation Matrix

<div align="center">
<img src="correlation_matrix.png" width="850">
</div>

---

## Key Findings

### Assessment Score and Skill Score

Strong positive relationship.

Educational Interpretation:

Students performing well in assessments typically demonstrate stronger proficiency.

---

### Engagement and Performance

Higher engagement generally corresponds with stronger outcomes.

Benefits include:

- Better retention
- Higher proficiency
- Improved consistency

---

### Learning Hours and Success

Learning effort contributes positively to performance.

However, quality of study remains equally important.

This observation supports the importance of Learning Efficiency.

---

## Educational Significance

Correlation analysis provides valuable insights regarding:

- Performance drivers
- Educational effectiveness
- Intervention planning
- Curriculum improvement

---

# Summary of Part 2

The Exploratory Data Analysis phase revealed important educational patterns regarding:

- Skill proficiency
- Learning deficiencies
- Learner groups
- Performance drivers

These findings establish a strong foundation for predictive modeling, recommendation generation, and educational decision support.

# Association Rule Mining

## Introduction

While clustering identifies groups of learners, Association Rule Mining identifies relationships among skills.

The objective is to discover:

- Frequently learned skills
- Skill dependencies
- Learning pathways
- Educational relationships

Association Rule Mining helps educational institutions understand how learners progress through different competencies and which skills are commonly acquired together.

---

## Why Association Rule Mining?

Educational datasets contain hidden relationships that traditional analysis often fails to identify.

Examples:

- Python → Machine Learning
- Statistics → Data Science
- SQL → Data Analytics

Understanding these relationships helps create better learning pathways and recommendation systems.

---

## Apriori Algorithm

The Apriori Algorithm was implemented to discover frequent skill combinations.

The process involves:

1. Identifying frequent skill itemsets.
2. Calculating support.
3. Generating association rules.
4. Evaluating confidence and lift.

---

## Support

Support measures how frequently a skill combination appears within the dataset.

High support indicates:

- Common learning patterns
- Frequently occurring educational pathways
- Strong curriculum relevance

---

## Confidence

Confidence measures the reliability of a rule.

High confidence suggests:

- Strong educational relationships
- Predictable skill progression

---

## Lift

Lift evaluates relationship strength.

Interpretation:

- Lift > 1 = Positive relationship
- Lift = 1 = Independent relationship
- Lift < 1 = Negative relationship

High-lift rules provide the most valuable educational insights.

---

## Example Rules

### Python → Machine Learning

Educational Interpretation:

Python serves as a foundational programming language for Machine Learning.

---

### Statistics → Machine Learning

Educational Interpretation:

Statistical knowledge supports understanding of machine learning concepts.

---

### SQL → Data Analytics

Educational Interpretation:

Database management skills frequently precede analytical skill development.

---

## Educational Benefits

Association Rule Mining supports:

- Curriculum design
- Course sequencing
- Learning pathway development
- Personalized recommendations

---

# Future Skill Prediction

## Introduction

Predictive analytics enables institutions to forecast future learner performance.

This capability allows:

- Early intervention
- Better planning
- Personalized learning
- Improved educational outcomes

The objective is to predict future Skill Scores using historical learner behavior.

---

## Model Selection

Random Forest Regression was selected because:

- Handles nonlinear relationships
- Reduces overfitting
- Supports feature importance analysis
- Produces strong predictive performance

---

## Features Used

Input Variables:

- Assessment Score
- Learning Hours
- Assignment Completion Rate
- Course Completion Percentage
- Login Frequency
- Engagement Score
- Learning Efficiency

Target Variable:

- Skill Score

---

## Prediction Visualization

<div align="center">
<img src="future_skill_prediction.png" width="850">
</div>

---

## Interpretation

The graph compares actual and predicted proficiency values.

Strong alignment indicates:

- Reliable forecasting
- Effective pattern recognition
- High predictive capability

These results demonstrate that learner behavior provides valuable information regarding future educational outcomes.

---

## Model Evaluation

### Mean Absolute Error (MAE)

Measures average prediction error.

Lower values indicate stronger performance.

---

### Mean Squared Error (MSE)

Measures squared prediction error.

Useful for evaluating stability.

---

### R² Score

Measures explained variance.

Higher values indicate stronger predictive power.

---

# Feature Importance Analysis

## Introduction

Feature importance identifies variables that contribute most significantly to educational success.

Understanding these factors supports:

- Educational planning
- Intervention strategies
- Personalized learning

---

## Important Predictors

### Assessment Score

Strongest indicator of future proficiency.

Educational significance:

Reflects conceptual understanding and learning achievement.

---

### Engagement Score

Measures participation and involvement.

Educational significance:

Engaged learners generally perform better.

---

### Learning Hours

Represents effort invested in learning.

Educational significance:

Higher effort often supports stronger outcomes.

---

### Assignment Completion Rate

Represents consistency and discipline.

Educational significance:

Regular practice improves retention and proficiency.

---

### Learning Efficiency

Measures outcomes relative to effort.

Educational significance:

Identifies productive learning behavior.

---

# Personalized Recommendation Engine

## Introduction

The Recommendation Engine generates customized learning pathways based on learner characteristics.

Traditional systems often provide identical content to all students.

This project introduces adaptive recommendations tailored to learner needs.

---

## Recommendation Dashboard

<div align="center">
<img src="recommendation_dashboard.png" width="850">
</div>

---

# Recommendations for Beginner Learners

## Characteristics

- Lower proficiency
- Lower engagement
- Larger skill gaps

---

## Recommended Skills

- Communication
- Problem Solving
- Excel
- Python

---

## Learning Strategy

- Structured learning plans
- Guided practice
- Frequent assessments
- Continuous mentoring

---

# Recommendations for Intermediate Learners

## Characteristics

- Moderate proficiency
- Stable engagement
- Consistent progress

---

## Recommended Skills

- SQL
- Statistics
- Power BI
- Machine Learning

---

## Learning Strategy

- Project-based learning
- Industry case studies
- Specialized coursework

---

# Recommendations for Advanced Learners

## Characteristics

- High proficiency
- Strong engagement
- Excellent performance

---

## Recommended Skills

- Deep Learning
- Cloud Computing
- Data Engineering
- Cybersecurity

---

## Learning Strategy

- Research projects
- Innovation challenges
- Industry certifications
- Leadership opportunities

---

# Deployment Strategy

## Objective

A machine learning solution must be deployable in real-world educational environments.

The proposed architecture supports scalability, reliability, and maintainability.

---

## System Architecture

Student Data

↓

Data Collection

↓

Preprocessing

↓

Feature Engineering

↓

K-Means Clustering

↓

Association Rule Mining

↓

Random Forest Prediction

↓

Recommendation Engine

↓

Dashboard

↓

Educational Decision Support

---

## Technology Stack

### Backend

- Python
- FastAPI

### Machine Learning

- Scikit-Learn
- MLxtend

### Database

- PostgreSQL

### Dashboard

- Streamlit
- Power BI

### Cloud

- AWS
- Microsoft Azure

---

# Scalability Considerations

## Automated Retraining

Learner behavior evolves over time.

Models should be retrained regularly.

Recommended schedules:

- Weekly
- Monthly

depending on data volume.

---

## Data Drift Monitoring

Educational environments change continuously.

Monitoring ensures:

- Model relevance
- Sustained accuracy
- Reliable recommendations

---

## Real-Time Recommendations

Future implementations should provide:

- Instant recommendations
- Immediate intervention support
- Adaptive learning experiences

---

## Enterprise Readiness

The architecture supports:

- Multiple institutions
- Large learner populations
- Cloud deployment
- Secure access control

---

# Business Recommendations

Based on project findings, several recommendations are proposed.

## Recommendation 1

Implement adaptive learning pathways.

---

## Recommendation 2

Prioritize intervention for learners with large skill gaps.

---

## Recommendation 3

Utilize predictive analytics for early risk detection.

---

## Recommendation 4

Continuously monitor learner engagement.

---

## Recommendation 5

Expand recommendation systems across educational programs.

---

## Recommendation 6

Support advanced learners through specialization opportunities.

---

# Conclusion

This project successfully developed an AI-driven framework for Skill Gap Analysis and Learner Segmentation.

The integration of:

- K-Means Clustering
- Association Rule Mining
- Random Forest Regression

demonstrates the value of machine learning in educational environments.

Key achievements include:

- Identification of learning deficiencies
- Discovery of learner groups
- Prediction of future proficiency
- Generation of personalized recommendations

The proposed framework enables educational institutions to move beyond traditional approaches and adopt data-driven, learner-centered strategies.

Through predictive analytics, intelligent recommendations, and scalable deployment architecture, the system provides a strong foundation for future educational innovation and continuous learner development.