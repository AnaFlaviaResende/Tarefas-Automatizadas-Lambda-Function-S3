# Tarefas-Automatizadas-Lambda-Function-S3
Este repositório serve como material de apoio para estudos e futuras implementações.

# Conceito básico

AWS Lambda: serviço de computação serverless que executa código em resposta a eventos. Não precisa gerenciar servidores, você só paga pelo tempo de execução.

Amazon S3: serviço de armazenamento de objetos (arquivos, imagens, logs, backups etc.).

Lambda + S3: Lambda pode ser acionado automaticamente quando algo acontece em um bucket S3.

# Tipos de eventos do S3 que podem disparar uma Lambda

PUT: quando um arquivo é enviado para o bucket.

POST: similar ao PUT, geralmente usado com formulários.

DELETE: quando um arquivo é removido.

COPY: quando um arquivo é copiado.

Exemplo: cada vez que alguém envia uma imagem para o bucket uploads, uma Lambda é acionada para redimensionar a imagem automaticamente.

# Casos de uso comuns

Processamento de arquivos

Redimensionar imagens

Converter arquivos de CSV para JSON

Compressão de arquivos grandes

Backups e replicação

Copiar automaticamente arquivos para outro bucket ou região

Fazer backup incremental de arquivos importantes

Validação e limpeza

Validar nomes ou formatos de arquivos enviados

Remover arquivos duplicados ou inválidos

Notificações

Enviar e-mails quando novos arquivos forem carregados

Registrar logs em outro sistema ou serviço

# Como funciona na prática

Cria-se um bucket no S3.

Cria-se uma função Lambda com o código para executar a tarefa desejada.

Configura-se um evento de S3 que aciona a Lambda quando um arquivo é criado, deletado ou modificado.

Lambda executa o código automaticamente, sem intervenção manual.