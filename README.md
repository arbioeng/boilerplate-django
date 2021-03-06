
# Django Boilerplate

This app is a boilerplate with ready-to-go settings for a new Django app.

## Steps to get started

1. Download this repository to your computer, and unzip it.

2. Create a folder to host the app.

3. Copy in it the contents of the downloaded folder (`boilerplate-django-master`)

4. Open your folder with VS Code.

5. Since the app contains a Pipfile, a virtual shell will be automatically started, otherwise run `pipenv shell` to start one.

6. Install the requirements from `Pipfile` with

    1. `pipenv install`
    2. `pipenv install --dev`

7. Change the name of the app to one of your liking by running

    `python manage.py rename your-desired-app-name`

8. Delete the folder `main`, which contains the now obsolete script used to rename the project.

9. Run (if necessary) `python manage.py collectstatic`.

10. Create a local repository with `git init`. The `.gitignore` file provided is ready to ignore all the commonly ignored files.

11. Settings are divided in the module `settings/environments`. Edit these for the different environments or `settings/components/base.py` for settings common to both development and production.

12. The `.env` file provided (`your-app-name/settings/.env`) should include your environment variables. Change `DJANGO_ENV` to either `development` or `production` for the corresponding settings to load.

13. Add eventual new settings in the following files:

    1. `your-app-name/settings/components/common.py` for settings common to both development and production
    2. `your-app-name/settings/environments/development.py` for settings used during development.
    3. `your-app-name/settings/environments/production.py` for settings used for production.

14. The app includes a handy django toolbar (only available in the development environment) that facilitates debugging.

That's all. Start coding!

## **Note**

If you're using VSCode's debug functionality *and* Pipenv, be aware that there's currently an issue and the request for the creation of the shell and the command to start the debugger are timed badly.

To avoid issues, install all dependencies from the Pipfile with:

`pipenv install`

`pipenv install --dev`

and once the environment has all dependencies installed, momentarily rename your Pipfile (for example adding a dash before the name) so pipenv won't attempt to create a new shell while the debugger is invoked.

Make sure to rename back Pipfile before installing new dependencies for a correct deployment.
