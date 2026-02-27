# Pesquisa: Bancos de Dados Não-Relacionais (NoSQL)

Este repositório contém a pesquisa realizada para a disciplina do SENAI sobre bancos de dados NoSQL.

 1. Definição e Características

*   **a) O que caracteriza um banco de dados não-relacional?**
    Diferente dos bancos SQL tradicionais, eles não utilizam o modelo de tabelas rígidas com linhas e colunas. Eles são caracterizados por terem esquemas flexíveis (schemaless), alta escalabilidade horizontal e serem otimizados para tipos específicos de dados (documentos, grafos, etc).
*   **b) Vantagens em relação aos bancos relacionais:**
    Flexibilidade no armazenamento de dados não estruturados, facilidade de expansão (escalabilidade) e performance superior para grandes volumes de leitura/escrita em tempo real.
*   **c) 3 situações práticas indicadas:**
    1. Sistemas de Big Data e análise em tempo real.
    2. Gestão de conteúdo (CMS) e catálogos de produtos com atributos variáveis.
    3. Aplicações de IoT (Internet das Coisas) que geram fluxos massivos de dados.

## 2. Tipos de Bancos de Dados Não-Relacionais

### a) Diferenças entre os tipos:
*   **Orientados a Documentos:** Armazenam dados em documentos (como JSON ou BSON). Ex: MongoDB.
*   **Chave-Valor:** O modelo mais simples, onde um valor é acessado por uma chave única. Ex: Redis.
*   **Colunas Amplas (Wide-Column):** Armazenam dados em famílias de colunas, otimizados para consultas em grandes datasets. Ex: Cassandra.
*   **Grafos:** Focados em relacionamentos entre entidades usando nós e arestas. Ex: Neo4j.

### b) Exemplos de Ferramentas:
*   **Documentos:** MongoDB, CouchDB.
*   **Chave-Valor:** Redis, Amazon DynamoDB.
*   **Colunas:** Apache Cassandra, HBase.
*   **Grafos:** Neo4j, ArangoDB.

## 3. Comparação Prática

*   **a) Relacional vs. Grafos:** No relacional, as relações são feitas via chaves estrangeiras (JOINs caros). No banco de grafos, o relacionamento é um dado nativo, permitindo percorrer conexões complexas com extrema rapidez.
*   **b) Redes Sociais:** O banco de **Grafos** seria o mais adequado. Justificativa: Redes sociais dependem fortemente de conexões (amigo do amigo, sugestões de seguimento), e os grafos gerenciam essas relações de forma muito mais eficiente que tabelas.

## 4. Escalabilidade e Flexibilidade

*   **a) Escalabilidade Horizontal:** Ao contrário da vertical (comprar um servidor mais potente), a horizontal consiste em adicionar mais máquinas comuns (nós) ao sistema. O banco NoSQL distribui os dados entre esses vários servidores automaticamente (sharding).
*   **b) Flexibilidade de Schema:** É importante porque permite que cada documento tenha uma estrutura diferente. Se você precisar adicionar um campo novo a um registro, não precisa alterar a estrutura de toda a tabela ou parar o banco.

## 5. Estudo de Caso

*   **a) Empresa:** Netflix.
*   **b) Uso e Benefícios:** A Netflix utiliza o **Apache Cassandra** para gerenciar o histórico de visualização e as preferências de milhões de usuários globalmente. O benefício principal é a alta disponibilidade e a latência extremamente baixa, garantindo que o serviço nunca fique fora do ar, mesmo que um servidor falhe em algum lugar do mundo.
