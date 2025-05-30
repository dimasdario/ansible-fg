 ```sh
cd Downloads

###install zotero

sudo apt update
sudo apt upgrade
sudo apt install libfuse2
wget -qO- https://raw.githubusercontent.com/retorquere/zotero-deb/master/install.sh | sudo bash
sudo apt update
sudo apt install zotero

###install Mendeley

wget https://static.mendeley.com/bin/desktop/mendeley-reference-manager-2.134.0-x86_64.AppImage
chmod +x mendeley-reference-manager-2.134.0-x86_64.AppImage
./mendeley-reference-manager-2.134.0-x86_64.AppImage --no-sandbox
```

# Repositório de Projetos de Automação com Ansible

Este repositório contém um conjunto de projetos utilizados nas aulas de Ansible, com o objetivo de demonstrar como podemos evoluir um projeto de automação para os laboratórios da faculdade. Este material deve ser usado como consulta para o desenvolvimento do projeto solicitado na disciplina de Elaboração de Projetos II.

## Estrutura do Repositório

O repositório está organizado da seguinte forma:

- `project-01-bp/`: Projeto base inicial.
- `project-01-nbp/`: Nova versão do projeto base.

Cada projeto contém os seguintes arquivos e diretórios principais:

- `.vscode/`: Configurações específicas do Visual Studio Code.
- `install-vscode.yaml`: Playbook do Ansible para instalar o Visual Studio Code.
- `inventory.ini`: Arquivo de inventário com a configuração dos hosts.
- `README.md`: Instruções específicas para cada projeto.

## Utilização

### Pré-requisitos

- Ansible instalado na sua máquina.
- Acesso aos arquivos `install-vscode.yaml` e `inventory.ini` configurados corretamente.
- Arquivo `become_pass.yml` com a senha armazenada via Ansible Vault (quando aplicável).

### Execução dos Playbooks

1. Abra o terminal.
2. Navegue até o diretório do projeto desejado:

    ```sh
    cd <nome-do-projeto>
    ```

3. Execute o comando Ansible Playbook:

    ```sh
    ansible-playbook install-vscode.yaml -i inventory.ini (--ask-vault-pass)
    ```

4. Insira a senha do Vault quando solicitado (quando aplicável).

### Observações

- Certifique-se de que o arquivo `inventory.ini` contém as informações corretas dos hosts.
- O comando `--ask-vault-pass` solicitará a senha do Vault para descriptografar o arquivo `become_pass.yml` (quando aplicável).

## Contato

Para mais informações, questione o seu professor.

---

Este repositório é parte do material didático da disciplina de Elaboração de Projetos II e deve ser utilizado como referência para o desenvolvimento do projeto solicitado.
