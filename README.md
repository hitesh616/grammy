# grammy

### To host this application you need to install some packges and need to configure database mysql database on instance 

1. you need python install on machin, install python by following command 
     sudo apt-get update
     sudo apt-get install python3
     
2. create python vritual environment
     sudo apt install python3-venv
     python3 -m venv .venv
   activate python virtual env by  source .venv/bin/activate

3. Install flask
    pip install flask 

4. configure Mysql on machine
     1. install Mysql on machine
         sudo apt install mysql-server
     2. check status of mysql service by
          sudo systemctl status mysql.servic
     3. Install mysql connector with python by
          pip3 install mysql-connector-python
     4.  create user name grammy in mysql and password of that user should be grammy do this by following command
           ''' CREATE USER 'grammy'@'localhost' IDENTIFIED BY 'grammy'; '''
     5. grant all permission to grammy user
         GRANT ALL PRIVILEGES ON *.* TO 'grammy'@'localhost' WITH GRANT OPTION;
     6. create databse name 'grammy' in mysql
          CREATE DATABASE grammy;

yes now you can run flask app by command "python3 main.py"
