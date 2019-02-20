# Primeira Prova de Projeto de Software
Sistema para Gerenciamento de Projetos

## Classes

1. Main
- Classe utilizada para iniciar os comandos no sistema e gerenciar os objetos.

2. Modelo
- Formulada para generalizar os atributos frequentes nas subclasses *Projeto* e *Atividade*, tais como um número para identificação, texto para descrição e dados como data e hora.

2.1. Projeto
- Contém os dados essênciais do projeto tais como o status do projeto, o coordenador, os associados e as atividades.

2.2. Atividade
- Contém os dados das atividades que serão utilizadas nos projetos tais como o responsável, as tarefas exercidadas e os seus realizadores.

3. Usuario
- Esta classe define o nome do usuário e o seu tipo que pode ser alunos de graduação, mestrado e doutorado, professores e pesquisadores (coordenadores), profissionais (desenvolvedor, testador e analista) e técnico.

## Distribuição dos Métodos

**Métodos de Criação e de Exclusão de Objetos**

- criarProjeto(), deletarProjeto(), criarUsuario() e deletarUsuario()

Para evitar a criação de outras classes ou a alta carga de overrides e também pela facilidade de administrar os dados, os métodos de criação e de exclusão foram postos na *Main*. Dela é possível controlar os projetos e os usuários guardados em listas de vetores de cada tipo.

**Métodos de Pesquisa de Objetos**

- consultaUsurario(), consultaProjeto(), consultaAtividade() e relatorioProjeto()

Também incluidos na *Main*, eles fazem a busca de dados dentro de cada lista.
