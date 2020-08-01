## Veja o meu passo a passo neste projeto Angular:


0. Criei um projeto backend:
   - Iniciei projeto com `npm init -y`
   - Instalei json-server com `npm i json-server`
   - Criei db.json contendo alguns produtos
   - Iniciei a API com `npm-start` e fiz requisições ao link em _Resources_

1. Criei o frontend:
   - (sudo) npm i -g @angular/cli
   - `ng new frontend --minimal` (flag minimal remove arquivos que não usarei nesse projeto simples)
     - Respondi perguntas: usar rotas? yes; qual das opções? css
   - Testei o frontend criado com `npm start` e abrindo o localhost/porta informado

2. Decorrente da flag `--minimal`, os html, css e js estavam em um só arquivo. Para evitar isso:
   - Alterei em angular.json:
     - `"inlineTemplate": false,` (html...
     - `"inlineStyle": false,` ... e css em arquivos separados)
   - Então em src/app/app.component.ts removi `template` e `styles`
     - Substituí isso por: `templateUrl: 'app.component.html'`
     - Criei arquivo src/app/app.component.html
     - Testei digitando algo para refletir na aplicação em localhost

3. Instalei os Componentes do Material
   - Antes de instalar é necessário parar a aplicação do angular
   - `ng add @angular/material`
     - Pergunta-se: qual estilo de cores / tipografia (yes) / animação (yes)

4. Criei componente _header_ em components/template/:
   - `ng g c components/template/header` (ou `ng generate component components/template/header`)
   - Em app.module.ts importei o componente MatToolbarModule do Material Design
     - `import { MatToolbarModule } from  '@angular/material/toolbar'`
     - inseri a referência em imports, para que outros módulos também possam usá-lo
   - Voltarei ao componente _header_, para ele usar o mat-toolbar