# Instruções para Desenvolvimento de Página Personalizada e Aplicação no Sistema Conecta

Antes de Começar a Desenvolver o Código.

Siga os passos abaixo para configurar corretamente o seu ambiente de desenvolvimento.

### **Stacks Utilizadas:**

 - **Requisitos Básicos:** HTML e CSS

 - **Requisitos Avançado:** Conhecimento em Framework Bootstrap [Documentação do Bootstrap 5.3](https://getbootstrap.com/docs/5.3/getting-started/introduction/)



## 1 - Alterar Variáveis no Arquivo `index.html`

Substitua as variáveis conforme as opções listadas abaixo.

### **Dominio:**
  - **seu_dominio**: Esse domínio pode ser o criado no Sistema Conecta ou o seu próprio domínio.  
    Exemplo: `https://seu_dominio.digisatconecta.com.br/`

    #### **Opção 1** - Mudar apenas o domínio criado no Sistema Conecta:
    - De: `seu_dominio = lojainformatica`
    - Para: `https://www.lojainformatica.digisatconecta.com.br/`

    #### **Opção 2** - Mudar para um domínio próprio:
    - De: `https://seu_dominio.digisatconecta.com.br/`
    - Para: `https://www.lojainformatica.com.br`

### **Assets/Galeria**
  - **assets/galeria/**: Para importar arquivos localmente na mesma pasta do projeto `index.html`.

    #### **Opção 1** - Importar arquivos/imagens via CDN do Conecta:
    - De: `assets/galeria/`
    - Para: `https://www.cdnconecta.com.br/ftp/tenants/seu_tenant/imgs/galeria/`

      Onde `seu_tenant` é o domínio criado no Sistema Conecta (e.g., `lojainformatica`).

      #### **Como acessar a galeria no Conecta**:
      1. Acesse `admin/tenant_catalogo/banner/`.
      2. Clique em `+Banner`.
      3. Escolha `Minhas imagens`.
      4. Selecione e envie o arquivo de imagem desejado.
      5. Ao clicar na imagem, o link será exibido no formato:
        `https://www.cdnconecta.com.br/ftp/tenants/preview/imgs/galeria/banner_desktop.jpg`.

    #### **Opção 2** - Importar arquivos/imagens via link externo:
    - De: `assets/galeria/nome_do_arquivo.png`
    - Para: `https://images.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png`

### **Substituições de Informações da Empresa:**
  - **nome_da_sua_empresa**: Substitua pelo nome da sua empresa.
  - **descricao_da_sua_empresa**: Substitua pela descrição da sua empresa.
  - **seu_telefone**: Substitua pelo número de contato ou WhatsApp da sua empresa.
  - **seu_email**: Substitua pelo e-mail de contato da sua empresa.



## 2 - Estrutura do Arquivo para Desenvolvimento `index.html`

Após realizar as configurações acima, dentro das tags `<body>`, você pode começar a desenvolver sua página.

### **Exemplo:**

```html
<body>

<!--Sua Páginas desenvolvida aqui-->

  <!-- Apagar este código para ficar limpo sua página -->
  <section class="d-flex" style="height: 100vh;">
    <div class="m-auto text-center">
        <h5 class="mb-5">Aqui é o local onde você pode desenvolver sua página personalizada.</h1>
        <div class="row g-5">
            <div class="col-md-6">
                <img src="assets/galeria/conecta_dark.png" alt="" style="width: 10rem;;">
            </div>
            <div class="col-md-6">
                <img src="assets/galeria/digisat_dark.png" alt="" style="width: 10rem;;">
            </div>
        </div>
    </div>
  </section>
  <!-- Até aqui -->

<!--Final da sua Páginas desenvolvida aqui-->

</body>
```


## 3 - Preparar aplicação para o Sistema Conecta `index.html`

Após desenvolver todo o aquivo `index.html` deve seguir os seguintes passos.

### **Comentar as linhas:**
  - **Bootstrap porque o sistema já importa o framework globalmente**:
    - linha: `<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous">`

  - **Style.css porque vai copiar tudo que tem nele e colar na tag <style></style> que mostra no exemplo**:
    - linha: `<link rel="stylesheet" href="assets/css/style.css">`

  - **Jquey porque o sistema já importa o framework globalmente**:
    - linha: `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>`

  - **Bootstrap porque o sistema já importa o framework globalmente**:
    - linha: `<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js" crossorigin="anonymous"></script>`

  - **Fontawesome porque o sistema já importa o framework globalmente**:
    - linha: `<script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/js/all.min.js" crossorigin="anonymous"></script>`


### **Exemplo:**

```html
<!-- <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous"> -->
<!-- <link rel="stylesheet" href="assets/css/style.css"> -->
<!-- Até aqui -->

  <style>
    /* Copiar e Colar aqui todo o style que estiver em assets/css/style.css entre as tags style */

    html {
        scroll-behavior: smooth;
    }
    body {
        font-family: "Roboto Condensed", sans-serif;
    }
  </style>
</head>

<body>

<!--Sua Páginas desenvolvida aqui-->

  <!-- Apagar este código para ficar limpo sua página -->
  <section class="d-flex" style="height: 100vh;">
    <div class="m-auto text-center">
        <h5 class="mb-5">Aqui é o local onde você pode desenvolver sua página personalizada.</h1>
        <div class="row g-5">
            <div class="col-md-6">
                <img src="assets/galeria/conecta_dark.png" alt="" style="width: 10rem;;">
            </div>
            <div class="col-md-6">
                <img src="assets/galeria/digisat_dark.png" alt="" style="width: 10rem;;">
            </div>
        </div>
    </div>
  </section>
  <!-- Até aqui -->

<!--Final da sua Páginas desenvolvida aqui-->


<!--Recomendaval comentar as abaixo até button scroll top, antes de copiar para o sistema conecta-->
<!-- <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script> -->
<!-- <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js" crossorigin="anonymous"></script> -->
<!-- <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/js/all.min.js" crossorigin="anonymous"></script> -->
<!-- Até aqui -->
```


## 4 - Aplica código HTML no Sistema Conecta `index.html`

Após desenvolver todo o aquivo `index.html` e comentar as linhas sugeridas no 3º passo da documentação deve copiar todo o código html para colar no Sistema Conecta.

### **Acessar Painel Administrativo:**
  - **1. Acesse**:
    - `admin/tenant_core/paginapersonalizada/`
  - **2. Clique em**:
    - `+Página Personalizada`
  - **3. Inserir o seguintes campos:**:
    - Url: `Endereço de acesso da página (Recomendação: /home/)`
    - Título: `nome da página`
    - Ordem de apresentação: `opcional`
    - Pública: `opcional ativo ou não`
    - Página inicial: `opcional ativo ou não`
    - Header: 
      - `Em branco = Toda a página html em branco.`
      - `Modelo Institucional = Com o menu no modelo Institucional do template que foi selecionado`
      - `Modelo Loja = Com o menu do E-commerce do template que foi selecionado`
    - Footer: 
      - `Em branco = Toda a página html em branco.`
      - `Modelo Institucional = Com o menu no modelo Institucional do template que foi selecionado`
      - `Modelo Loja = Com o menu do E-commerce do template que foi selecionado`
    - Conteúdo: 
      - `É onde vai colar todo o código html desenvolvido do aquivo index.html`
  - **4. Após seguir todos esses passos basta apenas salvar e visitar a página para visualização**: