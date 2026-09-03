# Workflow Syntax

## Download
* install package:
> brew install pyenv

* setup shell:
> echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
> echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
> echo 'eval "$(pyenv init -)"' >> ~/.zshrc
> source ~/.zshrc

* check:
> pyenv --version

* update packages
> brew upgrade pyenv

## Quản lý python version
* install python version
> pyenv install --list
> pyenv install <python-version>
> pyenv uninstall <python-version>

* versions đã tải
> pyenv versions
> pyenv version (đang được sử dụng)

* set global version
> pyenv global
> pyenv global <python-version>

* set local version
> pyenv local
> pyenv local <python-version>

* current shell
> pyenv shell 
> pyenv shell <python-version>
(set up cho terminal shell "hiện tại" 
=> tắt mở lại thì quay lại phiên bản local)

* python đang chạy
> python --version
> which python
> which pip
> pip --version

> pyenv which python

* using pip
> python -m pip install --upgrade pip
> python -m pip install <package>
> pip install --upgrade pip
> pip install <package>

## Virtual environment (pyenv + env)
* set up local version
> pyenv versions
> pyenv local <python-version>

* create virtual environment
> python -m venv .venv

* activate
> source .venv/bin/activate

* check python version
> which python
> python --version
> which pip

* upgrade pip
> pip install --upgrade pip

* (optional) download proj's packages
> pip install -r requirements.txt

* install necessary packages
> pip install <package1> <package1> ...
ex: pip install numpy pandas

* packages list
> pip list
> pip show <package>

* freeze dependencies
> pip freeze > requirements.txt

* turn off virtual env
> deactivate

* xoá hoàn toàn virtual env 
> rm -rf .venv
(dùng khi cần reset env)

## 