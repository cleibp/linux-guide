<h1 align="center"> 🚀 Linux </h1>

# DEFINIÇÃO

Linux é um termo popularmente empregado para se referir a sistemas operativos ou sistemas operacionais que utilizam o núcleo Linux. O núcleo (ou kernel, em inglês) foi desenvolvido pelo programador finlandês Linus Torvalds, inspirado no sistema Minix. O seu código-fonte está disponível sob a licença GPL (versão 2) para que qualquer pessoa o possa utilizar, estudar, modificar e distribuir livremente de acordo com os termos da licença.[6] A Free Software Foundation e seus colaboradores recomenda[7] o nome GNU/Linux para descrever o sistema operacional GNU, como resultado de uma disputa controversa entre membros da comunidade de software livre e código aberto.

# DIRETÓRIOS
* raiz (/)
* Binários executáveis: /bin (cp, mv, ping e grep)
* Binários do sistema: /sbin (ifconfig, fdisk)
* Programas diversos: /usr
* Configurações do sistema: /etc
* Bibliotecas: /lib
* Opcionais: /opt
* Aquivos pessoais: /home
* Inicialização: /boot
* Volumes e mídias: /mnt e /media
* Serviços: /srv
* Arquivos de dispositivos: /dev (usb)
* Arquivos variáveis: /var
* Processos do sistema: /proc
* Arquivos temporários: /tmp

# COMANDOS

* *Cancela comando*
~~~
CTRL + C 
~~~

* *Autocompletar*
~~~
tab
~~~

* *Retorna comandos anterior*
~~~
Seta para cima e seta para baixo
~~~

* *Vários comandos juntos*
~~~
date; cal
~~~

* *Sistema*
~~~
uname
~~~

* *Mostrar manual de um comando*
~~~
man echo
~~~

* *Calendario*
~~~
cal
~~~

* *Data*
~~~
date
~~~
~~~
date "+%d de %B de %Y"
~~~

* *Hora*
~~~
time
~~~

* *Retorna os últimos 1000 comando no console*
~~~
history
~~~

* *Abrir com terminal e em background*
~~~
firefox &
~~~

* *Caminho atual*
~~~
pwd
~~~

* *Entrar ou sair de um diretório*
~~~
cd
cd ..
cd / (raiz)
cd enter (diretório padrão)
~~~

* *Listar o conteúdo de um diretório*
~~~
ls
ls -l (lista mostrando os tipos)
ls -la (lista mostrando os tipos e quem esta oculto
começa com d = diretório
começa com l = link
começa com - = arquivo
~~~

* *Limpar a tela do console*
~~~
clear
~~~

* *Criar arquivo com texto*
~~~
touch arquivo.txt
> teste01
~~~

* *Criar pasta*
~~~
mkdir pasta
~~~

* *Renomear ou Mover*
~~~
mv message.txt message2.txt
~~~

* *Remover pasta*
~~~
rm -rf pasta
~~~

* *Copiar de caminho para outro*
~~~
cp minhapasta1/message.txt minhapasta2
~~~

* *Mostra o conteudo de um arquivo*
~~~
cat arquivo
echo conteudo > arquivo
~~~

* *Imprime as linhas iniciais*
~~~
head bemvindo.txt
head -n 3 bemvindo.txt
~~~

* *Imprime as últimas linhas*
~~~
tail bemvindo.txt
tail -n 3 bemvindo.txt
~~~

* *Calculadora*
~~~
bc
2+2
sqrt(81)
~~~

* *Exibir os dados de IP*
~~~
ifconfig
~~~

* *Criar usuário*
~~~
adduser teste
~~~

* *Criar senha*
~~~
passwd teste
~~~

* *Acessar o usuário*
~~~
su teste
~~~

* *Remover o usuário*
~~~
deluser teste
~~~

* *Exibir o conteudo desse arquivo*
~~~
cat /etc/passwd
tac arquivo (mostra o conteúdo com as linhas invertidas)
~~~

* *Mostrar o conteudo desse arquivo no editor NANO*
~~~
nano /etc/network/interfaces
~~~

* *Arquivo de um comando*
~~~
which man
~~~

* *Rede*
~~~
netstat -nlpt
~~~

* *Atualizar repositório*
~~~
apt-get update
~~~

* *Atualizar repositório*
~~~
apt-get upgrade
~~~

* *Mostra qual é meu usuario*
~~~
whoami
~~~

* *Informações do linux*
~~~
uname -s -r
~~~

* *Permissão*
~~~
chmod 777 arquivo.txt

Chow cleiton: cleiton arquivo.txt
~~~

* *Dono*
~~~
chow -R 777 * .
~~~

* *Listar processo*
~~~
top
~~~

* *Matar processo*
~~~
kill -9 98989
~~~

* *Tempo de atividade do sistema*
~~~
uptime
~~~

* *Comprimir*
~~~
zip bemvindo.zip *.txt
~~~

* *Descomprimir*
~~~
unzip bemvindo.zip
~~~

* *Print*
~~~
echo "Bem vindo" > bemvindo.txt
$PATH,  $?, PS1
~~~

* *Reiniciar*
~~~
sudo shutdown -r now
reboot
~~~

* *Desligar*
~~~
shutdown -h now
shutdown -h minutos
shutdown -h 1 (vai desligar em 1 minuto)
halt
init 0
telinit 0
last reboot
~~~

# SHELL SCRIPT

Shell script é o nome dado a um arquivo que será interpretado por algum programa tipo Shell. Atualmente existem vários programas tipo Shell. Além dos principais - sh e bash -, existem também, ksh, zsh, csh e tcsh. Um Shell script (ou script em Shell) necessita basicamente do interpretador Shell.

Para selecionar qual Shell será utilizado, use a combinação de hashtag (#) mais exclamação (!) e caminho do executável na primeira linha do arquivo script, isso vem a ser conhecido como Shebang.

* *Para declarar que o script deve ser interpretado por Bourne Shell (sh) a primeira linha será escrita da seguinte forma*
~~~
#!/bin/sh
~~~

* *Para declarar que o script deve ser interpretado por Bourne-Again shell (Bash) é recomendável a utilização do comando env, pelo fato que apesar de o Bash já vir instalado em muitas distribuições Linux, não sabemos se estará em todas elas no mesmo diretório /bin/, então use a seguinte formaa*
~~~
#!/usr/bin/env bash
~~~

* *Comentários*
~~~
#Comentário
#- Segundo comentário
# // [ Terceiro comentário ] //
~~~

* *Variáveis*
~~~
MENSAGEM_DATA=1979
MENSAGEM_NOME="Bourne Shell"
mensagem_tipo1="Unix Shell"
mensagem_autor="Stephen Bourne"
MENSAGEM=ola
_MENSAGEM2=oi-2.020
~~~

* *Variáveis Pré-definidas*
~~~
$? - Armazena o status de saída do último programa executado;
$# - Armazena a quantidade de parâmetros de linha de comandos;
$$ - Armazena o valor PID (Process Identifier) do script em shell que estiver em execução;
$@ - Armazena o valor de todos os parâmetros passados, similar a variável argv presente nas linguagens de programação C e C++;
$! - Armazena o PID do último processo em segundo plano. Isso é útil para acompanhar o processo à medida que o trabalho é realizado;
$0, ..., $9 - Armazena os valores de todos os parâmetros de linha de comando separadamente;
~~~

* *Variáveis Globais*
~~~
Variáveis globais ou variáveis de ambiente globais, são variáveis criadas/definidas com o comando export e podem ser utilizadas por múltiplos scripts em Shell. Um exemplo é a variável de ambiente LANG (Pré-definida em diversas distribuições Linux), Podendo ser acessada por diversos arquivos de script em Shell.

Outras variáveis pré definidas são:

PATH: define diretórios de procura por programas executados no shell;
USER: informa o nome do usuário do shell;
HOME: informa o caminho do diretório home do usuário;
LANG: Idioma/Linguagem, especificada como locale;
PWD: diretório atual;
TERM: Tipo de terminal atual em uso.
UID: UID do usuário atual.
RANDOM: Gera um número aleatório
~~~

* *Criando variáveis e imprimindo*
~~~
variavel= “ola”
echo "$variavel"
~~~

* *Lendo variáveis*
~~~
read teste
echo "foi $teste"
~~~

* *A duas formas de criar uma variável global, exportar uma variável pré definida ou definir quando for exportar*
~~~
VARIAVEL1=Teste
export VARIAVEL1
# Define e exporta com export
export VARIAVEL2=Teste
~~~


* *Array*
~~~
#!/usr/bin/env bash
meu_array=(1 2 3 4 5 6 7 8 9)
meu_Array=("abc" "def" "ghi")
~~~

* *Array Associativo*
~~~
#!/usr/bin/env bash
declare -A dicionario
dicionario["Brasil"]="Brasília"
dicionario["Goiás"]="Goiânia"
dicionário["São Paulo"]="São Paulo"
dicionario[Sergipe]=Aracajú
echo ${dicionario["Brasil"]}
~~~

* *Remover Variáveis*
~~~
unset VAR
unset VAR1 VAR2 VAR3 VAR4
~~~


* *Criar uma variável, ${var} é o mesmo que $var, porém não ambíguo.*
~~~
var="cleiton"
echo $var
~~~

* *Retornar o tamanho da string*
~~~
echo ${#var}
~~~

* *Executa o conteúdo de $var (igual ‘eval $$var’)*
~~~
echo ${!var}
~~~

* *Retorna os nomes de variáveis começadas por ‘U’*
~~~
echo ${!U*}
UID USER USERNAME
~~~

* *Retorna o texto a partir da posição 7’*
~~~
echo ${var:7}
~~~

* *Retorna 8 caracteres a partir da posição 11’*
~~~
echo ${var:11:8}
~~~

* *Operadores*
~~~
-lt <
-gt >
-le <=
-ge >=
-eq ==
-ne !=
~~~

* *IF*
~~~
if [ $3 ]; then
    echo "$3"
elif [ $2 ]; then
    echo "$2"
else
    echo "$1"
fi
~~~
~~~
read nota
if ("$nota" -ge "6")
then
echo "passou"
else
echo "rodou"
fi
~~~

* *CASE*
~~~
case "$var" in
    valor)
    ;;
esac
~~~
~~~
echo -n "Digite um numero entre 1 a 9"
read NUMERO
case $NUMERO in
	1 | 3 | 5 | 7 | 9) echo "Seu numero $NUMERO e impar";;
	2 | 4 | 6 | 8) echo "Seu numero $NUMERO e par";;
	*) echo "Precisa ser entre 1 a 9";;
esac
~~~


* *WHILE*
~~~
i = 0
while [ $i -lt 4]
do
	echo $i
	i = $[$i+1]
done
~~~

* *FOR*
~~~
for i in ${seq 1 10}
do
echo "$1"
done
~~~

* *Funções*
~~~
# Ambos aceitam esse formato
minha_função(){
    echo
}
# Esse formato apenas Bash aceitará
function minha_função(){
    echo
}
~~~

* *Exemplos*
~~~
 #!/bin/bash
   # sistema - script que mostra informações sobre o sistema
   # Autor: Fulano da Silva
   # Pede uma confirmação do usuário antes de executar
   echo "Vou buscar os dados do sistema. Posso continuar? [sn] "
   read RESPOSTA
   # Se ele digitou 'n', vamos interromper o script
   test "$RESPOSTA" = "n" && exit
   # O date mostra a data e a hora correntes
   echo "Data e Horário:"
   date
   echo
   # O df mostra as partições e quanto cada uma ocupa no disco
   echo "Uso do disco:"
   df
   echo
   # O w mostra os usuários que estão conectados nesta máquina
   echo "Usuários conectados:"
   w
   

   prompt$ testa-arquivos
   Digite o arquivo: /naoexiste
   O arquivo '/naoexiste' não foi encontrado
   prompt$ testa-arquivos Digite o arquivo: /tmp /tmp é um diretório
   prompt$ testa-arquivos Digite o arquivo: /etc/passwd /etc/passwd é um arquivo
   
   
   #!/bin/sh
   # argumentos - mostra o valor das variáveis especiais
   echo "O nome deste script é: $0"
   echo "Recebidos $# argumentos: $*"
   echo "O primeiro argumento recebido foi: $1"
   echo "O segundo argumento recebido foi: $2"
   
   prompt$ ./argumentos um dois três
   O nome deste script é: ./argumentos 
   Recebidos 3 argumentos: um dois três 
   O primeiro argumento recebido foi: um O segundo argumento recebido foi: dois

~~~

# VIM/VI

Vim (uma contração de Vi IMproved, em português Vi Melhorado) é um clone do programa editor de textos vi para Unix de Bill Joy. Foi escrito por Bram Moolenaar baseado na fonte para um porte do editor Stevie para o Amiga com a primeiro lançamento público em 1991. O Vim é destinado para uso a partir tanto de uma interface de linha de comando como uma aplicação isolada em uma interface gráfica de usuário. É um software livre e de código aberto e é lançado sob uma licença que inclui algumas cláusulas de caridade, encorajando os usuários que se juntarem ao software a considerar a doação para crianças da Uganda. A licença é compatível com a GNU General Public License por meio de uma cláusula especial permitindo a distribuição de cópias modificadas "sob a GNU GPL versão 2 ou qualquer versão posterior".



* *COMANDOS Abrir o arquivo*
~~~
vim arquivo.txt
~~~

* *Abrir o arquivo e colocar o cursor no fim*
~~~
vim arquivo.txt + 
~~~

* *Abrir o arquivo e colocar o cursor na linha 8*
~~~
vim arquivo.txt +8
~~~

* *Abre na linha que tiver bsd*
~~~
vim arquivo.txt +/bsd
~~~

* *Abre vários arquivos*
~~~
vim -o arquivo.txt arquivo2.txt
~~~

* *Salvar arquivo*
~~~
esc : w 
~~~

* *Sair*
~~~
esc : q
~~~

* *Salvar e sair*
~~~
esc : w q
:x
zz
~~~

* *Sair sem salvar*
~~~
esc : q!
~~~

* *Salvar*
~~~
esc : set autowrite
:set aw
~~~

* *Desfaz*
~~~
esc v
~~~

* *Salva tudo aberto*
~~~
esc : w a
~~~

* *Salva e sai de todos*
~~~
esc : wqa
~~~

* *Fim da linha*
~~~
esc $
~~~

* *Inicio da linha*
~~~
esc ^
~~~

* *Fim do arquivo*
~~~
esc :$ (dois pontos cifrao)
esc G
~~~

* *Inicio do arquivo*
~~~
esc gg
~~~

* *Linha 8*
~~~
esc :8
esc 8G
~~~

* *Pula para próxima palavra*
~~~
esc w
~~~

* *Pula para palavra anterior*
~~~
esc b
~~~

* *Pula para frase anterior*
~~~
esc [
~~~

* *Pula para frase posterior*
~~~
esc ]
~~~

* *Pula para paragrafo anterior*
~~~
esc {
~~~

* *Pula para paragrafo posterior*
~~~
esc }
~~~

* *Pesquisar palavra linux*
~~~
esc /linux
~~~

* *Insere na onde está*
~~~
esc i
~~~

* *Insere após a posição*
~~~
esc a
~~~

* *Insere nova linha após*
~~~
esc o
~~~

* *Insere nova linha após*
~~~
esc o
~~~

* *Insere reescrevendo*
~~~
esc r
~~~

* *Para cima*
~~~
esc K
~~~

* *Para direita*
~~~
esc l
~~~

* *Para esquerda*
~~~
esc h
~~~

* *Para baixo*
~~~
esc j
~~~

* *Seleciona o paragrafo*
~~~
esc shift v
~~~


## Contatos

[![Github Badge](https://img.shields.io/badge/-Github-000?style=flat-square&logo=Github&logoColor=white&link=https://github.com/cleibp)](https://github.com/cleibp)
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/cleitonpaiva/)](https://www.linkedin.com/in/cleitonpaiva/)
[![Whatsapp Badge](https://img.shields.io/badge/-Whatsapp-4CA143?style=flat-square&labelColor=4CA143&logo=whatsapp&logoColor=white&link=https://api.whatsapp.com/send?phone=5516988368457&text=Ola!)](https://api.whatsapp.com/send?phone=5516988368457&text=Ola!)
[![Gmail Badge](https://img.shields.io/badge/-Gmail-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:cleibp@gmail.com)](mailto:cleibp@gmail.com)

[Pague-me um ☕](https://www.buymeacoffee.com/cleibp)

Feito com muito ❤️☕👨🏻‍💻 por Cleiton Paiva

