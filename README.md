# Introdução

Um banco de dados não relacional é um banco de dados que não usa o esquema de tabela de linhas e colunas encontrado na maioria dos sistemas de banco de dados tradicionais. Em vez disso, os bancos de dados não relacionais usam um modelo de armazenamento otimizado para os requisitos específicos do tipo de dados que está sendo armazenado. Por exemplo, os dados podem ser armazenados como pares chave/valor simples, como documentos JSON ou como um gráfico que consiste em bordas e vértices.

O que esses armazenamentos de dados têm em comum é que eles não usam um modelo relacional. Além disso, eles tendem a ser mais específicos no tipo de dados ao qual dão suporte e no modo como os dados podem ser consultados. Por exemplo, os armazenamentos de dados de série temporal são otimizados para consultas em sequências de dados baseadas em tempo. No entanto, os armazenamentos de dados de grafo são otimizados para explorar as relações ponderadas entre entidades. Nenhum dos dois formatos será bem generalizado para a tarefa de gerenciamento de dados transacionais.

O termo NoSQL refere-se aos armazenamentos de dados que não usam o SQL para consultas. Em vez disso, os armazenamentos de dados usam outras linguagens de programação e constructos para consultar os dados. Na prática, "NoSQL" significa "banco de dados não relacionais", mesmo que muitos desses bancos de dados deem suporte a consultas compatíveis com SQL. No entanto, a estratégia de execução de consulta subjacente é geralmente muito diferente da maneira como um RDBMS tradicional executa a mesma consulta SQL.

### Para que é usado um banco de dados NoSQL?
Os bancos de dados NoSQL são amplamente usados em aplicativos da web em tempo real e big data, porque suas principais vantagens são alta escalabilidade e alta disponibilidade.

Os bancos de dados NoSQL também são a escolha preferida dos desenvolvedores, pois eles naturalmente aceitam um paradigma de desenvolvimento ágil, adaptando-se rapidamente aos requisitos em constante mudança. Os bancos de dados NoSQL permitem que os dados sejam armazenados de maneiras mais intuitivas e fáceis de entender, ou mais próximas da maneira como os dados são usados pelos aplicativos - com menos transformações necessárias ao armazenar ou recuperar usando APIs no estilo NoSQL. Além disso, os bancos de dados NoSQL podem aproveitar ao máximo a nuvem para oferecer tempo de inatividade zero.

### Benefícios de um banco de dados NoSQL
A velocidade e escala sem precedentes da interação digital e do consumo de dados observada nas últimas duas décadas exigiram que as empresas adotassem uma abordagem mais moderna e fluida de como armazenam dados e como os acessam. Com usuários em todo o mundo exigindo um fluxo ininterrupto de conteúdo e funções, não é de se admirar que os bancos de dados tenham que adaptar-se rapidamente. Com isso em mente, aqui estão alguns dos principais motivos pelos quais os desenvolvedores estão escolhendo NoSQL/bancos de dados não relacionais:

 - <strong>Flexibilidade</strong>
Com os bancos de dados SQL, os dados são armazenados em uma estrutura predefinida muito mais rígida. Mas com o NoSQL, os dados podem ser armazenados de uma forma mais livre, sem aqueles esquemas rígidos. Este design permite inovação e rápido desenvolvimento de aplicativos. Os desenvolvedores podem se concentrar na criação de sistemas para melhor atender seus clientes, sem preocupar-se com os esquemas. Os bancos de dados NoSQL podem lidar facilmente com qualquer formato de dados, como dados estruturados, semiestruturados e não estruturados em um único armazenamento de dados.
- <strong>Escalabilidade</strong>
Em vez de escalar adicionando mais servidores, os bancos de dados NoSQL podem escalar usando hardware comum. Isso tem a capacidade de suportar o aumento do tráfego para atender à demanda com tempo de inatividade zero. Ao expandir, os bancos de dados NoSQL podem se tornar maiores e mais poderosos, e é por isso que eles se tornaram a opção preferida para conjuntos de dados em evolução.
- <strong>Alto desempenho</strong>:
A arquitetura de expansão de um banco de dados NoSQL pode ser particularmente valiosa quando o volume de dados ou o tráfego aumenta. Conforme mostrado no gráfico abaixo, essa arquitetura garante tempos de resposta rápidos e previsíveis em milissegundos de um dígito. Os bancos de dados NoSQL também podem ingerir dados e entregá-los de forma rápida e confiável, e é por isso que os bancos de dados NoSQL são usados em aplicações que coletam terabytes de dados todos os dias, ao mesmo tempo que exigem uma experiência de usuário altamente interativa. No gráfico abaixo, mostramos uma taxa de entrada de 300 leituras por segundo (linha azul) com uma latência de 95 no intervalo de 3-4 ms e uma taxa de entrada de 150 gravações por segundo (linha verde) com uma latência de 95 no intervalo de 4-5ms.

### Tipos de bancos de dados NoSQL
Existem pelo menos quatro tipos principais de bancos de dados NoSQL:

#### Valor principal ou Chave-Valor

Este é o tipo mais flexível de banco de dados NoSQL porque o aplicativo tem controle total sobre o que é armazenado no campo de valor sem quaisquer restrições.

![image](https://user-images.githubusercontent.com/90854173/232905401-bd040cb5-ef74-4a27-ad5b-eb7c8faaf908.png)

#### Documento

Também conhecidos como armazenamento de documentos ou bancos de dados orientados a documentos, esses bancos de dados são usados para armazenar, recuperar e gerenciar dados semiestruturados. Não há necessidade de especificar quais campos um documento conterá.

![image](https://user-images.githubusercontent.com/90854173/232905132-0fa1a3c8-bc36-4725-837d-8449c5375d05.png)

#### Gráfico

Este banco de dados organiza os dados como nós e relacionamentos, que mostram as conexões entre os nós. Isso oferece suporte a uma representação de dados mais rica e completa. Bancos de dados gráficos são aplicados em redes sociais, sistemas de reserva e detecção de fraudes.

![image](https://user-images.githubusercontent.com/90854173/232905585-06cccb00-aa19-42b8-bf24-404f4ed8fdf7.png)


#### Coluna larga

Esses bancos de dados armazenam e gerenciam dados na forma de tabelas, linhas e colunas. Eles são amplamente implantados em aplicativos que requerem um formato de coluna para capturar dados sem esquema.

![image](https://user-images.githubusercontent.com/90854173/232905301-d6e031ff-0b33-4cc9-a969-a12dfdc5fc10.png)


# Arquitetura

Armazenamentos de dados não relacionais costumam usar uma arquitetura de armazenamento diferente da usada pelos bancos de dados relacionais. Especificamente, eles tendem a não ter nenhum esquema fixo. Além disso, eles tendem a não dar suporte a transações ou restringir o escopo das transações e geralmente não incluem índices secundários por motivos de escalabilidade.

Veja a seguir uma comparação dos requisitos de cada um dos armazenamentos de dados não relacionais:

| Requisito | Dados de Documentos | Dados de colunas | Dados de chave/valor | Dados de Gráficos|
| ---- | ---- | ---- | ----- | ---- |
| Normalização | Desnormalizado | Desnormalizado | Desnormalizado | Normalizado |
| Esquema | Esquema na leitura | Famílias de colunas definidas na gravação, esquema de coluna na leitura | Esquema na leitura | Esquema na leitura |
| Consistência (entre transações simultâneas) | Consistência ajustável, garantias no nível do documento | Garantias de nível da família de colunas | Garantias no nível da chave | Garantias no nível do gráfico |
| Atomicidade (escopo de transação) | Coleção | Tabela | Tabela | Grafo |
| Estratégia de Bloqueio | Otimista (livre de bloqueio) | Pessimista (bloqueios de linha) | Otimista (Etag) |  |
| Padrão de acesso | Acesso aleatório | Agregações em dados altos/largos | Acesso aleatório | Acesso aleatório |
| Indexação | Índices primários e secundários | Índices primários e secundários | Chave e valor | Gráfico que contém bordas e vértices |
| Esparsos | Sim | Sim | Sim | Não |
| Largo (grande quantidade de colunas/atributos) | Sim | Sim | Não | Não |
| Tamanho do dado | Pequeno (KBs) a médio (alguns MBs) | Médio (MBs) a grande (alguns GBs) | Pequeno (KBs) | Pequeno (KBs) |
| Escala máxima geral | Muito grande (PBs) | Muito grande (PBs) | Muito grande (PBs) | Grande (TB) |

# Bancos famosos:

### MongoDB

MongoDb é um banco de dados de código aberto com alta performance. Ele é aceito em diferentes sistemas operacionais e tem como característica ser orientado a documentos.

Sendo assim, ele armazena todas as informações relevantes em um documento e utiliza sistemas avançados de agrupamento e filtragem. Diferentes plataformas e linguagens possuem suporte ao MongoDB, entre elas estão o Java, JavaScript, PHP, Python e Ruby.

Os principais exemplos de empresas que usam o MongoDB são: o site Globo.com, MailBox, MTV e Pearson Education.

Esses são os principais exemplos de bancos de dados NoSQL ou não-relacionais. O uso entre eles pode se diferenciar de acordo com as necessidades de cada negócio. Portanto, o mais indicado é buscar o auxílio de uma empresa especializada em soluções de armazenamento de bancos de dados.

### Amazon DynamoDB
Este é um banco de dados NoSQL em nuvem, disponibilizado pela Amazon Web Service. Ele tem baixa latência, é rápido e flexível, sendo o modelo ideal para aplicações móveis, jogos na web e soluções com internet das coisas.

Ele ainda apresenta alto desempenho e escalabilidade automática, características imprescindíveis para negócios que precisam crescer com eficiência.

### Cassandra 
Este banco de dados NoSQL foi desenvolvido no Facebook. Ele usa um banco de dados descentralizado, em que os dados são armazenados em vários datacenters. Ele é otimizado para cluster e fornece baixa latência em suas atualizações.

### Redis
O Redis é o banco de dados NoSQL de chave-valor mais utilizado em todo o mundo. Ele vincula um valor a uma chave na sua estrutura, o que facilita o armazenamento e a busca desses dados. Por isso, é muito utilizado pelos desenvolvedores.

### HBase
O Hbase é um banco de dados que utiliza conjunto de linhas e colunas para armazenar as informações. Ele é utilizado em diferentes plataformas como o LinkedIn, Facebook e Spotify 


### Referências:
- https://www.oracle.com/br/database/nosql/what-is-nosql/#:~:text=que%20%C3%A9%20NoSQL%3F-,NoSQL%20definido,formato%20diferente%20das%20tabelas%20relacionais.
- https://learn.microsoft.com/pt-br/azure/architecture/data-guide/big-data/non-relational-data
- https://blog.saphir.com.br/conheca-os-principais-bancos-de-dados-nosql-nao-relacionais/
