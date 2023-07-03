# TEAMGANTT WORKLOAD AUTOMATION PROJECT

This is a project I made during my stay as a biomedical engineer intern at Neuroelectrics.

### Origin of the project

TeamGantt is a cloud-based Gantt chart and project planning solution for small, midsize and large enterprises. It offers project collaboration tools such as collaborative Gantt charts, time tracking, file sharing and task-level communication features.

It is a really useful tool for project management but, unfortunately, at the current time, the application-interface does not provide an option to download the project workload filtered by users and projects. This issue was handled in the company by manually putting all active projects on hold and then activating each project one by one to download the workload. Obviously, this was very time-consuming (1.5 hours/week were lost on manually doing the TeamGantt workload download).

Therefore, we decided to solve this issue by communicating with the TeamGantt API (https://api.teamgantt.com/) and automating this download. 

I truly hope this is as useful and time-saving for you as it has been for us!

### Basic information

The code has been developed with Jupyter Notebook, which uses Python. The first part is dedicated to importing the libraries and then it performs the authentication of the TeamGantt API. This is a very important step and you will need to insert your own email and password to get the API key and be able to access TeamGantt API.
Then, we distinguish two codes: "Workload download option A" and "Workload download option B". Basically, they are two versions of the same code that can have the same output result. 

### Workload download option A

In this version of the code, the user can decide the dates when the download will be made. Therefore, the user has to manually enter the start and end date period when they want to download the workload of each project. 
(Note: The workload has been set to be downloaded per day, but this can be changed by modifying the request with the API).

### Workload download option B

This version of the code has been configured to automatically do the download of the workloads (the user does not have to enter any date, the start_date is always today and the end_date is always 1 year after today). These dates can be manually modified if needed. 

### Result

The result of executing option A or option B, has to be an archive in .csv with information in different columns of the project_ID, user_ID, Hours total (spent for each user in that project) and the Date where these hours were done. Depending on the period (start_date and end_date chosen) the dates will be longer or shorter.
