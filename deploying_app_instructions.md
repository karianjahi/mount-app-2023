# Instructions for rendering an App on the `Render` platform
1. create a folder on **github** and give it an informative name
   - `cascabels_movie_recommeder`
   - Remember how to create a repo in github
   <br><br>
2. create a new virtual environment
    - `conda create -n cascabel-movie-app python=3.10` <br><br>
3. We activate the new environemnt
    - `conda activate cascabel-movie-app` <br><br>
4. Populate the folder with all your app files
    - in this case, we use the files from the encounter. <br><br>
5. Test if the app deploys locally using:
   - `python application.py`
    Note: If you want to kill a port use:
    `fuser -n tcp -k <port>` where <port> is the port number e.g. 5000 <br><br> 
6. Create a `requirements.txt` file. This is the file that instructs the application on which modules are necessary!
    `pip freeze > requirements.txt`<br><br>
7. To render the App in `RENDER`, we need to use a module called `gunicorn`. We have to add it to our `requirements.txt` file <br><br>
8. We now need to got the `Render` platform [here](https://spring-sardine-972.notion.site/Deploying-web-apps-using-Render-477bfc4b4200410294c0e16f8b7ef73a). <br><br>Sign up on Render either using your github account or email address. If you use your email address, you still have to link your github repo to your render account. <br><br>
   * 8.2 Once you create an account and linked your github account: <br><br>
    a. Click on `NEW` on page <br><br>
    b. `Web Service` <br><br>
    c. Copy the link to your github repo that you want to render and paste on `Public Git Repository`<br><br>
    d. Press `Continue`<br><br>
    d1. Under `name` create a name for your repo e.g. cascabels-recommends-movies <br><br>
    d2. Make sure you fill the required fields and pay attention to the root directory where your app is and also the `start command`. If your python launch file is e.g. start_app.py the start command should be
    `gunicorn start_app:app`<br><br>
    In our case our file is `application.py`. The start command therefore is: `gunicorn application:app` <br><br>
    e. Click on `Create Web Service` and wait for the app to deploy <br><br>
    d. Once it successfully deploys, you need to copy the link that has the name of your webservice. This link is what you can share with anyone on the globe (and perhaps beyond). 

    ! DONE!!!
