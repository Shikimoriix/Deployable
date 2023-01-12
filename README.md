**How to make any App or Application deployable on a Web based Platform like Koyeb & Render?**

- **Introduction** 
In This Article i am going to show you how can you make any source code deployable on Web based platforms.

- **Problem**
As you guys know we can't deploy simple source code of Telegram Bot on web based platforms like Koyeb & Render.
If your try to deploy these Source codes your Deployment will be unhealthy & will stop after sometime.

- **Reason**
Web based platforms requires your app to listen to external ports like 80 , 22 , 7 , etc.
Because of this many deployment on these platforms fails.

- **Solution**
So to solve this problem we will use a python framework called flask to deploy bots on these platforms.

- **What is Flask?**
Flask is a micro web framework written in Python. It is classified as a microframework because it does not require particular tools or libraries. It has no database abstraction layer, form validation, or any other components where pre-existing third-party libraries provide common functions.

- **Why Flask used in python**
Flask is a lightweight Python web framework that provides useful tools and features for creating web applications in the Python Language. It gives developers flexibility and is an accessible framework for new developers because you can build a web application quickly using only a single Python file.

<hr>

**Steps to Make any source code deployable on Web Based platforms** 👇

**1) Edit your `requirements.txt` file**

```
Flask==2.2.2
gunicorn==20.1.0
aiohttp==3.8.1
```

<details><b>
<summary>For Example</b></summary>

[<img src="https://lh3.googleusercontent.com/-8zC0EpVL2fQ/Y6rt9qsdecI/AAAAAAAAAPE/I_J00EhwXFkYTzTxjaC7_mwe5AG1bXB7QCNcBGAsYHQ/s1600/1672146420019984-0.png?raw=true"/>](https://github.com/ikx7a)

**NOTE** - Add These Dependencies In Your **requirements.txt** File 

</details>

**2) Create a new File Named As `app.py`**

```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'ikx7a'


if __name__ == "__main__":
    app.run()
```

<details><b>
<summary>For Example</b></summary>

[<img src="https://lh3.googleusercontent.com/-SSjoGB2SKhY/Y6rt9HlD-lI/AAAAAAAAAPA/8BfIsEltQeosN6H910NjbZpDbm4y-_6dACNcBGAsYHQ/s1600/1672146416995416-1.png?raw=true"/>](https://github.com/ikx7a)

</details>

**3) Create a new File named as "run cmd.txt"**

*gunicorn app:app & python3* "YOUR-APP-RUN-COMMAND"

```
gunicorn app:app & python3 bot.py
```

<details><b>
<summary>For Example</b></summary>

[<img src="https://lh3.googleusercontent.com/-ejMFZr4Tfqo/Y6rt8d2eVsI/AAAAAAAAAO8/8YniJFb5z2kCZwbZnweCg3iH03BiB5DSQCNcBGAsYHQ/s1600/1672146413900752-2.png?raw=true"/>](https://github.com/ikx7a)

**Here are app is ready to be deployed on any web based platform.**

</details>






















