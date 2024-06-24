### Создание SSH ключа

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### Копирование ключа на удалённый сервер

```
ssh-copy-id -i ~/.ssh/name.pub username@remote_host
```

### Отключение доступа по паролю

```bash
sudo vim /etc/ssh/sshd_config


PasswordAuthentication no
ChallengeResponseAuthentication no
UsePAM no


sudo vim /etc/ssh/sshd_config.d/50-cloud-init.conf

PasswordAuthentication no

```

### Перезапуск службы SSH

```bash
sudo systemctl restart ssh
```
