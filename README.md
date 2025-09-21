# DIO_Diagramas
Aqui está meu primeiro projeto público feito no Bootcamp Santander Code Girls 2025 da DIO. Ele contém 2 diagramas principais:

Primeiro Diagrama:
É o arquivo Fluxo_UPLOAD, em que mostra um usuário acessando a API por meio de seu computador, utilizando uma chave de autenticação e enviando arquivos via método POST. Esses arquivos são encaminhados para uma função AWS Lambda, que define dois fluxos possíveis: caso os dados sejam relacionados, eles são armazenados no DynamoDB; caso contrário, são enviados para o S3. Dentro do S3, considerei uma regra de ciclo de vida pré definida que move automaticamente arquivos com mais de 60 dias sem alteração para o S3 Glacier, garantindo armazenamento de longo prazo e mais econômico.

Segundo Diagrama:
É o arquivo EC2, em que mostra a interação de um usuário com uma instância do Amazon EC2, que funciona como servidor em nuvem responsável por processar aplicações e atender requisições. Essa instância está conectada a múltiplos volumes do Amazon EBS (Elastic Block Store), que fornecem armazenamento em bloco persistente. Os volumes EBS funcionam como discos virtuais anexados ao EC2, permitindo que dados sejam gravados, consultados ou mantidos mesmo após a interrupção da instância. Esse tipo de arquitetura é comum quando se deseja separar diferentes tipos de dados, ampliar a capacidade de armazenamento ou garantir maior flexibilidade e resiliência para aplicações executadas na nuvem.
