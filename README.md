# BSI C5 Catalog Project
An Udacity Full Stack Web Developer II Nanodegree project developed by Björn Ziller (First version from august in 2019.

## About
This application provides a cathalog for the common BSI C5 Cloud Requirements with an initial setup of attributes (description, annotations, ext_id) and it provides a user registration and authentication system on the oauth2 base. Third person provider is google, so you will need an google+ account.

### Features
- Google based authentication and authorisation check.
- Full CRUD support using SQLAlchemy and Flask.
- JSON endpoints.

### Project Structure
```
.
├── BSI_C5_project.py
├── client_secrets.json
├── database_setup.py
├── requirements_base.py
├── README.md
├── static
│   └── style.css
└── templates
    ├── newReField.html
    ├── deleteReField.html
    ├── editReField.html
    ├── main.html
    ├── header.html
    ├── login_g.html
    ├── newRequirement.html
    ├── editRequirement.html
    ├── deleteRequirement.html
    ├── reFields.html
    └── refieldCollection.html
```

## Steps to run this project

1. Download and install [Vagrant](https://www.vagrantup.com/downloads.html).

2. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

3. Clone or download the Vagrant VM configuration file to your directory

4. Open the above directory and navigate to the `vagrant/` sub-directory.

5. Open terminal, and type

   ```bash
   vagrant up
   ```

   This will cause Vagrant to download the Ubuntu operating system and install it. This may take quite a while depending on how fast your Internet connection is.

6. After the above command succeeds, connect to the newly created VM:

   ```bash
   vagrant ssh
   ```

8. Type `cd /vagrant/` to navigate to the shared repository.

9. Download or clone this repository, and navigate to it.

11. Install or upgrade Flask:
    ```bash
    sudo python3 -m pip install --upgrade flask
    ```
12. Set up the database:
    ```bash
    python3 database_setup.py
    ```
13. Insert dummy values. **If you don't run this, the application might not run.**
    ```bash
    python3 requirements_base.py
    ```
14. Run this application:
    ```bash
    python3 BSI_C5_Project.py
    ```
15. Open `http://localhost:5000/` in your favourite Web browser, and enjoy.

## Debugging
In case the app doesn't run, make sure to confirm the following points:
- You have run `python3 requirements_base.py` before running the application. This is an essential step.
- The latest version of Flask is installed.
- Python 3.6 is installed. In the vagrant machine, you may find Python 3.5 installed by default.

## Known Issue
In some case, you need to hit enter twice after signing in via google+ to get a redirect to the page.

## Help and Support
In case you run into any trouble, create an issue on GitHub. I will make sure to look into it as soon as possible.
