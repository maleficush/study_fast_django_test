study_fast_aws_backends

1. user@AL01978827 study_fast_aws_backends % python3 -m venv venv
2. user@AL01978827 study_fast_aws_backends % source venv/bin/activate
3. (venv) user@AL01978827 study_fast_aws_backends % python3 -m pip install --upgrade pip

4. (venv) user@AL01978827 study_fast_aws_backends % source ~/.bash_profile
#
export BREW_HOME=/opt/homebrew/bin
export MYSQL_HOME=/opt/homebrew/bin/mysql/bin
export GRADLE_HOME=/opt/homebrew/Cellar/gradle/7.3.3
export PATH=${PATH}:$BREW_HOME:$MYSQL_HOME:$GRADLE_HOME/bin
#

5. (venv) user@AL01978827 study_fast_aws_backends % pip install -r requirements.txt
6. (venv) user@AL01978827 study_fast_aws_backends % python3 manage.py runserver

7. localhost:8000/order/order


