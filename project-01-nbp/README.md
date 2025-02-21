# Project-01-NBP

## Instruções para Executar o Script Ansible

Este projeto utiliza Ansible para automatizar a instalação do Visual Studio Code. Siga as instruções abaixo para executar o script `ansible-playbook`.

### Pré-requisitos

- Ansible instalado na sua máquina.
- Acesso ao arquivo `install-vscode.yaml`.
- Arquivo de inventário `inventory.ini` configurado corretamente.

### Credenciais

O usuário padrão é `redes` e a senha padrão é `redes2025`.

### Passos para Execução

1. Abra o terminal.
2. Navegue até o diretório do projeto:

    ```sh
    cd project-01-nbp
    ```

3. Execute o comando Ansible Playbook:

    ```sh
    ansible-playbook install-vscode.yaml -i inventory.ini --ask-become-pass
    ```

4. Insira a senha de sudo `redes2025` quando solicitado.

### Observações

- Certifique-se de que o arquivo `inventory.ini` contém as informações corretas dos hosts.
- O comando `--ask-become-pass` solicitará a senha de sudo para executar tarefas que requerem privilégios elevados.

### Contato

Para mais informações, questione o seu professor. Project-01-NBP