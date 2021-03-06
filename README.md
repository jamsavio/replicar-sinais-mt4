# Replicar sinais através do MT4
## Sistema desenvolvido na linguagem MetaQuotes da plataforma de negociação MetaTrader 4 utilizando a lib `MQLMySQL` 

### Documentos: `server.ex4` e `client.ex4` 

###### `server.ex4` é o responsável por enviar o registro das ordens que forem abertas para o banco de dados. (Servidor) 
###### `client.ex4` é o responsável por capturar o registro das ordens no banco de dados e executá-las. (Cliente)

# Manual de instalação
###### Importante: Alterar os dados de conexão com o banco de dados nos arquivos `server.mq4` e `client.mq4` e compilar de novo. 

* Colocar cada documento nas suas respectivas pastas do `MetaTrader 4`
* Importar as tabelas   
* Liberar porta 3306 no servidor (VPS) para receber conexões externas  
* Usar o EA (`server.ex4`) no MetaTrader 4 do Master que irá emitir os sinais. 
* Fazer a mesma coisa com o EA (`client.ex4`) nas Slaves que irão receber os sinais. 
* Criar registro na tabela `fx_assinaturas` com os dados (id->Nome de usuário na corretora / nome->Nome real) e tempo de licença de cada cliente que irá receber os sinais. 
* Verificar na aba `Expert Advisors (Robôs)` do terminal se os EAs estão funcionando corretamente. 
* **Enjoy**

#### Créditos : [HOW TO ACCESS THE MYSQL DATABASE FROM MQL5 (MQL4)] (https://www.mql5.com/pt/articles/932) .

