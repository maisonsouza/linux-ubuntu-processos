

# Anotações do Curso de Linux II: Programas, processos e pacotes

![](https://www.alura.com.br/assets/api/share/curso-linux-ubuntu-processos.png)
## [Link do Curso](https://cursos.alura.com.br/course/linux-ubuntu-processos)

### kill,ps,grep.
* Podemos executar programas no terminal
* ps -e para visualizar os processos.
* kill `<id do processo>` para matar um processo, mas dá uma chance ao programa.
* kill -9 `<id do processo>` para matar o processo sem dar chance para o programa.
* ps -el para mostrar mais informaçes sobre o programa
* grep filtra resultados em arquivos e identificar processos.

### killall, top.
* top gerenciador de tarefas do Linux.
* killall `<Nome do processo >` para matar o processo e associados.

### jobs,bg,pstree, &.
* Quando executamos um programa direto do terminal ele trava o terminal.
* pstree para verificar os processos listados como árvore.
* Ctrl + Z para parar o processo temporariamente
* jobs para verificar os processos que estão parados ou rodando em background ou foreground.
* bg `<Nome do processo>` ou bg `<Numero do job>` para rodar em background.
* fg `<Nome do processo>` ou fg `<Numero do job>` para rodar em foreground.
* & significa (rodando em background).
* Ctrl + c para encerrar o processo
* `<Nome do processo>` & para rodar o processo em background.
* ./script para executar ./(diretório atual)

### Scripts e permissões de execução: sh e chmod.
* O bash permite criar scripts
* Para executar um script utilizamos sh na frente.
* Permissões de arquivo no linux (r-read,w-write,x-execucao).
* As permisses podem ser para o (dono, grupo, qualquer usuário)
* chmod para adicionar ou retirar permissões.

### Procurando arquivos:locate e updatedb.
* locate para pesquisar um arquivo.
* Armazena informaçes sobre os arquivos em um banco de dados.
* updatedb para atualizar o banco de dados interno.
* sudo para executar como root, ele pedirá a senha.

### Trocando de usuários: sudo e su.
* root é o usuário com todas as permissões.
* Evitar tá passando senha de root.
* sudo para executar operações que exigem root.
* passwd para mudar senha do usuario.
* sudo passwd par mudar a senha do root.
* Programas que estão em /usr/bin executam sem sh.
* su `nome do usuario` Para logar como outro usuario.
* whoami para verificar o nome do usuario ativo.

### Novos usuários e controle de acesso: adduser e chmod.
* sudo adduser para adicionar um novo usuario.
* su `nome do usuario` Para logar como outro usuario.
* root troca para qualquer usuário sem pedir senha.
* No ubuntu eu consigo acessar os diretórios dos usuários.
* chmod u-rwx para retirar permissões do usuário, g-rwx para permissões de grupo, e o-rwx para permisses de outros.

### Variáveis de ambiente e o Path.

* Quando executamos o comando `env`, podemos ver quais são as variáveis que estão definidas

* A variável `HOME`, por exemplo, guarda o caminho para o diretório do usuário.

* A variável `PATH`, guarda informações de onde estão nossos arquivos executáveis para que possamos executar um comando sem a necessidade de digitar o caminho absoluto.

* ``gedit .bashrc & para adicionar no PATH``

* `PATH=$PATH:/home/seuUsuario/workspace`

### Instalação de programas: apt.

- `apt-get install`: instala um programa dado o nome
- `apt-get remove`: desinstala um programa dado o nome
- `apt-get update`: busca uma lista das versões atualizadas dos programas
- `apt-cache search`: procura os programas disponíveis para instalação

### Instalando novos programas:dpkg.

1. Via *apt*: quando o programa já está disponibilizado na central do Sistema Operacional Linux.
2. Via *dpkg*: quando baixamos pelo navegador da internet um pacote *.deb* do programa.

Instalar

```
sudo dpkg -i [nome do pacote]
```

Desinstalar

```
sudo dpkg -r [nome do pacote]
```

### Scripts de inicialização e serviços do sistema.



### Compilando a partir do código fonte: Make e Git.
### Acesso remoto com ssh e scp.
