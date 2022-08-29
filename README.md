# Apache-Airflow
data pipeline management framework Airflow and how it can help us solve the problem of the traditional ETL 
### 📗 what is it?
 is a platform that lets you build and run and monitor workflows or PipeLines
### 📗 workflow
squence of scheduled tasks triggered by an event

used to handle big data pipelines

![image](https://user-images.githubusercontent.com/51888893/187298696-e8f50bde-7e62-4133-8b54-1fbaad440bd6.png)
### 📗 traditional ETL
-  write `script` to pull data from DB & send to `HDFS` to process

-  schedule script as a `cronjob`

![image](https://user-images.githubusercontent.com/51888893/187299249-834b53a6-6c59-4bb4-95ec-a908554c23d3.png)
### 📗 Problems
- Failures: retry if happends(how many times?,how often?)
- Monitoring: pass or fails (how long does it take?)
- Dependencies: 
     - Data dependencies: upstream data is missing
     - execution dependencies: job2 runs after job 1 is finished
- Scalability: no centralized schedulerbetween diff cron machines
- Deplyment: deploy smt new constantly
- Process historic data: backfill/rerun historical data
