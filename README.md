# Proxmox Hypervisor Recipes

- Habilita o repositório proxmox public
- Desabilita o repositório enterprise
- Atualiza o repositório do Debian
- Instala os pacotes adicionais padroes

# Setup
O arquivo host está dentro do dir. roles.

## Tags utilizadas
- setup : Para ser executada no ambiente PROXMOX recém instalado 

# Dependencias

## Roles
- Debian

# Exemplo

```shell
export REPO_PATH="/var/lib/ansible/roles"
export TAGS="--tags setup"
export CMD="ansible-playbook -i $REPO_PATH/hypervisor/hosts $REPO_PATH/hypervisor/recipes.yaml $TAGS"

echo $($CMD)
```