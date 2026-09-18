---
layout: post
title: setting up jupyter notebook
subtitle: ""
date: 2026-09-15
tags: networks-past
---

James helped me set up a Jupyter Notebook on my droplet.

First I tried:

```sudo pip install jupyter```

Which showed:

![story](/i-am-in-itp-sometimes/assets/images/error.jpg)

So James helped me set up a virtual environment.

First I had to download the python3-venv package:

```sudo apt install python3.12-venv```

Then I ran:

```python3 -m venv pythonenv```

```pythonenv``` is the name of my virtual environment

After that we did:

 ```source pythonenv```

So we are on the virtual environment.

And within the virtual environment, we did:

 ```pip install jupyter```

But it turned out that this wouldn't run the Jupyter Notebook locally. It would be running somewhere else, though.

So we did something called 'tunnelling', which I don't quite get yet. Then we added a new rule because '8888' is where Jupyter Notebook runs:

```sudo ufw allow 8888/tcp```

Then, I had to logout from my instance, and we started referencing: 

[https://www.digitalocean.com/community/tutorials/how-to-set-up-jupyter-notebook-for-python-3](https://www.digitalocean.com/community/tutorials/how-to-set-up-jupyter-notebook-for-python-3)

```ssh -L 8888:localhost:8888 shlokamohanty@161.35.107.157```

which takes you into your droplet.

Then to access virtual environment, I had to:

 ```source pythonenv/bin/activate```

Then within my virtual environment to look at the jupyter notebook server, we had to:

 ```jupyter server list```

And on my browser, I can then just copy and paste the link to a running server:

 ```http://localhost:8888/?token=d109836562d2cded474f1165f578b7f5fd28f9c055cf7a7c```

This was the one that was running then.