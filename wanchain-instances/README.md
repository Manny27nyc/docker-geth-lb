sudo docker build -t wanchain-instance .
sudo docker run -e WS_SECRET='abcdef' -e WS_SERVER='ws://127.0.0.1:3000' -e INSTANCE_NAME="wanchain-instance-$(cat /dev/urandom | tr -dc 'a-zA-Z0-9' | fold -w 8 | head -n 1)" -it -p 8545:8545 -p 30303:30303 -v ./temp_files:/root/.wanchain wanchain-instance



/usr/bin/screen -m -d -S docker docker run -e WS_SECRET='CryptoCurve!@' -e WS_SERVER='ws://18.188.178.152:3000' -e INSTANCE_NAME="wacnhcain-instance-1" -it -p 8545:8545 -p 30303:30303 -v /wanchain:/root/.wanchain andrecronje/docker-geth-lb:wanchain-instance