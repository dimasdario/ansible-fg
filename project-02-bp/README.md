# Project-02-bp

## Descrição
Este projeto utiliza Ansible para gerenciar a configuração de hosts. O objetivo principal é configurar o acesso aos hosts sem a necessidade de senha.

## Passos para Configuração

1. **Executar o Playbook `configure-host.yaml`**
    - Este playbook é responsável por configurar o acesso aos hosts sem a necessidade de senha.
    - Para executá-lo, utilize o comando:
      ```bash
      ansible-playbook configure-host.yaml --ask-vault-pass
      ```

2. **Editar o Arquivo `inventory.ini`**
    - Após a execução do playbook, edite o arquivo `inventory.ini`.
    - Remova a linha contendo `ansible_ssh_pass=redes2025`.
    - A partir de agora, não será mais necessário o uso de senha no arquivo `inventory.ini`.

## Exemplo de Arquivo `inventory.ini` Após Edição
```ini
[hosts]
host1 ansible_host=192.168.1.1 ansible_user=usuario
host2 ansible_host=192.168.1.2 ansible_user=usuario
```

## **Executar o Playbook `install-vscode.yaml`**
  - Este playbook é responsável por instalar o Visual Studio Code nos hosts.
  - Para executá-lo, utilize o comando:
  
      ```bash
      ansible-playbook install-vscode.yaml --ask-vault-pass
      ```
## Conclusão
Seguindo os passos acima, você configurará o acesso aos hosts sem a necessidade de senha, simplificando a gestão dos mesmos com Ansible.
