#Curso Git & GitHub 2025

Um curso para iniciantes aprenderem a trabalhar com versionamento de código e repositórios remotos com GitHub.

Além disso, vamos trabalhar com GitFlow ao final do curso e VS Code.

## Fluxo de trabalho Git local

01. git checkout -b <nova-branch>
02. cria ou atualiza arquivos
03. git status
05. git add *arquivos*
06. git status
07. git commit -m "minha mensagem"
08. git checkout main
09. git merge nova_branch

## Fluxo de trabalho GitHub <> Local (projeto próprio ou da sua empresa)
01. git clone <endereco do projeto>
02. git checkout -b <nova_branch>
03. alterações de arquivos
04. git status
05. git add *arquivos*
06. git status
07. git commit -m "nova mensagem"
08. git push origin <nova_branch>
09. abrir Pull request no GitHub para main
10. excluir <nova_branch> origin
11. git checkout main
12. git branch -D <nova_branch>

## Fluxo de trabalho GitHub <> Local (projetos open-source)
01. Fork do projeto para seu próprio github
02. git clone <endereco do projeto fork>
03. git checkout -b <nova_branch>
04. alterações de arquivos
05. git status
06. git add *arquivos*
07. git status
08. git commit -m "nova mensagem"
09. git push origin <nova_branch>
10. abrir Pull request no GitHub da branch fork para a main do projeto original
11. excluir <nova_branch> origin
12. git checkout main
13. git branch -D <nova_branch>

----

##Fluxo de trabalho - Git Flow

>> no repositorio remoto criar uma nova branch com nome de "develop"

>> no repositorio local utilizar os seguintes comandos:

git fetch (verificar as branch no remoto)

git branch

git checkout develop (aqui não esta criando esta acessando e "puxando" a branch do remoto)

git branch

git pull origin develop (garantir que tudo que esta no develop estaja atualizado no local)

git checkout -b <nova_branch>

	1 — Os tipos de categoria do branch. Os tipos podem ser os seguintes:

   
    docs: apenas mudanças de documentação;
    feat: uma nova funcionalidade;
    fix: a correção de um bug;
    perf: mudança de código focada em melhorar performance;
    refactor: mudança de código que não adiciona uma funcionalidade e também não corrigi um bug;
    style: mudanças no código que não afetam seu significado (espaço em branco, formatação, ponto e vírgula, etc);
    test: adicionar ou corrigir testes.

	exemplos:
	
	git checkout -b feat/01
	
	git checkout -b teste/01
	
	git checkout -b teste/02

	git checkout -b docs/readme
	
>>alterações nos arquivos

git status

git add .

git commit -m "Mensagem padronizada"

	O Conventional commits se utiliza dos tipos baseados na Convenção do Angular:

    build: alterações que afetam o sistema de build ou dependências externas. (ex: npm, nugget)

		build(webpack): atualizar entry point do build

    ci: alterações em arquivos e scripts de integração contínua.

		ci(azure-pipelines): usar template de ci de dotnet

    docs: alterações somente na documentação.

		docs(readme): melhorar documentação sobre dependências

    feat: uma nova funcionalidade.

		feat(login): implementar serviço de login

    fix: uma correção de bug.

		fix(login): corrigir bug de validação de email

    perf: alterações que melhoram o desempenho.

		perf: mover links de css para o HEAD do html

    refactor: refatorações de código.

		refactor(login): ordenar imports em ordem alfabético

    style: alterações que não afetam o significado do código (espaço em branco, formatação, ponto e vírgula, etc).

		style: formatar código com prettier

    test: adição de testes que faltavam ou corrigindo testes existentes.

		test(login): escrever testes do serviço de login

    revert: reverte um commit que foi feito

		revert: nunca mais falaremos do incidente do miojoRefs: 676104e, a215868
		
git push origin <nome da branch padronizado>

>>Realizar um pull request no github para a branch DEVELOP
	OBS.: VERIFICAR NO GITHUB SE ESTA APONTANDO PARA BRANCH DEVELOP. POR PADRÃO, SEMPRE APONTA PARA MAIN

>>Deletar a branch no remoto

git checkout develop

git branch -D <nome da branch padronizada>
	
	exemplo: git branch -D docs/readme

