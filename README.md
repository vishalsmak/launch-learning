

# launch-learning


### 🧑‍💻 Steps:

1. Open terminal and navigate to your project directory.

   **Case (a): Setting up in _Development_ environment** 
   
      If you are setting up the project inside **development** environment, use:

      ```
         source project_setup.sh --install --install-dev
      ```

      Incase you are working behind a proxy, use the following command instead:
         
      ```
         source project_setup.sh --install --install-dev --use-proxy
      ```
   

   **Case (b): If you are setting up the project in _production_ environment**, 
   
      If you are setting up the project inside **production** environment, you may only require base packages to be installaed, use:

      ```
         source project_setup.sh --install
      ```

      If you are working behind a proxy, use the following command:
      
      ```
         source project_setup.sh --install --use-proxy
      ```

2. If you are setting up the project first time using this template, then you should replace contents of the README.md with the name of your project:

   ```
   source project_setup.sh --clear-readme
   ``` 
   
   ***Use this command only once in the development environment. DO NOT run this once you write your own readme. Also, do not run this in production environment.***



#### 📝 Important Note 

*  For any other package installation apart from the listed packages in `Pipfile` use `pipenv` as follows:

   ```
   pipenv install package_name
   ```

   By default, `pipenv` loads all the `.env` variables, therefore you need to unset the proxy first if you are not behind proxy.

   Use the following command:

   ```
   source project_setup.sh --unset-proxy
   ```
   You should then be able to install packages using pipenv as stated above.

*  During package installation, the packages are downloaded and cached. This consumes a lot of disk, hence you should clear pip and pipenv cache from time to time. Use the following command:

   ```
   source project_setup.sh --remove-cache
   ``` 


*  ✅ To ensure a conflict-free environment setup, it is strongly recommended to always run the `project_setup.sh` script to create a virtual environment for your project.

*  ❗You should run the script **ONLY** using the `source` command to ensure that the virtual environment `.venv` is automatically activated at the end of setup in the current shell session.
