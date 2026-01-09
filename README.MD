```bash
pyenv install 3.9.18
```

# setting

```bash
pyenv local qv-py39
```

```bash
pyenv activate qv-py39
pip install --upgrade pip
pip install jupyter ipykernel
```

```bash
python -m ipykernel install \
  --user \
  --name qv-py39 \
  --display-name "Python (qv-py39)"
```

# select kernal

![사진1](.source/images/1.png)

- select Another Kernel... 선택

![사진2](.source/images/2.png)

- jupyer kernal... 선택 

![사진3](.source/images/3.png)

- 앞서 설정해둔 qv-py39 등의 가상환경 선택