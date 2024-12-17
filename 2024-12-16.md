
비밀번호 변경 : passwd 계정명

[apt-get 업데이트]
apt-get update -y

apt-get upgrade -y ???

[sudo]
apt-get install sudo

[vim]
apt-get install vim

[계정 생성]
useradd 계정명

[docker 의존성 패키지 설치]
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y

[도커 GPG 키 추가]
curl -fsSL <https://download.docker.com/linux/ubuntu/gpg> | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

[도커 레포지토리 설정]
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

[도커 설치]
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io

[도커 시작 및 활성화]
sudo systemctl start docker
sudo systemctl enable docker

[도커 상태 확인]
sudo systemctl status docker

[도커 실행 확인]
sudo docker run hello-world

[도커 컴포즈 다운]
sudo curl -L "<https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-$(uname> -s)-$(uname -m)" -o /usr/local/bin/docker-compose
