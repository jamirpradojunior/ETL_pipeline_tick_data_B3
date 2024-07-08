# ETL_pipeline_tick_data_B3
Este código busca exemplificar um pipeline ETL (Extract, Transform, Load) usando Python. 
Mantive o formato .ipynb (notebook) para facilitar o acompanhamento da rotina por iniciantes.

Ele está dividido em três etapas:
1) Extração de múltiplos dados via webscraping;
2) Transformação dos dados;
3) Carregar os dados já estrurados para um database;


Os principais comandos automatizados:
* Checa os arquivos na pasta referência e seleciona as datas que já possuem dados;
* Baixa as datas que não possuem dados (formato txt mas zipados);
* Extrair os arquivos zip e depois os deleta;
* Carrega os arquivos txt, transforma em parquet e deleta os txt;
* Corrige o formatos de dados (str, float e datetime) e exclui colunas redundantes;
* Salva os arquivos e faz um teste de integridade dos dados entre tabelas;
* Faz a primeira carga num banco de dados SQL local;
* Faz uma segunda carga (incremental) no banco de ados criado.
