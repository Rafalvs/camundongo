# App React Native + Expo com Firebase Auth

Este projeto implementa autenticação com Firebase em um app React Native usando Expo.

## Configuração do Firebase

### 1. Criar projeto no Firebase Console

1. Acesse [Firebase Console](https://console.firebase.google.com/)
2. Clique em "Adicionar projeto"
3. Siga as instruções para criar seu projeto

### 2. Ativar Authentication

1. No console do Firebase, vá para "Authentication"
2. Clique em "Começar"
3. Na aba "Sign-in method", ative "Email/senha"

### 3. Configurar o app

1. No console do Firebase, clique no ícone da web (</>) para adicionar um app web
2. Registre o app com um nome de sua escolha
3. Copie as configurações do Firebase

### 4. Configurar variáveis de ambiente

1. Copie o arquivo `.env.example` para `.env`:
   ```bash
   cp .env.example .env
   ```

2. Edite o arquivo `.env` e substitua os valores pelas suas configurações do Firebase:
   ```env
   FIREBASE_API_KEY=AIzaSyBxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
   FIREBASE_AUTH_DOMAIN=meuapp-12345.firebaseapp.com
   FIREBASE_PROJECT_ID=meuapp-12345
   FIREBASE_STORAGE_BUCKET=meuapp-12345.appspot.com
   FIREBASE_MESSAGING_SENDER_ID=123456789012
   FIREBASE_APP_ID=1:123456789012:web:abcdef1234567890abcdef
   ```

3. **Importante**: O arquivo `.env` já está no `.gitignore` para não ser commitado no repositório.

## Como usar

### Executar o projeto

```bash
npm start
```

### Funcionalidades implementadas

- ✅ Tela de login/cadastro
- ✅ Autenticação com email e senha
- ✅ Criação de nova conta
- ✅ Estado de autenticação persistente
- ✅ Logout
- ✅ Tratamento de erros

### Estrutura do projeto

```
├── config/
│   └── firebase.js          # Configuração do Firebase
├── context/
│   └── AuthContext.js       # Contexto de autenticação
├── pages/
│   ├── Login.js            # Tela de login/cadastro
│   └── Home.js             # Tela principal (usuário logado)
└── App.js                  # Componente principal
```

### Dependências adicionadas

- `firebase` - SDK do Firebase
- `@react-native-async-storage/async-storage` - Armazenamento local
- `react-native-dotenv` - Para usar variáveis de ambiente

### Arquivos de configuração

- `.env` - Variáveis de ambiente (não commitado)
- `.env.example` - Modelo das variáveis de ambiente
- `babel.config.js` - Configuração do Babel para usar variáveis de ambiente
- `config/firebase.js` - Configuração do Firebase usando variáveis de ambiente

## Próximos passos

- Implementar recuperação de senha
- Adicionar validação de campos
- Implementar navegação com React Navigation
- Adicionar mais métodos de autenticação (Google, Facebook, etc.)
