#Veja meu passo a passo neste projeto Angular:

0 - Criei um projeto backend:
  - 0.1 - Iniciei projeto (npm init -y)
  - 0.2 - Instalei json-server (npm i json-server)
  - 0.3 - Criei db.json com alguns produtos
  - 0.4 - Testei API:
        - npm-start
        - Link de 'Resources'

1 - Criação do frontend:
  - 1.1 - (sudo) npm i -g @angular/cli
  - 1.2 - ng new frontend --minimal (flag minimal para remover arquivos que não usarei nesse projeto)
        - 2 perguntas do comando: yes (usar rotas) & (usar) css
  - 1.3 - Testei frontend criado
        - Na pasta frontend foi criada, executei npm start
        - Entrei no localhost/porta informado

2 - Alterações para não trabalhar com html, css e js em um só arquivo
  - 2.1 - Alterei em angular.json:
        - "inlineTemplate": false, //html e...
        - "inlineStyle": false, //...css em arquivos separados
  - 2.2 - Então em src/app/app.component.ts removi 'template' e 'styles'
        - Substituí isso por: templateUrl: 'app.component.html'
        - Criei arquivo src/app/app.component.html
        - Digitei algo e vi que reflete no site em localhost 
3 - Instalei os Componentes do Material
  - 3.1 - É necessário parar a aplicação do angular
  - 3.2 - ng add @angular/material
        - São feitas algumas perguntas:
	  - Estilo de cores / tipografia (yes) / animação (yes)