# Projeto-01-BP

## Instruções para Executar o Script Ansible

Este projeto utiliza Ansible para automatizar a instalação do Visual Studio Code. Siga as instruções abaixo para executar o script `ansible-playbook`.

### Pré-requisitos

- Ansible instalado na sua máquina.
- Acesso ao arquivo `install-vscode.yaml`.
- Arquivo de inventário `inventory.ini` configurado corretamente.
- Arquivo `become_pass.yml` com a senha armazenada via Ansible Vault.

### Credenciais

A senha definida no Vault é `redes2025`.

### Passos para criar o arquivo `become_pass.yml` com Ansible Vault

1. Abra o terminal.
2. Navegue até o diretório do projeto:

    ```sh
    cd project-01-bp
    ```

3. Execute o comando abaixo para criar o arquivo [become_pass.yml](http://_vscodecontentref_/1) com a senha criptografada:

    ```sh
    ansible-vault create become_pass.yml
    ```

4. Quando solicitado, insira a senha do Vault: `redes2025`.
5. No editor que abrir, adicione a seguinte linha:

    ```yaml
    ansible_become_pass: 'redes2025'
    ```

6. Salve e feche o editor.

### Passos para editar o arquivo [become_pass.yml](http://_vscodecontentref_/2) existente

1. Abra o terminal.
2. Navegue até o diretório do projeto:

    ```sh
    cd project-01-bp
    ```

3. Execute o comando abaixo para editar o arquivo [become_pass.yml](http://_vscodecontentref_/3):

    ```sh
    ansible-vault edit become_pass.yml
    ```

4. Quando solicitado, insira a senha do Vault: `redes2025`.
5. No editor que abrir, faça as alterações .
necessárias6. Salve e feche o editor.

### Passos para execução

1. Abra o terminal.
2. Navegue até o diretório do projeto:

    ```sh
    cd project-01-bp
    ```

3. Execute o comando Ansible Playbook:

    ```sh
    ansible-playbook install-vscode.yaml -i inventory.ini --ask-vault-pass
    ```

4. Insira a senha do Vault `redes2025` quando solicitado.

### Observações

- Certifique-se de que o arquivo [inventory.ini](http://_vscodecontentref_/4) contém as informações corretas dos hosts.
- O comando `--ask-vault-pass` solicitará a senha do Vault para descriptografar o arquivo [become_pass.yml](http://_vscodecontentref_/5).

### Contato

Para mais informações, questione o seu professor.