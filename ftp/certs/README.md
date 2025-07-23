# Requerimientos

1. Se necesita un certificado valido para el subdominio de nginx si se espera usar una conexión segura HTTPS. Puede ser wildcard o puede ser específico.

2. SFTP solicita 2 llaves ssh para autorizar las conexiones. NO PONER CONTRASEÑA. Se pueden crear con:

```
ssh-keygen -t ed25519 -f ssh_host_ed25519_key < /dev/null
ssh-keygen -t rsa -b 4096 -f ssh_host_rsa_key < /dev/null
```