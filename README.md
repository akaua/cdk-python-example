# cdk-python-example

## Bucket example

### Needed

### - NVM
```sh
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
$ source ~/.bashrc
$ nvm list-remote
$ nvm install v13.7.0
```
### - Install CDK
```sh
$ npm install -g aws-cdk
```

### - Init App CDK
```sh
$ mkdir app
$ cd app/
$ cdk init app --language python
```

### - Install venv
```sh
$ apt install python3-pip
$ apt install python3-venv
$ pip3 install virtualenv
$ python3 -m venv .env
```

### - Init venv
```sh
$ source .env/bin/activate
```

### - install dependencies
```sh
$ pip install -r requirements.txt
$ pip install aws-cdk.aws-s3
```

### - Write dependencies on requirements
```sh
$ pip freeze
```

### - Write dependencies on requirements
```sh
$ pip freeze
```

### - Write import bucket code on app/app_stack.py
```python
from aws_cdk import (
    aws_s3 as s3,
    core
)
```

### - Write bucket code resource on app/app_stack.py
```python
bucket = s3.Bucket(self, 
    "MyFirstBucket", 
    versioned=True,)
```

### - Synth CDK with AWS Cloudformation
```sh
$ cdk synth
```

### - Deploy CDK App
```sh
$ cdk deploy
```

### - Destroy CDK App
```sh
$ cdk destroy
```