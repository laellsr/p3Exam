# Primeira Prova de Projeto de Software

## Sistema para Gerenciamento de Projetos


![Diagrama de Classes](https://github.com/laellsr/p3Exam/blob/master/P3exame.png)

## Classes

1. **Main**
- Classe utilizada para iniciar os comandos no sistema e gerenciar os objetos.

2. **Modelo**
- Formulada para generalizar os atributos frequentes nas subclasses *Projeto* e *Atividade*, tais como um número para identificação, texto para descrição e dados como data e hora.

2.1. **Projeto**
- Contém os dados essênciais do projeto tais como o status do projeto, o coordenador, os associados e as atividades.

2.2. **Atividade**
- Contém os dados das atividades que serão utilizadas nos projetos tais como o responsável, as tarefas exercidadas e os seus realizadores.

3. **Usuario**
- Esta classe define o nome do usuário e o seu tipo que pode ser alunos de graduação, mestrado e doutorado, professores e pesquisadores (coordenadores), profissionais (desenvolvedor, testador e analista) e técnico. O usuário guarda a identificação dos projetos e das atividades associados a ele em uma lista de inteiros.

## Distribuição dos Métodos

**Métodos de Criação e de Exclusão de Objetos**

- criarProjeto(), deletarProjeto(), criarUsuario() e deletarUsuario().

Para evitar a criação de outras classes ou a alta carga de overrides e também pela facilidade de administrar os dados, os métodos de criação e de exclusão foram postos na *Main*. Dela é possível controlar os projetos e os usuários guardados em listas de vetores de cada tipo. Ao criar, é retornado o objeto criado. Para deletar, é necessário passar os parâmetros de identificação que pode ser uma numeração, caso seja um projeto, ou uma string, caso seja um usuário, junto com a sua lista.

**Métodos de Pesquisa de Objetos**

- consultaUsurario(), consultaProjeto(), consultaAtividade() e relatorioProjeto().

Também incluídos na *Main*, eles fazem a busca de dados dentro de cada lista.

**Métodos de Gerenciamento de Atributos do Objeto**

- adicionarUsuario(), removerUsuario() e alterarStatus().

Esses métodos são polimórficos pela necessidade de generalização, 75% deles são aproveitados em todas as subclasses. Atuam em *Projeto* e em *Atividade*.

## Herança
(*Ver imagem "Diagrama de Classes" no cabeçalho*)

- Basicamente, *Projeto* e *Atividade* tem 70% dos atributos e 75% dos métodos semelhantes, então, para evitar problemas com duplicação, foi criado a superclasse *Modelo* para reunir esses dados em comum.

## Tratamento de Exceções

É necessário o tratamento de exceções quando os atributos de inteiro recebem valores diferentes de números, diferente dos outros atributos que podem receber valores númericos em sua entrada.
