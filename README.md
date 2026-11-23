Alunos  Gabriel Benetti Berno    GRR20221553<br>
        Rafael Garcia Cerci      GRR20234604

**#1 MeuDiário**<br>
Arquivos do App Meu Diário, para registro pessoal de humor e registro de sentimentos. 
Nosso objetivo é contribuir com sua saúde mental através da reflexão, auxiliando você a reconhecer suas emoções e identificar as causas dos sentimentos através do Diário de Emoções, e acompanhamento da sua atividade pelo Relatório de Emoções.<br>
Indicado para pessoas desejam um desenvolvimento pessoal e emocional.<br>
Contém os arquivos de projeto da API, e da Aplicação ReactNative.<br>

**#2 Tecnologias**<br>
Banco de Dados postgres para persistência de dados.<br>
Aplicação api - Biblioteca Express para tratamento de requisição e respostas HTTP.<br>
              - Biblioteca bcryptjs para criação de hashes.<br>
              - Biblioteca pg para comunicação com o banco Postgres.<br>
              - Biblioteca jsonWebToken para gerenciamento da sessão de usuários.<br>
Aplicação React - Framework React v19 e ReactNative v0.88.1 para tecnologia de Interfaces.<br>
                - Bibliotecas Platform para detectar a plataforma do dispositivo du usuário.<br>
                - Bibliotecas UseEffect, UseState para comunicar dados a interface, troca de telas.<br>
                - Bibliotecas StyleSheet, Text, View para formatação do estilo e exibição dos componentes.<br>
                - Biblioteca SecureStore para guardar tokens.<br>
                - Biblioteca SafeAreaContext v5.11.<br>
                - Biblioteca Expo v58 para criação e gerenciamento de interfaces Web e Mobile.<br>

**#3 Arquiteturas**<br>
Api divididas em Controllers, Models, Routes. Arquivos de confiuração em "config".
APP segue arquitetura MVC, com Models, Controlers, Views separanndo informaçãoes e organizando o projeto para manutenção futura.

**#4 Execução da Aplicação**<br>
#### Executando backend
Para que a API funcione, é preciso criar Banco de Dados "diarioBD", utilizamos postgres.

Dentro do DBEaver, no usuário principal "postgres", clique botão direito sobre "Banco de Dados" -> "Criar novo Banco de Dados".
Coloque o nome "diarioBD", com opção de modelo "template0".
Crie uma nova conexão de Banco de dados, com o Database "diarioBD", e cole o Script de criação.

Copie o arquivo ".env API" para dentro da pasta diario-api, e renomeie para ".env", e coloque o USUARIO e SENHA do Administrador do banco de dados na linha 6.
Execute os comandos: 
```
npm install
npm run dev
```

#### Executando Aplicação<br>
Favor descompactar arquivo "diario-app.zip", não consegui upar a pasta.
Copie o arquivo ".env App" para dentro da pasta diario-app, e renomeie para ".env", e coloque o IP da sua máquina local na linha 9.
Execute os comandos:
```
npm install
npx expo start -c
```

**#5 Geração de APK**<br>
Execute os comandos
```
npm install -g eas-cli
eas login
```
    -> cria uma conta ou faça login no site do Expo.
```
eas build:configure
```
    -> selecione as plataformas
    -> edite o arquivo eas.json, definindo o perfil "preview" dentro de "build".
{
  "build": {
    "preview": {
      "android": {
        "buildType": "apk"
      }
    }
  }
}

```
eas build -p android --profile preview
```
    -> Se perguntar, deseja criar uma KeyStore agora? Digite Yes
    -> Dica, vai demorar um pouco pra executar, no final aparecerá um link para baixar o arquivo APK.

**#6 Requisitos de Qualidade**<br>
Interface distribuída, sem muitos componentes clicáveis perto um do outro.
Separação das camadas da arquitetura é uma boa prática para manutenção dos projetos.

**#7 Requisitos de segurança e proteção de dados adotados**<br>
O banco de dados não guarda a senha do usuário, ele guarda um hash da senha.
API configurada com Token de acesso, para controle de sessão, dificultando acesso de pessoas não autorizadas.
Usuário consegua acessar apenas informações de seu próprio ID, implementado na Aplicação.
Usuário deve permitir a coleta e processamento de suas informações de acordo com a LGPD.
O usuário pode apagar sua própria conta de usuário. Implementado na Aplicação.

**#8 Interface, IHC e UX**<br>
Recomendação 3- Fazer perguntas reflexivas fáceis sobre os registros.
  Tela registro de Emoções com emojis, e pergunta descritiva.

Recomendação 10 - Garantir que o usuário tenha controle e soberania total sobre seus dados.
  Tela Privacidade - O usuário pode apagar os dados da sua conta do aplicativo.

Recomendação 15 - Assegurar conformidade com as diretrizes da LGPD e do GDPR, garantindo privacidade, segurança e transparência no tratamento de dados dos usuários.
  Tela de Cadastro de Usuário, e tela de Privacidade.

Recomendação 47 - Respeitar a autonomia, privacidade e vulnerabilidade emocional dos usuários.
  Tela Aceite dos Termos de Uso, e Tela de Privacidade.
  
Recomendação 51 - Fornecer políticas de privacidade claras e transparentes.
  Tela de Cadastro de Usuário, e tela de Privacidade.
  
Recomendação 85 - Aproveitar o princípio da familiaridade com padrões de design e usabilidade.
  Tela Registro de Emoções, Relatório, e Privacidade.

Recomendação 88 - Registro de humor via escala Likert curta.
  Tela Registro de Emoções

Recomendação 97 - Revelar conexões, padrões, tendencias e comparações entre os registros.
  Tela de Relatório em PDF, com filtro de 7 dias, 30 dias e 90 dias.
  
Recomendações 100 - Utilizar ícones acompanhados de rótulos e textos.
  Tela Registro de Emoções, Personalização de Tema.

**#9 Criatividade**<br>
  Nada

**#10 Divisão do Trabalho**<br>

Membro     Telas     Código do aplicativo(React Native)     Código das APIs,BD       Itens do documento
Gabriel    Login                                              Estrutura Banco         Itens de Segurança
        Cadastro Usuario                                          API               Requisitos de Qualidade


Rafael    Diário             Visualização e Ajustes                                    Execução do App
          Relatório            GitHub                                                 Geração de APK       
          Privacidade
        Personalizar Tema
<br>
        
Tela Inicial do APP. (https://drive.google.com/file/d/14pz9AQ6r8NnXWRijBnfPTPDp0SNjNYty/view?usp=drive_link)

Tela Registro de Emoção. (https://drive.google.com/file/d/1RmNDxFh1CMD4JkMkriLVrT0Y0EbeJr5a/view?usp=drive_link)

