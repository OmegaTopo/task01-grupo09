# task01-grupo09

- Repositório para documentação da task do Vem Ser -

⋅⋅* Funcionamento, sintaxe e aplicação do comando git rebase:

git rebase é o comando para transferir branches de um branch específico para outro branch ou direto para o main, serve também para unificar diversos commits em somente um commit.

A sintaxe é: git rebase <branch que vai ser o alvo do rebase>

É possível fazer também da seguinte forma: git rebase main feat-atualizacao - sendo main a base principal e feat-atualizacao a base que vai ser transferida.

Também é possível utilizar o comando --onto para indicar diretamente qual a base que vai ser o alvo da rebase. o comando ficaria assim: git rebase --onto <newbase>
___

⋅⋅* Funcionamento, sintaxe e aplicação do comando git cherry pick:

___

⋅⋅* Funcionamento, sintaxe e aplicação do comando git revert:

Revert serve para reverter as mudanças de um ou mais commits e gravar novos commits. Não é o mesmo comando do que se quiser descartar as mudanças que não foram commitadas, comando esse que seria o git reset.

A sintaxe é: git revert 

É possível utilizar o git revert com a chave exata do commit que se deseja reverter ou utilizando o HEAD na seguinte forma:

git revert HEAD~<numero_do_commit>

Sendo o <numero_do_commit> substituído pelo número do commit que se deseja reverter sendo o último commit o número 1, o penúltimo sendo o 2 e assim por diante.

Caso haja algum erro durante a reversão, é possível cancelar a operação utilizando o comando:

git revert --abort

___

⋅⋅* Funcionamento, sintaxe e aplicação do comando git squash:





Referências:

https://git-scm.com/docs/git-revert
https://git-scm.com/docs/git-rebase#Documentation/git-rebase.txt---skip