# hashicorp-tools

Imagem com ferramentas da Hashicorp para Infraestrutura:

* Packer
* Vault
* Terraform
* Consul Template

## Criar imagens

```
export PACKER_VERSION='x.x.x'
export VAULT_VERSION='x.x.x'
export TERRAFORM_VERSION='x.x.x'
export CONSUL_TEMPLATE_VERSION='x.x.x'
docker build --network host -t <image_name>:<tag> \
    --build-arg PACKER_VERSION \
    --build-arg VAULT_VERSION \
    --build-arg TERRAFORM_VERSION \
    --build-arg CONSUL_TEMPLATE_VERSION .
```

## Automação

Automatizado para criar imagem com GitLab CI/CD, usando GitLab Runner com suporte a Docker (standalone ou Kubernetes).