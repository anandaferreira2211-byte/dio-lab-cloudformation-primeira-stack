# 🚀 Desafio DIO: Implementando Minha Primeira Stack com AWS CloudFormation

Este repositório documenta a prática realizada como parte do desafio da DIO, que teve como objetivo implementar uma Stack simples utilizando o serviço **AWS CloudFormation** (Infraestrutura como Código - IaC).

---

## 🎯 Requisitos do Desafio (Entregável)

* **Objetivo:** Implementar a primeira Stack na AWS CloudFormation.
* **Entrega:** Repositório organizado (público) contendo anotações e insights.
* **Ferramentas:** AWS CloudFormation, S3 e GitHub (para documentação).

## 👩‍💻 A Prática: Provisionando um Amazon S3 Bucket

O recurso escolhido para este laboratório foi um **Amazon S3 Bucket**, um serviço de armazenamento simples, ideal para uma primeira Stack.

### 1. Template CloudFormation (O Código)

O template define o estado desejado da nossa infraestrutura. O arquivo `primeiro-bucket-ananda.yaml` foi utilizado:

```yaml
AWSTemplateFormatVersion: "2010-09-09"
Description: >
  Template para criar o primeiro bucket S3 da Ananda com CloudFormation.
  
Resources:
  MeuBucketS3Ananda:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: minha-primeira-stack-cfn-ananda-20251023 # Nome único globalmente
      AccessControl: Private
      Tags:
        - Key: Projeto
          Value: LaboratorioCloudFormation
        - Key: Nome
          Value: BucketDaAnanda
