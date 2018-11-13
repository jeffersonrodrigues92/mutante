## MUTANTE - MERCADO LIVRE

Magneto quer recrutar tantos mutantes para lutar contra os X-Men.

Ele contratou você para desenvolver um projeto que detecta se um
Humano é mutante baseado em sua sequência de DNA.

## SOBRE O AMBIENTE

- Ambiente foi desenvolvido em duas funções AWS Lambda, sendo uma função chamada Mutante (verifica se é mutante e salva no banco de dados) e a segunda função chamada Mutante Stats que representa o retorno do objeto quantidade de humanos, mutantes e o ratio. 

- Ambiente 100% serverless.
- Escabilidade Contínua, sem provisionar ou gerenciar servidores.
- Monitorado via CloudWatch (Dashboard construído na AWS).
- Altamente perfomático com a média de response time de 210ms para busca.

## TECNOLOGIAS
- Java 8
- AWS API Gateway
- AWS Lambda
- AWS DynamoDB
- AWS S3
- AWS CloudWatch 
- JUnit
- Mockito

## URL API 

AWS API Gateway: https://zvgr0hmrr1.execute-api.us-east-1.amazonaws.com/prd/

## SERVIÇOS

Verifica DNA Mutante e persiste os dados.

Request:

POST - /mutant
Request body (Exemplo DNA Mutante):
  ```json
  {"dna":["ATGCGA", "CAGGGC", "TTATGT", "AGAAGG", "CCCCTA", "TCACTG"]}
```
Response Status:
  200 OK

POST - /mutant
Request body (Exemplo DNA Humano):
  ```json
  {"dna":["AATACT", "CCCAGA", "GGGATT", "AATTCC", "AGAGCG", "TCACTG"]}
```
Response Status:
  403 Forbidden

## SWAGGER

- Caso tenha dúvidas acesse o Swagger para verififcar todos os serviços disponíveis
- Swagger https://s3.amazonaws.com/mercado-livre-mutante-swagger/mutant-prd-swagger.json

## Desenvolvedor
Jefferson Rodrigues

## LinkedIn
https://www.linkedin.com/in/jefferson-nascimento-rodrigues/


