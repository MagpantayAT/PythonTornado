# Setting up Python Tornado
How to setup Python Tornado as backend webserver on Windows. You may also like to check my reference here https://www.youtube.com/watch?v=DQNW9qhl4eA

### Step 1
- Install Anaconda on your computer (https://www.anaconda.com/)
- You may watch (https://youtu.be/-63AWJPAzhM) for installing Anaconda Navigator

### Step 2
- Run Anaconda Navigator then go to `Environment > Search Package > Tornado` then install
- OR
- Run Anaconda Prompt and type in `conda install -c anaconda tornado` (https://anaconda.org/anaconda/tornado)

### Step 3
- Download the sample `sever.py` together with the sample html file

### Step 4
- Open Anaconda Prompt and navigate to the directory where the Python and HTML file located
- then type in `python server.py` to run your server
- in case you encounter `raise NotImplementedError NotImplementedError` just add the following codes:
```
import asyncio
asyncio.set_event_loop_policy(asyncio.WindowsSelectorEventLoopPolicy())
```
(https://www.programmersought.com/article/49705560362/)

### Step 5
- Open a web browser and type `localhost:8881` this will run the `basicRequestHandler` class
- type in `localhost:8881/html` to load the HTML file under `staticRequestHandler` class
- `localhost:8881/isEven?n=[some value]` to run `queryStringRequestHandler` class
- `localhost:8881/resource/[some value]` to run `resourceRequestHandler` class
- `localhost:8881/api` to run `callJSON` class which will return a JSON

