# Mictec_Django

## Set-up

- Ensure that you have git installed into your machine, The link for downloading git is [Git Download](https://git-scm.com/download/win)

- If you dont have a github account, Kindly create one. Open this link in a new tab and create your account [GitHub Signup](https://github.com/join)

- You can learn the basics of git from this tutorial just one hour [free code camp git tutorial](https://www.youtube.com/watch?v=RGOj5yH7evk&t=7s)

- The next thing is to ensure that you have Python and Anaconda into your machine, You can download Python via [Python Download](https://www.python.org/ftp/python/3.9.6/python-3.9.6-amd64.exe) and then do the installations. For anaconda terminal the download link is [Anaconda Download](https://www.anaconda.com/download/#windows), Download it and do the installations.

- The next step is that we will need an editor where we will write our codes, You can choose one of this; sublime text, Atom and VS Code. The link for downloading sublime text is [Sublime Text Download](https://download.sublimetext.com/Sublime%20Text%20Build%203211%20x64%20Setup.exe), For Atom is [Atom](https://atom.io/download/windows_x64) and for VS Code is [VS Code Download](https://code.visualstudio.com/download)

- Now we are good to get our hands dirty with the framework for perfectionist:+1: :+1: :+1:

## Getting Started

- After Doing all the above installations, Go to your windows search bar and search for anaconda and open it. Also you can confirm if you have python installed by typing **python --version** on the anaconda terminal.

- The next step is to download the virtual environment, It is always important to create an environment where you will store all the dependencies required by your project. There are two packages that i usually use for this case; virtualenv wrapper and the virtualenv. For our project we will use the virtualenv, though you can still learn how to use the virtualenv wrapper and use it. To install the virtualenv type **_pip install virtualenv-win_**. After the installation has taken place, lets create a folder where we will store our projects, type **_mkdir Mictec_** then cd into that directory by typing **_cd Mictec_** on your terminal.

> NB: You ll need to pay attention to the spellings of the folder you have created and the folder you want to cd to.

- Let us now create a folder where we will house our project and the environment that we will create. To do this we ll do as we have done above **_mkdir BlogEnv_** and then we ll cd into that folder by doing **_cd BlogEnv_**.
  > Now you should be an expert in that.
- Now lets create our environment by typing the following command into the terminal **_python -m venv BlogEnv_** where the BlogEnv is the name of our environment. To activate our environment we will type **_BlogEnv/Scripts/activate_** into the terminal. You should see the name of BlogEnv behind the word Base on your terminal.

- if you are using atom you can open your project folder on the editor by typing **_atom ._** and for VS Code you can type **code .** for sublime you can type **_subl ._**. If any of that does not work, "Physically go to your local disk" and open the folder Users, then the folder named User or has your name, Scroll down and open the first folder that you created i.e The **Mictec folder\***, Now you should see the folder named **BlogEnv**, Slowly drag and drop it :shipit: to your prefered editor.

- The next step is to now install django, Simply type **_pip install django_** in your terminal.

## Creating our Django Project

- After we have installed Django, starting the project should now be a childs play. To start the project simply type **_django-admin startproject src_** Where src is the name of the project that you would want to create, It can be an E-Commerce Project, a blog, a todolist, space-z, etc.

> On your editor you should see that some additional files have been added

- I want you to cd into the project that you have created above for my case i will **_cd src_**

- To run our project, type **_python manage.py runserver_** on your terminal you should see something amazing. Copy paste the address that you see [Local Host](http://127.0.0.1:8000/) http://127.0.0.1:8000/ and paste it on your browser's url, You should see a congratulations message telling you that you have run django successfully.

> Now that is not magic, it's your talent and your hard work

- Now get back to your terminal and you should see an error message that reads;

  > You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s)

- To do away with this error message just type **_python manage.py migrate_** and then rerun your local server by using our usual command **_python manage.py runserver_**

- You can further access the admin panel by adding /admin to your url it should be something like ***http://127.0.0.1:8000/admin***. You should now be able to see a django admin login page. But you need to create a user that can be able to login. To do this type **_python manage.py createsuperuser_** it should prompt you to input a username, email and password and confirmation password.

- After you have done this rerun the server with the same command **_python manage.py runserver_** go to your admin url ***http://127.0.0.1:8000*** in your browser.

- You should now be able to login using the credentials that you have used in registering the new superuser on the terminal.

- After you have logged in you will be meet a nice looking user panel, with the group(s) and Users tabs on the left side. Now i want you to enjoy yourself by creating new users and new groups.

> Now Repeat the whole process for how many times? Let's just say 1000 times and we ll be looking at the next [Jeff Dean](https://en.wikipedia.org/wiki/Jeff_Dean). In the next class we will create our first application and do something more constractive. Well, I hope you enjoyed that.

> Happy Coding!!!

# Lesson II

- After our last class i can confidently state that, most of you now have the capabilities of creating a new project, running the migrations, creating a superuser.
- Additionally most of you now have a clear knowledge of what the settings.py does, what the urls.py is for and so on....
- Probably, most of you have even created tonnes of these projects with the previous instructions and are even wondering what next after this :sunglasses::sunglasses::sunglasses:

> Before we go on just remember that this is a marathon and not a sprint, **_"Pasos cortos vision larga"_** which means **_Short Steps Long Vision_**. Thus, i would like to encourage you to continue creating at least 4 projects a day using the instructions from the previous class.

- In today's lesson we will start by configuring our **_settings.py_**, just adding some basic codes to it. So go to your settings.py and right at the top of the **_from pathlib import path_**, import the os simply by typing this line of code;
  ```
  import os
  ```
- The other line of code in the settings.py that i would like you to alter with it is the **_ALLOWED_HOSTS=[]_** which usually helps us indicate the hosting platform that we would like to host our project in, but to do away with that i would like our project to be hosted by any hosting company thus your code should go as follows;

```
ALLOWED_HOSTS = ["*"]
```
