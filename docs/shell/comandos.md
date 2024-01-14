# Comandos

Anotações baseadas na aula 1 do [Missing Semester of CS - MIT](https://www.youtube.com/watch?v=Z56Jmr9Z34Q)

## O que é o shell

bash/shell (ou como conhecemos, o bom e velho terminal) é uma linguagem de programação, ele conhece os comandos, porque os programas responsáveis por eles estão dentro dele. Então você pode loops, funções, etc dentro dele.

## Comandos aleatórios mas interessantes

`date` ⇒ retorna a data do dia.

`echo` ⇒ imprime no terminal o que vem dps dele.

`echo $PATH` ⇒ Esse comando emite todas as pastas que guardam os comandos disponíveis para serem executados no Shell. Quando solicitamos algo, é nessas pastas que ele procura o código responsável pelo comando (se existir).

`which` → Sinaliza de onde está vindo o comando que estamos rodando, exemplo `which aws`, me mostra a pasta onde tá os arquivos da aws que eu rodo no terminal quando chamo o comando.

`cat` ⇒ lê arquivos e exibe o conteúdo no terminal.

`tee` ⇒ além de escrever em arquivos, ele exibe o resultado no terminal.

`tail -n <quantidade de linhas>` ⇒ Imprime as últimas n linhas de um input fornecido a ele (arquivo por exemplo)

## Comandos relacionados a pastas/caminhos

`xdg-open <pasta/arquivo>` ⇒ Necessário instalação no wsl2 ([link aqui](https://askubuntu.com/questions/704712/in-ubuntu-xdg-open-command-is-not-working)), mas você indica o arquivo ou pasta a abrir, e ele abre o mesmo com o aplicativo adequado.

`cd (change directory) <caminho relativo até onde você deseja ir>` ⇒ altera a pasta que você está no momento.

`cd -` ⇒ Te retorna pro diretório que você estava anteriormente.

`ls -l` ⇒ fornece mais informações sobre os diretórios que estamos olhando (arquivos, pastas, permissões, etc).

`pwd (print working directory)` ⇒ exibe o caminho onde você está atualmente (qual pasta).

## Copiar/mover arquivos

`mv <old name of a file/folder> <new name>` - Permite renomear arquivos e pastas.

`copy <old name of a file/folder> <new name>` - Permite renomear arquivos e pastas.

## Remover arquivos/pastas

`rm <caminho>` → você pode remover arquivos. Esse comando não é recursivo, então não consegue apagar pastas.

`rm -rf` ⇒ Permite apagar pastas com coisas dentro (recursivo).

`rmdir <pasta>` ⇒ Permite apagar pastas vazias.

## Para saber mais sobre o comando utilizado

`<comando> —help` ⇒ Fornece informações sobre o comando, para que serve e como utilizar ele.

`man <comando>` ⇒ Fornece informações sobre o comando, utilização semelhante ao `—help` mas com a diferença que é exibido no modo de leitura e não diretamente impresso no terminal.

## Manipular input/output de outros comandos

`|` ⇒ O nome desse símbolo é pipe, basicamente sinaliza para o shell pegar o output da esquerda e usar como input para o que vier na direita.

Exemplo:

`ls -l | tail -n1` ⇒ `ls -l` imprime tudo que tem na pasta, o pipe pega esses dados e joga para o tail, que imprime apenas a última linha.

`<input> **>** <output>` ⇒ Direciona o input gerado na esquerda para dentro do comando executado a direita.

Exemplo:

`echo hello > hello.txt`

Aqui estamos fornecendo para o comando echo a entrada “hello”, e enviando esse input direto para dentro do arquivo hello.txt (se ele não existir, vamos criar um do zero).

`<input> **<** <output>` ⇒ Direciona o output da direita, como um input para o o comando da esquerda.

Exemplo:

`cat < hello.txt`

Basicamente estamos pegando um output (o que está escrito dentro do arquivo) e dizendo para o terminal usar isso como input para o comando cat.

`>>` ⇒ Mesma ideia do comando citado acima, com a diferença que ao invés de causar um overwrite (apagar tudo e substituir pela informação nova) ele dá um append (junta a informação antiga com a nova).

## Sudo e usuário Root

`Sudo <comando que deseja realizar>` → Comando para poder executar algum outro comando como usuário root (com todas as permissões). Sudo basicamente significa Superuser Do.

`#` ⇒ É usado no terminal para indicar que você está executando as coisas como root user.

`sudo su` ⇒ Troca o terminal pra modo root, você roda tudo como usuário root e pode fazer tudo. Usar com cautela.
