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


----Docker 설치
sudo yum update -y
sudo amazon-linux-extras install docker
sudo service docker start
sudo usermod -a -G docker ec2-user
-- 재접속후
docker info


----Docker 이미지 빌드
docker build -t server_dev/django .
docker run -t -i -p 80:80 hello-world


---IAM 사용자 로그인
aws configure
AKIA33RM24CCJLY67GFC  / QmY3jhBN7LfbrRLXl+Bjjr6ryX87r8HmA08bcH78


----ECR 로그인 
aws ecr get-login --no-include-email --region us-east-1


----ECR repository 생성
aws ecr create-repository --repository-name hello-cli --region us-east-1

url : 815064080516.dkr.ecr.us-east-1.amazonaws.com/hello-cli


---Docker TAG
docker tag server_dev/django 815064080516.dkr.ecr.us-east-1.amazonaws.com/hello-cli


---Docker Push
docker push 815064080516.dkr.ecr.us-east-1.amazonaws.com/hello-cli


---
