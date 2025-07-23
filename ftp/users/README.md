# Requerimientos

1. Debe existir un archivo users.conf que siga el siguiente formato: `user:pass[:e][:uid[:gid[:dir1[,dir2]...]]] ...`

2. Un grupo con nombre cualquiera con `groupadd` que sirva para que el directorio compartido sea de propiedad del usuario root pero de propiedad del grupo.

3. El usuario que ha de poder cargar debe existir en la máquina huesped y debe pertenecer al grupo. La imagen usada simplemente es un proceso que aísla los paquetes, pero ha de tener acceso a los archivos de la máquina real si se quiere persistencia.

3. El directorio `/srv/boveda_data` o cualquiera que sea el que se comparta debe tener permisos de lectura, escritura y de ejecución para el grupo y de lectura y ejecución para los otros, de tal manera que nginx pueda leerlos y servirlos. Se puede usar 777, pero es más inseguro.