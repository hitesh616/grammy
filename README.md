# Grammy Application

## Introduction

Welcome to the Grammy application, a feature-rich platform for entertainment. This readme provides a step-by-step guide to help you set up and run the application on your machine.

## Prerequisites

Before hosting the Grammy application, ensure that the following prerequisites are installed on your machine:

1. **Python:**
   - Install Python 3 using the commands:

     ```bash
     sudo apt-get update
     sudo apt-get install python3
     ```

2. **Virtual Environment:**
   - Create a Python virtual environment:

     ```bash
     sudo apt install python3-venv
     python3 -m venv .venv
     ```

   - Activate the virtual environment:

     ```bash
     source .venv/bin/activate
     ```

3. **Flask:**
   - Install Flask:

     ```bash
     pip install flask
     ```

4. **MySQL Database:**
   - Install MySQL:

     ```bash
     sudo apt install mysql-server
     ```

   - Check MySQL service status:

     ```bash
     sudo systemctl status mysql.service
     ```

   - Install MySQL connector for Python:

     ```bash
     pip3 install mysql-connector-python
     ```

   - Configure MySQL:
     - Create a user 'grammy' with the password 'grammy':

       ```sql
       CREATE USER 'grammy'@'localhost' IDENTIFIED BY 'grammy';
       ```

     - Grant all privileges to the 'grammy' user:

       ```sql
       GRANT ALL PRIVILEGES ON *.* TO 'grammy'@'localhost' WITH GRANT OPTION;
       ```

     - Create a database named 'grammy':

       ```sql
       CREATE DATABASE grammy;
       ```

## Running the Application

Now that you have the prerequisites, follow these steps to run the Grammy application:

1. Run the Flask app:

   ```bash
   python3 main.py
