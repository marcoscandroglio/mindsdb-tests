# Welcome to the MindsDB Manual QA Testing for Reddit Handler

> **Please submit your PR in the following format after the underline below `Results` section. Don't forget to add an underline after adding your changes i.e., at the end of your `Results` section.**


## Testing Reddit Handler with [Predictive Maintenance](https://www.kaggle.com/datasets/tolgadincer/predictive-maintenance?select=train.csv)

**1. Testing CREATE DATABASE**

```
CREATE DATABASE my_reddit
WITH 
    ENGINE = 'reddit',
    PARAMETERS = {
     "client_id": "-pDrSRZ5WB8neV_2aN47FA",
     "client_secret": "q6oLrIoeG-YvgGuMCc8HE4pnm3LjeQ",
     "user_agent": "mindsdb_test"
    };

```
<img width="875" alt="mindsdb_cloud_1.png" src="https://github.com/marcoscandroglio/mindsdb-tests/blob/94db3928548e3ed4e3081fc130f228c5887f9477/reddit/images/mindsdb_cloud_1.png">

**2. Testing CREATE PREDICTOR**

```
CREATE PREDICTOR mindsdb.machine_failure_rate_predicotr
FROM machine_failure                     
(SELECT * FROM machine_train LIMIT 10000)  
PREDICT Machine_failure;    
```

![je3exwn7nbdot9l1hs66](https://user-images.githubusercontent.com/26898623/195608656-26b092ab-7f4a-4bb0-81ba-1cf7d673ce86.jpg)


**3. Testing SELECT FROM PREDICTOR**

```
SELECT Machine_failure
FROM mindsdb.machine_failure_rate_predictor
WHERE torque =40;
```

![eocx8ayd6p036b6sfh6u](https://user-images.githubusercontent.com/26898623/195609435-883ce74e-021f-423b-85cf-158fc0a60b6d.jpg)


### Results

Drop a remark based on your observation.
- [X] Works Great 💚 (This means that all the steps were executed successfully and the expected outputs were returned.)
- [ ] There's a Bug 🪲 [Issue Title](URL To the Issue you created) ( This means you encountered a Bug. Please open an issue with all the relevant details with the Bug Issue Template)

---
