 

Primeiro repositório:
Dentro da pasta:  
git init para iniciar um repositório.
git add nome do arquivo para adiconar 
git add .  "Usar Ponto" - todos 

git commit ARQUIVO -m "Uma descrição" //-m usado para add um comentário
git commit // salva tudo, ira abrir um editor para comentar no caso do vim para salva pressionar esc :wq ou :q para sair
git commit -a -m "Uma descrição" //Adiciona automaticamente  sem precisar usar add - comita todos
git status - Mostra se os arquivos estão utilizados ou não
git log - Mostra os comitts
git checkout -- arquivo  - Remover arquivo da lista dos que serão comitados automaticamente. | Ideal: rodar antes de comitar 

Untracked files -arquivo não adiciona
Changes to be committed - arquivo foi adicionadomas falta comitar


git log
git log -p - Mostra os comitts com detalhes de modificações
git log -p -2 - Comando acima exibindo somente a quantidade dos últimos comits
git log --stat - Mostra as linhs alteradas
git log --pretty=oneline - Exibe os conteúdos em uma linha melhorando a formatação
git log --pretty=format:"%h - %an,  %ar : %s "  - Mesmo acima aplicando formatação na data
git log --sing=2.days Mostra os commits de dois dias atras


 Ignorar arquivos ou pastas: criar um arquivo chamado .gitignore e dentro dele o nome dos arquivos para ignorar
Criar um arquivo vazio no terminal: touch arquivo.txt

Para voltar um arquivo que foi adicionado não mas não  comitado:
git reset HEAD arquivo.txt

Voltar para a versão do Hash/id específico: git checkout 'id ou hash ver no git log' 
Volta o número de comites colocados depois do ~    git reset HEAD~1

Mesmo acima deixando os arquivos para serem comitados    git reset HEAD~1 --soft
Volta excluindo os commits posteriores git reset HEAD~1 --hard 


Voltando ao estado original
Vamos imaginar que você possui um arquivo no controle de versão chamado exemplo.php.
Imagine agora que você fez diversas alterações nesse arquivo, porém, por qualquer motivo, você se arrependeu de fazê-las (lembrando que você apenas fez as alterações, mas não as commitou). Para você fazer o conteúdo do arquivo voltar ao estado original, digite:
git checkout -- exemplo.php
Rodando esse comando, todos as alterações realizadas serão perdidas e o arquivo voltará exatamente como estava antes.
Esse recurso é extremamente útil, porém deve ser usado com cuidado.

Branches
git branch - exibe qual branch esta em uso
git checkout -b nome - cria um novo branch
git checkout nomedobranch - vai para o branch desejado
git merge nomedobranch - mescla com o branch em uso
git rebase nomedobranch - alinha conforme commits "Usar Localmente"
O merge não reordena os commits e ainda muitas vezes gera um commit adicional para ser concluído. O rebase reordena os commits, não gerando assim um commit adicional
Removendo um branch
Após uma funcionalidade ser desenvolvida e o merge realizado, você poderá optar por remover o branch. É isso mesmo =)
Remover um branch não significa que você removerá os commits que você realizou, pois o merge já foi feito.
Para remover um branch utilize o comando: git branch -D nome-do-branch
Teste isso agora mesmo em seu computador!

GITHUB
criar uma chave: ssh-keygen
cria uma pasta .ssh com uma chave pública na pasta de usuário
Adicionar Caminho:
git remote add origin https://github.com/brzoski/aulagit.git
Subir o branch master
git push  origin nomedobranch

Clonar
git clone https://github.com/brzoski/aulagit.git  novonome
- Clona trazendo o branch principal
- novonome para o projeto é alternativo
- para ver todos os branches incluindo os remotos usar:  git branch -a
- para adicionar outros branches git checkout -b nomedobranch origin/nomedobranch

git pull mostra se os arquivos estão sinconizados/atualizados
git push origin master atualizar no github
git pull origin master puxa do servidor arquivos atualizados 


create a new repository on the command line
echo "# aulagit" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/brzoski/aulagit.git
git push -u origin master

push an existing repository from the command line
git remote add origin https://github.com/brzoski/aulagit.git
git push -u origin master

PullRequest
Para fazer faz um fork depois um PR pullrequest
