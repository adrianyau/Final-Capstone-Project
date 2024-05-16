# Final-Capstone-Project

## Project/Goals
My wife works in the field of Human Resources and she was fascinated about what I have learned in my Data Analytics Bootcamp.  I consulted with her asking what she would be interested if the numbers could give deep insight in her line of work.  She suggested to me about employee attrition - the departure of employees from an organization, whether voluntary or involuntary.  This is important to Human Resources because it is a metric that provides insight on how well does an organization retain their workforce.  Reasons for attrition are mainly due to:
- Low Compensation
- Poor Recognition
- Lack of Career Growth
- High Levels of Stress

Attrition can have a negative impact on an organization:
- Loss of employees with valuable knowledge and expertise
- Time and resources spent on new employees
- Increased workload on existing employees
- Negative morale and engagement from employee turnover
- Costs to recruit, hire, and onboard new employees
- Temporary dip in work productivity and efficiency
- Disruption of client relationships and trust from loss of established contacts
- Disruption to continuity of service and quality of service
- Delays in ongoing products and initiatives
- Disruption in team cohesion
- Harm organization's reputation to attract top talent and promote positive work culture
- Suggest organization's underlying financial issues to investors and stakeholders.

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
   - This will be the basis to measure attrition influenced by other variables in the dataset.

   Here is information about employees with respect to age, marital status, education, and work:
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

   Here is the information about the organization's departments and job positions, as well as responsibilities and importance:
   - Departments:
     - Human Resources
     - Research & Development
     - Sales
   - Job Roles (with Job Levels):
     - Healthcare Representative (2-4)
       - Build relationships with healthcare providers
       - Provide product information
       - Support adoption and use of organization's products
     - Human Resources (1-3)
       - Recruit, train, and develop employees
       - Handle employee compensation and benefits
       - Maintain positive work culture and support organizational goals
     - Laboratory Technician (1-3)
       - Test and analyze products
       - Prepare samples, operate laboratory equipment, and record data
       - Support projects in research and development
     - Manager (3-5)
       - Oversee teams and departments within the organization
       - Plan, coordinate, and direct activities
       - Ensure efficient operations, manage budgets, and provide leadership
     - Manufacturing Director (2-4)
       - Oversee and optimize production processes
       - Ensure timely manufacturing efficiencies and meet quality assurances
       - Manage production schedules and supervise manufacturing staff
     - Research Director (3-5)
       - Lead research and development projects
       - Set agendas, oversee progresses, and manage reserch teams
       - Innovate new products for the market
     - Research Scientist (1-3)
       - Conduct experiments and investigations to develop new products or improve existing products
       - Plan research, analyze data, and publish findings
       - Support research and development efforts
     - Sales Executive (2-4)
       - Sell organization's products to clients
       - Find sales opportunities, build relationships with clients, negotiate contracts, and close deals
       - Generate revenue and drive business growth
     - Sales Representative (1-2)
       - Promote and sell organization's products
       - Understand needs, provide information, and ensure customer satisfaction
       - Support sales and maintain long-term relationships
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
   
   - Job Involvement (the degree on how employees are engaged with their jobs):
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
     - Hourly Rate
     - Daily Rate
     - Monthly Rate
     - Monthly Income
       - Salary Slab:
         - Up to $5,000
         - $5,001 to $10,000
         - $10,001 to $15,000
         - Over $15,000
   - Other Compensation:
     - Percent Salary Hike
       - Between minimum of 11% to maximum 25%
     - Stock Option Levels:
       - 0: None
       - 1: Basic
       - 2: Intermediate
       - 3: Advanced
   - Standard Hours (80 Hours)
   - Performance Rating:
     - 3: Meets Expectations
     - 4: Exceeds Expectations

   Here are satisfaction scores with respect to the environment, job, relationships, and work-life balance:
   - Range (1 - Very Dissatisfied, 2 - Dissatisfied, 3 - Satisfied, 4 - Very Satisfied):
     - Environment Satisfaction
       - Workspace Safety, Cleaniness, and Comfort
     - Job Satisfaction
       - Tasks and Responsibilities
     - Relationship Satisfaction
       - Interpersonal Relationships with Colleagues and Supervisors
     - Work Life Balance
       - Equilibrium Between Work and Personal Life Commitments

   Here is information about business travel and distance between home and work:
   - Business Travel:
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
   - Distance From Home:
     - Average 9.22
     - Min. 1.00
     - Max. 29.00

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

- 

## Challenges 

- 

## Future Goals

- 


