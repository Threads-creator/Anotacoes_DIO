## Business Intelligence (BI)

É o processo de utilização de ferramentas, infraestrutura de TI e dados para auxiliar a tomada de decisões dentro de uma empresa. O BI extrai informações importantes e realiza análise de dados através da mineração de dados, inteligência artificial, visualização de dados e outros. Os **dados** são originados de diversas fontes:

- **Dados da operação**: dados que provem das atividades operacionais da empresa(venda, suporte, entre outros);
- **Dados gerenciais**: dados originados do departamento gerencial da empresa;
- **Pesquisa de campo**: dados originados de pesquisas com clientes, chatbots entre outros;
- **Indicadores de mercado**: pesquisas que abordam a situação do mercado da empresa;

## Data Warehouse

É um repositório central de informações que podem ser analisadas para tomar decisões mais adequadas. Os dados provem principalmente de duas fontes: 

- **OLTP** (On-Line Transaction Processing): banco de dados de operações voláteis na empresa. Está relacionada a transações e envolvem dados da área operacional da empresa
- **OLAP** (On-Line Analytical Processing): banco de dados com poucas alterações. Está relacionado a sumarização de dados para análise gerencial, envolve a área tática da empresa.

O data warehouse utiliza dos dados da empresa para formar "resumos" de períodos das informações da empresa e são armazenados em OLAP DW.

## Big Data

É uma coleção de uma grande quantidade de informações em formatos diversos, voz, video, texto, emails entre outros.

## Dados Não estruturados

### Dados semi-estruturados

Dados que são minimamente estruturados, são mais permissivos a alterações e aos tipos de dados que são armazenados. Ex: xml, json, rdf, owl.

Os banco de dados que armazenam esse tipo de informação são os bancos **NoSQL (Not Only SQL)**. Exemplos de bancos NoSql: cassandra, mongodb, apache hbase e outros.

### Dados não estruturados

Dados que não seguem uma estrutura padrão. Ex: twits, posts no facebook, dados de redes sociais, entre outros.

## Data Lake

É um conjunto muito grande de dados brutos em diversos formatos que estão presentes em uma empresa. Esses dados são definidos como brutos por não terem passados por um processamento útil para os objetivos da empresa. Todos os dados são mantidos, nada é removido ou filtrado antes do armazenamento.





## MongoDb Prática

Para entrar no cli do mongoDB deve-se definir o local de instalação como uma variável de ambiente do Windows. Depois entre no **cmd** e digite **mongo**. Então você entrará no promp de comando do sgbd, dentres os comandos usados:

- **use**: cria um novo banco de dados
- **db."nomeTabela".insert({ "objeto json" })** : cria uma tabela e insere objetos nela 
- **db."nomeTabela".find()** : busca todos os dados da tabela 





## Arquitetura em Nuvem

Consiste na utilização de serviços e infraestrutura de TI por uma empresa sendo que essa infraestrutura não esta localizada dentro da empresa e sim em servidores de empresas terceiras acessados através da internet. Tipos de arquitetura em nuvem:

- **IaaS** (Infraestrutura como Serviço): fornece infraestrutura de TI, como armazenamento, processamento de dados, firewall, segurança de rede, entre outros através da internet. Ex: Microsoft Azure, Google Cloud, Amazon AWS.
- **PaaS** (Plataforma como um Serviço): fornece uma plataforma que facilita o gerenciamento da infraestrutura de TI em nuvem. Por exemplo plataformas para configurar servidores e hosts, gerenciamento de banco de dados, business analytics e outros. Ex: Terraform e CloudFormation
- **BaaS**(Backend como um Serviço): fornece um serviço de backend acessível via internet. Exemplo: Firebase, banco de dados para aplicações mobiles que geram relatórios e prove apis para aplicações android.

### Disponibilidade

Serviços em nuvem podem ser escalonados de algumas formas, dentre elas através de containers. Pode ser feito por Kubernets (k85) por exemplo. **Dica**: via de regra, é recomendável definir multiplos nodos de uma aplicação, no mínimo 3 nodos. Um bom *load balancer* (gerenciador de conexões) é importante para balancear a carga entre os nodos.

### Serverless

Consiste no modelo se desenvolvimento nativo em nuvem em que a abstração de implantação, gerenciamento e provisionamento de recursos computacionais fica  a cargo do provedor do serviço serverless. O desenvolvedor apenas precisa se preocupar com o desenvolvimento da aplicação e levantar a aplicação em container na nuvem. O resto fica a cargo do serviço nuvem que funciona através de eventos, criando novas instancias de acordo com a demanda. Todo o processo de patch de segurança, monitoramento, escalonamento fica de responsabilidade do provedor de serviço nuvem. Ex: API Gateway, AWS Lambda, Amazon Kinesis, Amazon S3.



## DevOps

É um termo criado para definir o conjutno de práticas que integram e automatizam os processos entre as equipes de desenvolvimento, operações e de apoio(como QA) para produção rápida e confiável de software. Para verificar a presença de devops utiliza-se o **framework CALMS** cujos princípios são:

- **Culture**: as ferramentas e automação são inúteis se as pessoas envolvidas não possuirem uma cultura de colaboração entre elas
- **Automation**: elimina trabalho manual repetitivo, gerando velocidade na entrega e torna os envolvidos mais produtivos
- **Lean (enxuto, magro)**: foca nas entregas de valor para o cliente. Verifica-se as limitações e gargalos do processo, de modo a focar apenas no que gera valor ao cliente
- **Measurement**: deve-se realizar métricas dos softwares produzidos para a melhoria contínua. Os dados podem ser logs, feedbacks e outros
- **Sharing**: compartilhamento de conhecimento para criação de times genéricos, com conhecimentos básicos em diversos assuntos do negócio e tecnologias. Time se torna autossustentável. Assim caso alguém saia da equipe, não haverá problemas graves e a identificação de novas melhorias é facilitada

#### 3 Princípios

O DevOps é cíclico e possui os seguintes princípios:

- **Flow**: aplicação de metodologias ágeis e automação
- **FeedBack**: monitoramento ajuda a gerar informações relevantes para evolução do projeto
- **Learning**: visa gerar conhecimento através da experimentação. Hipóteses são melhores do que uma certeza imediata, isso reduz as consequências e a carga emocional dos erros sobre a equipe

### CI (Continuous Integration)

Consiste na análise do código, testes unitários e empacotamento dos artefatos gerados

###  CD (Continuous Delivery/Deployment)

Consiste na implementação do projeto, sendo realizado testes de deploy e testes de integração. Quando é automatizado e não passa por nenhum aprovador (pessoa que aceita a solução) é Deployment se não é Delivery. 

Ferramentas: CircleCI, AppVeyor, Azure Pipelines, Gitlab CI, Travis CI, Jenkins e outros. Exemplo Prático: https://github.com/ThiagoBarradas/jsonmasking

### Continuous Inspection

Consiste na utilização de ferramentas que automatizam a análise da qualidade do código. Essas ferramentas reportam códigos duplicados, métodos comentados, verifica a complexidade do código, quantidade de ifs entre outros. Exemplos de ferramentas: SonarQube, CodeClimate, Codacy.



