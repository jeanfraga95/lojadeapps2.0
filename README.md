# Loja de Apps Android

Uma loja de aplicativos Android completa com sistema de autenticação, upload de APKs e avaliações.

## Funcionalidades

### Para Usuários
- ✅ Sistema de cadastro e login
- ✅ Busca de aplicativos por nome
- ✅ Visualização de detalhes do aplicativo
- ✅ Download de APKs
- ✅ Sistema de avaliação (1-5 estrelas) com comentários
- ✅ Carrossel com aplicativos recentes na tela inicial

### Para Desenvolvedores
- ✅ Cadastro como desenvolvedor
- ✅ Upload de aplicativos (APK + logo)
- ✅ Campos obrigatórios: nome, versão, descrição
- ✅ Upload de imagem da logo do app
- ✅ Controle de downloads

## Tecnologias Utilizadas

- **Frontend**: React 18, HTML5, CSS3, JavaScript ES6+
- **Backend**: Node.js, Express.js
- **Banco de Dados**: SQLite3
- **Autenticação**: JWT (JSON Web Tokens)
- **Upload de Arquivos**: Multer
- **Estilização**: CSS customizado com gradientes e animações

## Instalação e Configuração

### Pré-requisitos
- Node.js (versão 16 ou superior)
- npm ou yarn

### Passos para instalação

1. **Clone o repositório**
```bash
git clone <url-do-repositorio>
cd loja-apps-android
```

2. **Instale as dependências**
```bash
npm install
```

3. **Inicie o servidor backend**
```bash
node server.js
```

4. **Em outro terminal, inicie o frontend**
```bash
npm start
```

5. **Acesse a aplicação**
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## Estrutura do Projeto

```
loja-apps-android/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── App.js
│   │   ├── AppCard.js
│   │   ├── AppDetails.js
│   │   ├── Carousel.js
│   │   ├── Home.js
│   │   ├── Login.js
│   │   ├── Navbar.js
│   │   ├── RatingModal.js
│   │   ├── Register.js
│   │   └── UploadApp.js
│   ├── contexts/
│   │   └── AuthContext.js
│   ├── App.css
│   ├── App.js
│   ├── index.css
│   └── index.js
├── server.js
├── package.json
└── README.md
```

## API Endpoints

### Autenticação
- `POST /api/register` - Cadastro de usuário
- `POST /api/login` - Login de usuário

### Aplicativos
- `GET /api/apps` - Listar aplicativos (com busca)
- `GET /api/apps/recent` - Aplicativos recentes
- `GET /api/apps/:id` - Detalhes do aplicativo
- `POST /api/apps` - Criar aplicativo (desenvolvedores)
- `GET /api/apps/:id/download` - Download do APK

### Avaliações
- `POST /api/apps/:id/rate` - Avaliar aplicativo
- `GET /api/apps/:id/ratings` - Listar avaliações

## Banco de Dados

O sistema utiliza SQLite com as seguintes tabelas:

- **users**: Usuários e desenvolvedores
- **apps**: Aplicativos publicados
- **ratings**: Avaliações dos aplicativos

## Funcionalidades Implementadas

### ✅ Sistema de Autenticação
- Cadastro de usuários comuns e desenvolvedores
- Login com JWT
- Proteção de rotas
- Context API para gerenciamento de estado

### ✅ Interface de Usuário
- Design responsivo e moderno
- Carrossel de aplicativos recentes
- Sistema de busca em tempo real
- Cards de aplicativos com informações
- Modal de avaliação interativo

### ✅ Sistema de Upload
- Upload de APK (até 100MB)
- Upload de logo (imagens)
- Drag and drop
- Preview de arquivos
- Validação de tipos de arquivo

### ✅ Sistema de Avaliação
- Avaliação de 1 a 5 estrelas
- Comentários opcionais
- Média de avaliações
- Contagem de downloads

## Como Usar

### Para Usuários
1. Acesse a loja
2. Cadastre-se ou faça login
3. Busque por aplicativos
4. Visualize detalhes e baixe APKs
5. Avalie os aplicativos

### Para Desenvolvedores
1. Cadastre-se como desenvolvedor
2. Faça login
3. Acesse "Subir App"
4. Preencha as informações do aplicativo
5. Faça upload do APK e logo
6. Publique o aplicativo

## Características Técnicas

- **Responsivo**: Funciona em desktop, tablet e mobile
- **Seguro**: Autenticação JWT, validação de arquivos
- **Performático**: SQLite para dados, otimizações de carregamento
- **Moderno**: Interface com gradientes, animações e ícones Font Awesome
- **Intuitivo**: UX otimizada para fácil navegação

## Próximas Melhorias

- [ ] Sistema de categorias de aplicativos
- [ ] Filtros avançados (por categoria, avaliação, data)
- [ ] Sistema de notificações
- [ ] Dashboard para desenvolvedores
- [ ] Sistema de comentários em avaliações
- [ ] Compressão automática de imagens
- [ ] Sistema de versionamento de aplicativos

## Suporte

Para dúvidas ou problemas, entre em contato através dos issues do repositório.
