# Instruções para usar Ansible

### Editar o ficheiro ***"/etc/ansible/ansible.cfg"*** para alterar ou adicionar algumas configurações.
Descomentar (retirar o caratér ; ou # do inicío da linha) a linha ***host_key_checking=False***.  
Este ficheiro permite fixar todas as configurações do ansible.

### Criar um ficheiro "secrets.yml" para guardar os users e passwords dos ambientes que queremos gerir.
Para criar o ficeiro é usado este comando que nos vai pedir a criação de um password para aceder ao ficheiro que vai ficar encriptado:  
***ansible-vault create group_vars/secrets.yml***  
Para voltar a aceder ao ficheiro usamos o mesmo comando mas com a flag edit em vez de create, antes de abrir, pede a password escolhida na criação do ficheiro:  
***ansible-vault edit group_vars/secrets.yml***

### Criar ficheiros de inventário para guardar listas dos objetos onde queremos atuar.
Os ficheiros de inventário podem ter dois formatos, ini ou yaml.  
Por defeito temos o ficheiro "ini" ***"/etc/ansible/hosts"*** mas podemos criar outros com o formato que preferirmos e onde quisermos.

## Em construção

### Comandos para de playbooks:
#### Comando para verificar a syntax de um playbook.
***ansible-playbook --syntax-check playbook.yml***  
#### Comando para executar um playbook utilizando o inventário hosts.
***ansible-playbook -i hosts playbook.yml***  
#### Comando para executar um playbook utilizando o inventário hosts com as credenciais guardadas no vault.
***ansible-playbook -i hosts playbook.yml --ask-vault-pass***  
#### Comando para executar um playbook com debug.
***ansible-playbook -i hosts playbook.yml --vvv***  
#### Comando para executar um playbook com debug.
***ANSIBLE_DEBUG=1 ansible-playbook -i hosts --ask-vault-pass playbook.yml --vvv***  

###
