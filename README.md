# Infraestrutura como Código (IaC)

## Visão Geral
A Infraestrutura como Código (IaC) é a prática de gerenciar e provisionar a infraestrutura de TI através de arquivos de definição legíveis por máquina, em vez de processos físicos de hardware ou ferramentas de configuração interativas.

## Benefícios
- **Consistência:** Elimina o erro humano ao configurar servidores e componentes de rede.
- **Escalabilidade:** Facilita a escalabilidade de sistemas.
- **Desenvolvimento Contínuo:** Integração com CI/CD para implantações automáticas.
- **Documentação Automática:** A infraestrutura é auto-documentada pelo código.

## Ferramentas Populares
- **Terraform:** Uma ferramenta de código aberto para definir e fornecer data centers por meio de uma linguagem de configuração de alto nível.
- **Ansible:** Uma ferramenta de automação de TI que gerencia sistemas de forma declarativa.
- **AWS CloudFormation:** Um serviço que ajuda a modelar e configurar recursos da AWS.
- **Puppet:** Uma plataforma de automação que permite entregar e operar software em qualquer lugar.

## Exemplo de Uso
Aqui está um exemplo básico de um script Terraform para provisionar uma instância EC2 na AWS:

```hcl
provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleInstance"
  }
}
