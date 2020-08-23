
# cdk-python-example

## Bucket example

### Needed

#### - Install NVM
```sh
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
$ source ~/.bashrc
$ nvm list-remote
$ nvm install v13.7.0
```
#### - Install CDK
```sh
$ npm install -g aws-cdk
```

#### - Install venv
```sh
$ apt install python3-pip
$ apt install python3-venv
$ pip3 install virtualenv
$ python3 -m venv .env
```

### Init tools

#### - Init App CDK
```sh
$ mkdir app
$ cd app/
$ cdk init app --language python
```

#### - Init venv
```sh
$ source .env/bin/activate
```

### Start project

#### - install dependencies
```sh
$ pip install -r requirements.txt
$ pip install aws-cdk.aws-s3
```

#### - Write dependencies on requirements
```sh
$ pip freeze
```

#### - Write import bucket code on app/app_stack.py
```python
from aws_cdk import (
    aws_s3 as s3,
    core
)
```

#### - Write bucket code resource on app/app_stack.py
```python
bucket = s3.Bucket(self, 
    "MyFirstBucket", 
    versioned=True,)
```

### Publishing 

#### - Synth CDK with AWS Cloudformation
```sh
$ cdk synth
```

#### - Deploy CDK App
```sh
$ cdk deploy
```

#### - Destroy CDK App
```sh
$ cdk destroy
```

## Useful commands

 * `cdk ls`          list all stacks in the app
 * `cdk synth`       emits the synthesized CloudFormation template
 * `cdk deploy`      deploy this stack to your default AWS account/region
 * `cdk diff`        compare deployed stack with current state
 * `cdk docs`        open CDK documentation

To add additional dependencies, for example other CDK libraries, just add
them to your `setup.py` file and rerun the `pip install -r requirements.txt`
command.

Enjoy!
