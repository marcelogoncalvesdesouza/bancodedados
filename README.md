## Banco de dados
Prof. Marcelo Gonçalves de Souza

<B>As oito etapas para a modelagem de dados</B>

- Entender o <B>PROBLEMA</B>
Neste início deve-se entender qual a natureza dos dados e como eles irão se conectar. Por exemplo: Em uma clínica médica o que é importante? Como tirar um maior proveito desse banco de dados? É necessário se informar com o responsável pelo projeto (cliente, colaboradores, etc) o que seria viável ter disponível no banco de dados a qualquer momento de forma íntegra, ou seja, sem brechas para duplicidade de informações inconsistentes.

- <B>MER</B> (Modelo Entidade-Relacionamento)
 Etapa em que se identifica as entidades (tabelas), atributos (características) e relacionamentos (integração dos dados relacionais). Por exemplo: A entidade Médico possui qual relação com a entidade Especialidade?

- <B>DER</B> (Diagrama Entidade-Relacionamento)
Fase em que tendo as entidades, características e relacionamentos definidos colocamos estas informações em formato de diagrama para que qualquer programador posso interpretá-lo.

- Cardinalidades
Definir quais são as cardinalidades entre essas entidades (tabelas). Em suma, quais serão as possibilidades de inserção no banco de dados, as regras do jogo. Por exemplo um médico pode ter uma especialidade ou ele pode ter mais de uma especialidade? E uma especialidade pode ter um ou mais médicos registrados?

- Modelo <B>LÓGICO</B>
Momento em que se define o modelo lógico com base no MER e do DER. Quais são as tabelas que nós teremos? As entidades são as bases para as tabelas e os atributos serão bases para as colunas. Por exmeplo a entidade Especialidade dará origem a tabela especialidade e os atributos às colunas, tais como um campo identificador, descrição e observação.

- Normalização
Etapa que se aplicam verificações nas tabelas para garantir que elas atendas os requisitos. Um método para realizar isto são as cinco formar normais - 5FN - com isso garantindo uma estruturação profissional.

- Dicionário de dados
Documentação para registrar toda a lógica usada para a criação do banco de dados. O grande objetivo é a possibilidade de entendimento do projeto meses e/ou anos depois para a manutenção ou escalabilidade do projeto.

- Modelo <B>FÍSICO</B>
É a implementação dentro de um Sistema Gerenciador de Banco de Dados (SGBD), como: PostgreSQL, MySQL, Oracle, etc. Por intermédio da linguagem SQL (Structured Query Language, na tradução livre, Linguagem de Consulta Estruturada) vamos organizar as nossas tabelas dentro do SGBD com o objetivo homologar o projeto e verificar seu funcionamento para a produção (momento em que o cliente começa a utilizar o sistema desenvolvido).