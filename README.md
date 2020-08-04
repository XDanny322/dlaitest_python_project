# dlaitest_python_project

This is a quick test on creating your own pip package and upload the pypi.

https://pypi.org/project/dlaitest-python-project/

## See
- https://medium.com/@joel.barmettler/how-to-upload-your-python-package-to-pypi-65edc5fe9c56
- https://marthall.github.io/blog/how-to-package-a-python-app/

## How to:

- Register for your account in pypi
- `pip install -U pip setuptools twine`
- Create your program / script
- Package your script: `python setup.py sdist`
- Upload to pypi:
    ``` console
    python setup.py sdist
    twine upload dist/*
    ```

## Example client code

```
import boto3
import json
from dlaitest_python_project import Car

print("HI")

myride = Car("11","ii",6)
myride.accelerate()
print(myride.get_speed())
```