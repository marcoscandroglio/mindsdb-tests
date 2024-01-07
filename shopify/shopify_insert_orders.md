# Welcome to the MindsDB Manual QA Testing for Reddit Handler

> **Please submit your PR in the following format after the underline below `Results` section. Don't forget to add an underline after adding your changes i.e., at the end of your `Results` section.**


## Creating Reddit App

**1. Creating Reddit App**

<img width="875" alt="reddit_2.png" src="https://github.com/marcoscandroglio/mindsdb-tests/blob/cb2a5e42446396e970495c929ffaf94321c085de/reddit/images/reddit_2.png">

## Testing Reddit Handler

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


### Results

Drop a remark based on your observation.
- [ ] Works Great 💚 (This means that all the steps were executed successfully and the expected outputs were returned.)
- [X] There's a Bug 🪲 [Issue Title](URL To the Issue you created) ( This means you encountered a Bug. Please open an issue with all the relevant details with the Bug Issue Template)

---
