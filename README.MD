# MBA Full Stack - Data Engineering Foundation

## Trabalho Final

Italo Fernandes

Thiago Marinho

#

Utilizando os conjuntos de dados a seguir:

https://ckan.pbh.gov.br/dataset/b127c1d8-9e1b-4820-884a-8bd8129ba5e3/resource/903286ca-b77f-44ad-aa6a-958aa018c33f/download/si_env-2019.csv
- Relação de pessoas envolvidas em acidentes de trânsito

https://ckan.pbh.gov.br/dataset/a07412b3-8371-402a-8ca6-68a518bf2403/resource/ad490dd1-7af5-4868-b35f-9471f15be744/download/si-log-2019.csv
- Relação de logradouros dos locais de acidentes de trânsito

https://ckan.pbh.gov.br/dataset/6511cb66-3635-4560-95cc-d0c39aafb547/resource/ab6db535-b706-4e7b-9fdc-3bc1e823401e/download/si-bol-2019.csv
- Relação de ocorrências de trânsito

Carregue os arquivos no Hadoop/Hive, em seguida construa as seguintes analises:

1) Total de acidentes com vítima por bairro em acidentes com embriaguez;
2) Total de acidentes por tipo de pavimento e condição do tempo;
3) Total de pessoas acidentadas por tipo de veiculo e tipo de pavimentação;
4) Média de idade dos condutores por tipo de veículo e tipo de acidente;
5) Média de idade dos condutores por indicativo de embriaguez;

A entrega deve conter:

-Os códigos fonte necessários para a carga dos dados;

-O notebook com o resultado das analises;

#
## comandos

$ vagrant up

$ vagrant ssh node1

$ hdfs dfs -mkdir -p /user/vagrant/dados/trabalho-final

$ hdfs dfs -put /vagrant/trabalho-final/si_env-2019.csv /user/vagrant/dados/trabalho-final/

$ hdfs dfs -put /vagrant/trabalho-final/si-bol-2019.csv /user/vagrant/dados/trabalho-final/

$ hdfs dfs -put /vagrant/trabalho-final/si-log-2019.csv /user/vagrant/dados/trabalho-final/

$ cd /vagrant

$ export PYSPARK_DRIVER_PYTHON=jupyter

$ export PYSPARK_DRIVER_PYTHON_OPTS='notebook --ip 0.0.0.0'

$ pyspark
