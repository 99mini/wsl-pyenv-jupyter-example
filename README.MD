# wsl 설치

### Windows PowerShell (관리자)

```bash
wsl --install
```

기본 배포판: Ubuntu 22.04 LTS 권장

설치 후 재부팅 → Ubuntu 실행 → 사용자 계정 생성

# WSL 기본 패키지 업데이트

```bash
sudo apt update && sudo apt upgrade -y
```

### 필수 빌드 패키지 설치 (pyenv 필수)

```bash
sudo apt install -y \
  build-essential \
  curl \
  git \
  libssl-dev \
  zlib1g-dev \
  libbz2-dev \
  libreadline-dev \
  libsqlite3-dev \
  llvm \
  libncursesw5-dev \
  xz-utils \
  tk-dev \
  libxml2-dev \
  libxmlsec1-dev \
  libffi-dev \
  liblzma-dev
```


# pyenv 설치
```bash
curl https://pyenv.run | bash
```

```bash
vim ~/.bashrc
```

```bash
# vim ~/.bashrc
# 아래 내용을 .bashrc 맨 아래에 추가
# i를 누를 후 복사 붙여넣기
# esc -> :wq 엔터

# pyenv
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"

eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

```bash
source ~/.bashrc
```

# Python 3.8 ~ 3.11 설치
```bash
pyenv install 3.8.18
pyenv install 3.9.18
pyenv install 3.10.13
pyenv install 3.11.7
```

```bash
pyenv versions
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