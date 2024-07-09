# Instruções para usar Ansible

### Criar um ficheiro secrets.yml para guardar os users e passwords dos ambientes que queremos gerir.
Para criar o ficeiro é usado este comando que nos vai pedir a criação de um password para aceder ao ficheiro que vai ficar encriptado:  
***ansible-vault create group_vars/secrets.yml***  
Para voltar a aceder ao ficheiro usamos o mesmo comando mas com a flag edit em vez de create, antes de abrir, pede a password escolhida na criação do ficheiro:  
***ansible-vault edit group_vars/secrets.yml***

### Criar ficheiros de inventário para guardar listas dos objetos onde queremos atuar.
Os ficheiros de inventário podem ter dois formatos, ini ou yaml.  
Por defeito temos o ficheiro "ini" ***/etc/ansible/hosts*** mas podemos criar outros com o formato que preferirmos e onde quisermos.

###
