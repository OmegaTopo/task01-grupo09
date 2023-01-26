# task01-grupo09

___

## Repositório para documentação da task do Vem Ser -

### Funcionamento, sintaxe e aplicação do comando git rebase:

git rebase é o comando para transferir branches de um branch específico para outro branch ou direto para o main, serve também para unificar diversos commits em somente um commit.

A sintaxe é: ``` git rebase <branch que vai ser o alvo do rebase> ```

É possível fazer também da seguinte forma: git rebase main feat-atualizacao - sendo main a base principal e feat-atualizacao a base que vai ser transferida.

Também é possível utilizar o comando --onto para indicar diretamente qual a base que vai ser o alvo da rebase. o comando ficaria assim: ``` git rebase --onto <newbase> ```
___

### Funcionamento, sintaxe e aplicação do comando git cherry-pick:

Em um dado número de commits existentes em um branch, esse comando aplica as mudanças de cada um no branch atual, criando novos commits para cada um deles. Cherry pick pode ser útil para corrigir erros de commit como, por exemplo, criar mudanças em uma ramificação errada.


Sua sintaxe é: ``` git cherry-pick [options] <commit(s)> ```

##### Exemplos
``` git cherry-pick master~4 master~2 ``` 

Aplica as mundanças do quinto e terceiro ultimos commits do branch master e cria dois commits.

``` git cherry-pick master ```

Aplica as mundaçãs introduzidas pelo commit no topo do branch master (HEAD) e cria um novo commit com essa mudança.


___
### Funcionamento, sintaxe e aplicação do comando git revert:

Revert serve para reverter as mudanças de um ou mais commits e gravar novos commits. Não é o mesmo comando do que se quiser descartar as mudanças que não foram commitadas, comando esse que seria o git reset.

A sintaxe é: ``` git revert ```

É possível utilizar o git revert com a chave exata do commit que se deseja reverter ou utilizando o HEAD na seguinte forma:

``` git revert HEAD~<numero_do_commit> ```

Sendo o <numero_do_commit> substituído pelo número do commit que se deseja reverter sendo o último commit o número 1, o penúltimo sendo o 2 e assim por diante.

Caso haja algum erro durante a reversão, é possível cancelar a operação utilizando o comando:

```git revert --abort ```

___

### Funcionamento, sintaxe e aplicação do comando git squash:

Diferente dos já mencionados, **squash**, não se trata propriamente de um dos comandos do Git, invés disso, é um procedimento que a ferramente provê para a junção de N commits em uma única mudança. Seu uso é através do comando ``` git rebase ```, que ao usar a opção do fluxo interativo (```-i```), nos leva ao nosso editor de preferência listando os commits realizados com suas respectivas indetificações.

##### Exemplo
```git rebase -i HEAD~3 ```

Irá nos redirecionar para um editor de texto com o log dos 3 últimos commits:
```vim
pick dc97841 commit1
pick 716da3d commit2
pick 90987ff commit3
```
E caso desejemos uni-los, basta trocar o comando previamente imposto ```pick``` por ```squash```, dessa forma:

```vim
pick dc97841 commit1
squash 716da3d commit2
squash 90987ff commit3
```
Então salvamos o arquivo para persistir as mundanças no git.

##### Referências:

https://git-scm.com/docs/git-revert

https://git-scm.com/docs/git-rebase#Documentation/git-rebase.txt---skip

https://git-scm.com/docs/git-cherry-pick
