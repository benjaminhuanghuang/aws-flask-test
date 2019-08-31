# aws-flask-test
## Reference
- https://docs.aws.amazon.com/zh_cn/elasticbeanstalk/latest/dg/create-deploy-python-flask.html

## Setup Flask app
Create virtual env for python project
```
  pip install virtualenv
  virtualenv --system-site-packages -p python3 venv3
```
Active the virtual env
```
  . venv3/bin/activate
```
Install Flask
```
  pip install Flask==1.0.2
```
Create app.py


## Deploy to aws
Install EB cli
```
  pip3 install awsebcli
  eb --version
```
Create a .ebingore file to tell Elasktic Beanstalk to ignore some folder or files in project folder, like the virtul env folder.

Create an application env on aws
```
  eb init -p python-3.6 ben-flask-test --region us-west-2
```
This command creates a new application named ben-flask-test and configures your local repository to create environments with the  Python 3.6.

Run eb init again to configure a default keypair so that you can connect to the EC2 instance running your application with SSH:
```
  eb init
```
Create an environment and deploy app
```
  eb create ben-flask-env
```
Open web site
``` 
  eb  open
```



