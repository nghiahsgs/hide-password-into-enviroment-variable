# hide-password-into-enviroment-variable
hide password into enviroment variable


```python
# windows
# setx VariableName "nghia"
# reset terminal
# echo %VariableName%
import os
name = os.environ.get('VariableName')
print('name',name)
```


```python
# linux
# export NAME=1997
# echo $NAME

# export name="nghiahsgs"
# echo $name

# vi ~/.bash_profile
# source ~/.bash_profile
import os
name = os.environ.get('name')
print('name',name)
```



```python
from email.policy import default
import os
from typing import Optional
from pydantic import BaseSettings

class Settings(BaseSettings):
    name:str
    # setx password "123456"
    # echo %password%
    password:str = os.environ.get('password')
    class Config:
        env_file = os.path.join(os.path.dirname(os.path.realpath(__file__)),'.env')

settings = Settings()

if __name__ =="__main__":
    print(settings.name)
    print(settings.password)
    
```
