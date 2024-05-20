# Final-Capstone-Project

## Project/Goals
My wife works in the field of Human Resources and she was fascinated about what I have learned in my Data Analytics Bootcamp.  I consulted with her asking what she would be interested if the numbers could give deep insight in her line of work.  She suggested to me about employee attrition - the departure of employees from an organization, whether voluntary or involuntary.  Employees can choose to leave in pursuit of better career opportunities, higher pay, better work-life balance, or other personal reasons.  Also, employers can make the decision to lay off employees due to organization restructuring or terminate employees for poor performance or misconduct.

Attrition can have a negative impact on an organization:
- Loss of employees with valuable knowledge and expertise
- Time and resources spent on new employees
- Increased workload on existing employees
- Negative morale and engagement from employee turnover
- Costs to recruit, hire, and onboard new employees
- Temporary dip in work productivity and efficiency
- Disruption of client relationships and trust from loss of established contacts
- Disruption to continuity of service and quality of service
- Delays in ongoing projects and initiatives
- Disruption in team cohesion
- Harm to organization's reputation to attract top talent and promote positive work culture
- Suggestion of organization's underlying financial issues to investors and stakeholders.

However, attrition can provide positive attributes to an organization:
- Result in savings and reduce overhead costs
- Flexibility to add fresh, new, and potential talent
- Let go of underperforming employees
- Opportunities for internal promotions with existing employees
- Search of employees that fit with organization's culture

This is important to Human Resources because it is a metric that provides insight on how well does an organization retain their workforce.  Trends of attrition are defined, measured, and reviewed on the following factors:
- Low Compensation
- Poor Recognition
- Lack of Career Growth
- High Levels of Stress

Inspired by her intrigue and passion, I have downloaded a dataset from Kaggle that contains information about HR Analytics.  I wanted to explore:

1. What does the data on job satisfaction suggest?
2. Does the amount of travel play a factor?
3. Are employees still quitting after a salary increase?
4. Is gender an important element?
5. How long do employees stay before they leave?

## Process

1. Download 'HR_Analytics.csv' from https://www.kaggle.com/datasets/rishikeshkonapure/hr-analytics-prediction.
2. Import 'HR_Analytics.csv' to Jupyter Notebooks for data review and cleaning, if necessary.
3. Based on the dataset, this is an organization that may belong in the field of healthcare or pharmaceuticals.  There is involvement in scientific research and development, as well as sales and marketing of the products being studied and tested.
4. Summary and Explanation of the Data:

   Attrition (Yes or No)
   - This will be the basis to find comparisions influenced by other variables in the dataset.

   Here is information about employees with respect to age, marital status, education, and work experience:
   - Age Groups:
     - 18 to 25
     - 26 to 35
     - 36 to 45
     - 46 to 55
     - Over 55
   - Marital Status:
     - Divorced
     - Married
     - Single
   - Education:
     - 1: High School
     - 2: College
     - 3: Bachelor's
     - 4: Master's
     - 5: Doctorate
   - Education Fields:
     - Life Sciences
     - Medical
     - Marketing
     - Human Resources
     - Technical Degree
     - Other
   - Number of Companies Worked:
     - Average 3
     - Min. 0
     - Max. 9

   Here is the information about the organization's departments and job positions, including responsibilities and importance:
   - Departments:
     - Human Resources
       - Human Resources (1-3)
         - Recruit and onboard new hires
         - Process compensation and benefits
         - Support positive work culture and organizational goals
       - Manager (3-5)
         - Develop job positions and career development programs
         - Oversee payroll processes
         - Handle grievances, conflicts, labor laws, and workplace compliances
     - Research & Development
       - Laboratory Technician (1-3)
         - Test, sample, and analyze products
         - Operate laboratory equipment and record data
         - Support cases in research and development
       - Research Scientist (1-3)
         - Conduct experiments on developing and improving products
         - Plan research, analyze data, and publish findings
         - Support efforts to research and development
       - Healthcare Representative (2-4)
         - Build relationships with healthcare providers
         - Provide product information
         - Support adoption and use of products
       - Manufacturing Director (2-4)
         - Oversee and optimize production processes
         - Ensure manufacturing efficiencies and meet quality assurances
         - Manage production schedules and supervise staff
       - Manager (3-5)
         - Oversee project deadlines, budgets, and deliverables
         - Supervise staff and assign tasks to employees
         - Evaluate performance and resolve technical issues
       - Research Director (3-5)
         - Develop strategy for research and development that align with organizational goals
         - Provide leadership to managers and their teams
         - Collaborate with stakeholders and manage funding, budgets, risks, and execution
     - Sales
       - Sales Representative (1-2)
         - Promote and sell products
         - Understand needs, provide information, and ensure customer satisfaction
         - Support sales and maintain relationships
       - Sales Executive (2-4)
         - Generate revenue and drive business growth through product sales
         - Build relationships with customers, negotiate contracts, and close deals
         - Attend industry events, conferences, and seminars for networking opportunities
       - Manager (3-5)
         - Set sales targets and financial objectives
         - Develop sales strategies, campaigns, promotions, and initiatives for sales team
         - Manage marketing resources to optimize sales efforts

   - Job Levels:
     - 1: Entry-Level
       - Little or no experience
       - Basic tasks with learning and training
     - 2: Associate
       - Some experience and a step higher level of competency than entry-level
       - More complex tasks, perform regular duties, and support senior staff
     - 3: Mid-Level
       - Specialized knowledge and work independently
       - Manage own work and contribute to projects
     - 4: Senior
       - Extensive experience and leadership capabilities
       - Responsible for planning, decision-making, and mentorship
     - 5: Executive
       - Significant responsibility and influence within the organization
       - Involved in organizational strategy, leadership, and vision

   - 'Standard Hours' suggests to be 80 hours per week for all employees
     - A typical work week is between 35 to 40 hours over 5 days, in addition to overtime for accomodating quarterly sales push or meeting deadlines for product research
     - It is applicable to all departments, job positions, and job levels
     - Data validity is needed to:
       - Confirm whether the number of working hours aligns with labor laws and organization's policies
       - Confirm whether this variable has an effect to employee attrition

   Here is the information about 'Job Involvement' - the degree measured on how employees are engaged with their jobs:
     - 1: Low
       - Minimal interest in their work
       - Means to earn a paycheque with little attachment to the job
       - Higher turnover rate, lower productivity, and lower job satisfaction
     - 2: Moderate
       - Basic level of interest in their work
       - Adequate performance and some participation to work-related activities
       - Steady and reasonable job satisfaction, but potential for engagement and productivity
     - 3: High
       - High level of interest and personal significance in their work
       - High performance and activate participation with the organization
       - More productivity, higher job satisfaction, and higher organizational loyalty
     - 4: Very High
       - Deeply engaged and passionate in their work
       - Exceptional performance and strong commitment to the organization
       - High productivity and innovation, but potential to burnout if not managed properly

   Here is the information about the organization's compensation structure:
   - Base Compensation:
     - 'Hourly Rate', 'Daily Rate', and 'Monthly Rate' are not properly measured because the conversion between hourly, daily, and monthly does not make sense.  For example, the most hours worked (49 hours) divide 'Daily Rate' by 'Hourly Rate' exceed 24 hours in a day.  According to Human Resources, not only does the rate include salary, but also, other overhead costs and expenses to keep an employee, such as benefits, social insurance, and pension.  Therefore, the salary rates will be excluded and 'Monthly Income' will be measured as the employee salary.
     - 'Monthly Income' will be the variable used for compensation as the total amount of money that an employee receives in one month from the employer.  Plus, the monthly income is categorized by the following 'Salary Slabs':
         - Up to $5,000
         - $5,001 to $10,000
         - $10,001 to $15,000
         - Over $15,000
   - Other Compensation:
     - 'Percent Salary Hike' is the percentage increase to an employee's salary:
       - Average 15.21%
       - Min. 11%
       - Max. 25%
       - Factors to apply a percent salary hike for employees:
         - Performance
         - Inflation
         - Market Competitiveness
  - Stock Options are a form of compensation for employees to purchase a number of company's shares.  It encourages employees to work productively to boost the company's stock value and stay longer with the company for further benefits to their stock options.
     - Stock Option Levels:
       - 0: None
         - Minimal to no stock options with focus on base salary and other benefits for new employees
       - 1: Basic
         - Moderate stock options for individual contributors with no managerial responsibilities
       - 2: Intermediate
         - Large stock options for managers and leaders with greater contributions and higher responsibilities
       - 3: Advanced
         - Substantial stock options that are heavily incentivized and a part of an employee's compensation package, mainly for top directors and executives

   Here is the information about 'Performance Rating'.  Employees have only received 3 or 4, which will be used to grade as follows:
     - 3: Meets Expectations
     - 4: Exceeds Expectations

   Here is the information about satisfaction scores with respect to the environment, job, relationships, and work-life balance:
   - Range (1 - Very Dissatisfied, 2 - Dissatisfied, 3 - Satisfied, 4 - Very Satisfied):
     - Environment Satisfaction
       - Workspace Safety, Cleaniness, and Comfort
     - Job Satisfaction
       - Work, Contributions, Compensation, and Opportunities
     - Relationship Satisfaction
       - Interpersonal Relationships with Colleagues and Supervisors
     - Work Life Balance
       - Equilibrium Between Work and Personal Life Commitments

   Here is information about 'Business Travel' and the distance between home and work:
     - Non-Travel
       - No travel for work
       - Consistent daily routine and work environment
       - Stable, low stress, better work-life balance
       - Lack of networking opportunities and limited exposure to new environments
     - Travel Rarely
       - Few trips annually, such as conferences, training sessions, and important meetings
       - Building relationships and attend key events
       - Occasional disruption to work-life routine and minor stress related to travel
     - Travel Frequently
       - Multiple trips and continuous travel throught the year
       - High level interactions with clients and stakeholders with networking opportunities and exposure to business practices
       - Frequent disruption to work-life routine and high level of travel-related stress
   - For 'Distance From Home', we will use the imperial metric system:
     - Average 9.22 mi
     - Min. 1 mi
     - Max. 29 mi

   Here is information about the number of years with respect to experience, training, tenure, and promotion:
   - Years:
     - Total Working Years
       - Average 0
       - Min. 0
       - Max. 40
     - Training Times Last Year
       - Average 3
       - Min. 0
       - Max. 6
     - Years At Company
       - Average 7
       - Min. 0
       - Max. 40
     - Years In Current Role:
       - Average 4
       - Min. 0
       - Max. 18
     - Years Since Last Promotion
       - Average 2
       - Min. 0
       - Max. 15
     - Years With Current Manager
       - Average 0
       - Min. 0
       - Max. 17


## Results
Human Resources
- 63 Staff
  - 11 Managers
  - 52 Human Resources
- 12 Employee Attritions (6 Males and 6 Females)
- Average Salary:
  - Manager at 217,064
  - Human Resources at 50,829
- Satisfaction Scores:
  - 5/12 Attritions rate Job Satisfaction with Score 1
  - 10/12 Attritions rate Relationship Satisfaction and Work Life Balance with Scores 3 and 4
- It is concluded that employees are seeking higher compensation with more responsibilities despite good relationships with their direct report while Human Resources Managers occupy the job positions.

Research and Development
- 967 Staff
- 133 Employee Attritions (13.75%)
- Trend of almost half of Lab Technicians quit within the first few years
  - More than half of the employees who quit are described as young, educated, and single male employees aged 35 years and younger
  - They have the last amount of working experience, spent the least amount of time in their job role and report to management, as well as not staying to wait for promotions
  - They can be described as ambitious and aspire for higher compensation, job titles, and responsibilities

Sales
- 450 Staff
- 93 Employee Attritions (20.67%)
- Of the 93 Staff, more than two thirds of Sales Executives have zero stock options.
- Despite those have worked as much as 23 years and earned approximately 90,000 annual salary, the overall compensation package is also important.

## Challenges 

- 

## Future Goals

- 


