## UFW

### Примеры:

```
ufw enable
ufw app list
ufw allow OpenSSH
sudo vi /etc/default/ufw
sudo ufw app info 'Apache'
sudo ufw status numbered
sudo ufw delete 1
```
```
$ sudo ufw allow http [By service name]
$ sudo ufw allow 80/tcp [By port number]
$ sudo ufw allow 'Apache' [By application profile]
```
```
sudo ufw allow 5000:5003/tcp
sudo ufw allow 5000:5003/udp
```

#### Если вы хотите разрешить соединения на всех портах с определенного IP-адреса 192.168.56.1, вам необходимо указать этот IP-адрес следующим образом:
```
sudo ufw allow from 192.168.56.1
```
```
$ sudo ufw allow from 192.168.56.1 to any port 22
```
