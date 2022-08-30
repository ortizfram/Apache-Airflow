# Apache-Airflow
data pipeline management framework Airflow and how it can help us solve the problem of the traditional ETL 

![image](https://user-images.githubusercontent.com/51888893/187445687-5718c0d6-c551-4667-b55e-bbb4ed8784ff.png)

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

### 📗 Airflow DAG
![image](https://user-images.githubusercontent.com/51888893/187300937-2714ac1c-6a21-4733-b233-e1e4455f17b5.png)

## 🔶  Set up airflow environment with docker
[Docker & DockerCompose](https://docs.docker.com/desktop/install/windows-install/)

![image](https://user-images.githubusercontent.com/51888893/187445491-7aacc201-a41f-4a52-905a-22eea4a20607.png)

allows you to run many containers simultaneously

- `container are lightweight` no need of  of hypervisor
- you can run more container than if tou were using virtual machine
- 
**Beneficts:**

  - no more taks-managing/manteining dependencies, deployment
  - easy to share & deploy different version & environments
  - keep track through github tags & releases 
  - ease of deployment from testing to production environment  
