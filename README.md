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
