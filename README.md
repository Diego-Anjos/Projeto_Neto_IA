<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />

# 🤖 NetoIA - Seu Assistente Digital Paciente

### Apresentado na Expo Tech UniFECAF 2025

[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)

</div>

---

## 📋 Sobre o Projeto

**NetoIA** é um assistente digital inteligente desenvolvido com foco em acessibilidade e facilidade de uso. O sistema utiliza a API Google Gemini para fornecer respostas contextuais e instruções passo a passo, sendo especialmente útil para auxiliar usuários em tarefas do dia a dia no ambiente digital.

O projeto foi criado como trabalho acadêmico para apresentação na **Expo Tech UniFECAF 2025**, demonstrando a integração de tecnologias modernas de IA com interfaces web responsivas e acessíveis.

### 👥 Equipe de Desenvolvimento

| Nome | RA |
|------|-----|
| **Diego dos Anjos Gomes** | 7961 |
| **Gustavo Ribeiro Santos** | 90044 |
| **Ian Meirelles** | 94838 |

---

## ✨ Funcionalidades

- 🗣️ **Reconhecimento de Voz**: Faça perguntas usando o microfone
- 🔊 **Síntese de Voz**: Ouça as respostas em áudio com voz
- 📝 **Instruções Passo a Passo**: Receba tutoriais visuais detalhados
- 🌐 **Suporte Multilíngue**: Interface em Português e Inglês
- 💬 **Histórico de Conversas**: Mantenha e organize suas interações
- 🎨 **Interface Moderna**: Design responsivo e intuitivo
- 🖼️ **Descrições Visuais**: Cada passo inclui descrições de imagens ilustrativas
- 📋 **Copiar Textos**: Copie facilmente instruções e respostas

---

## 🚀 Tecnologias Utilizadas

### Frontend
- **React 19.1.1** - Biblioteca JavaScript para construção de interfaces
- **TypeScript 5.8.2** - Superset JavaScript com tipagem estática
- **Vite 6.2.0** - Build tool e servidor de desenvolvimento rápido

### Inteligência Artificial
- **Google Gemini API (@google/genai 1.21.0)** - Modelo de IA generativa para processamento de linguagem natural
- **Web Speech API** - Reconhecimento e síntese de voz nativa do navegador

### Recursos Nativos
- **SpeechRecognition API** - Captura de entrada de voz
- **SpeechSynthesis API** - Conversão de texto em fala
- **LocalStorage** - Persistência de conversas no navegador

### Estrutura do Projeto
```
NetoIA/
├── components/          # Componentes React reutilizáveis
│   ├── ChatInterface.tsx
│   ├── Header.tsx
│   ├── InputBar.tsx
│   ├── MessageBubble.tsx
│   ├── Sidebar.tsx
│   └── SettingsModal.tsx
├── contexts/           # Contextos React (Estado Global)
│   └── LanguageContext.tsx
├── hooks/              # Custom Hooks
│   ├── useSpeech.ts
│   └── useTranslations.ts
├── services/           # Integração com APIs externas
│   └── geminiService.ts
├── utils/              # Utilitários e traduções
│   └── translations.ts
├── types.ts            # Definições de tipos TypeScript
└── App.tsx             # Componente principal
```

---

## 🛠️ Como Configurar e Executar

### Pré-requisitos

- **Node.js** (versão 16 ou superior)
- **npm** ou **yarn**
- **Chave de API do Google Gemini**

### Passo 1: Obter a Chave API do Google Gemini

1. Acesse [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Faça login com sua conta Google
3. Clique em **"Create API Key"** (Criar chave de API)
4. Copie a chave gerada

### Passo 2: Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/Neto_IA.git
cd Neto_IA
```

### Passo 3: Instalar Dependências

```bash
npm install
```

### Passo 4: Configurar Variáveis de Ambiente

1. Crie um arquivo `.env` na raiz do projeto
2. Adicione sua chave API:

```env
GEMINI_API_KEY=sua-chave-api-aqui
```

> **Nota**: Você pode adicionar múltiplas chaves separadas por vírgula para rotação automática:
> ```env
> GEMINI_API_KEY=chave1,chave2,chave3
> ```

### Passo 5: Executar o Projeto

```bash
npm run dev
```

O aplicativo estará disponível em: **http://localhost:3000**

### Passo 6: Build para Produção

```bash
npm run build
```

Os arquivos otimizados serão gerados na pasta `dist/`

---

## 🎯 Como Usar

### 1. Fazer uma Pergunta

- **Por Texto**: Digite sua pergunta no campo de entrada e pressione Enter
- **Por Voz**: Clique no ícone do microfone e fale sua pergunta

### 2. Receber Respostas

- As respostas aparecem em formato de chat
- Instruções complexas são exibidas em passos numerados
- Cada passo inclui descrição visual e texto explicativo

### 3. Ouvir Respostas

- Clique no ícone de alto-falante (🔊) ao lado das mensagens
- O sistema lerá o conteúdo em voz alta
- Use o botão de pausa para controlar a reprodução

### 4. Gerenciar Conversas

- **Nova Conversa**: Clique no botão "+ Nova Conversa"
- **Histórico**: Acesse conversas anteriores na barra lateral
- **Configurações**: Altere idioma e preferências no menu de configurações

### 5. Copiar Conteúdo

- Use o botão de copiar (📋) para copiar textos de instruções
- Copie passos individuais ou mensagens completas

---

## 🌟 Funcionalidades Técnicas Detalhadas

### Sistema de Rotação de Chaves API

O sistema implementa rotação automática entre múltiplas chaves API do Google Gemini, garantindo:
- **Alta disponibilidade**: Troca automática em caso de limite de quota
- **Balanceamento**: Distribuição equilibrada de requisições
- **Resiliência**: Continuidade do serviço mesmo com falhas pontuais

### Geração de Instruções Estruturadas

Utiliza **structured output** do Gemini para gerar:
- Passos numerados e organizados
- Descrições de imagens para cada etapa
- Formato JSON validado e tipado

### Síntese de Voz Otimizada

- Priorização de vozes femininas em português
- Controle de velocidade e entonação
- Gerenciamento de estado centralizado (singleton pattern)
- Suporte a pausa/retomada da leitura

### Persistência de Dados

- Armazenamento local de conversas
- Sincronização automática com LocalStorage
- Recuperação de contexto entre sessões

---

## 🔒 Segurança e Privacidade

- ✅ Chaves API armazenadas apenas em variáveis de ambiente
- ✅ Conversas armazenadas localmente no navegador do usuário
- ✅ Nenhum dado enviado para servidores próprios
- ✅ Comunicação direta com API Google via HTTPS

---

## 📱 Compatibilidade

### Navegadores Suportados

- ✅ Google Chrome (recomendado)
- ✅ Microsoft Edge
- ✅ Safari (iOS 15+)
- ⚠️ Firefox (reconhecimento de voz limitado)

### Dispositivos

- 💻 Desktop (Windows, macOS, Linux)
- 📱 Mobile (Android, iOS)
- 📟 Tablets

---

## 🐛 Solução de Problemas

### Erro: "Nenhuma chave de API do Google foi configurada"

**Solução**: Verifique se o arquivo `.env` existe e contém `GEMINI_API_KEY=sua-chave`

### Áudio não funciona

**Solução**: 
1. Verifique se deu permissão de áudio no navegador
2. Confirme que o dispositivo de áudio está ligado e selecionado
3. Teste em modo de navegação anônima (pode haver extensões bloqueando)

### Reconhecimento de voz não responde

**Solução**:
1. Verifique permissões de microfone no navegador
2. Teste com outro navegador (Chrome recomendado)
3. Certifique-se de que o microfone está funcionando

---

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos como parte da **Expo Tech UniFECAF 2025**.

---

## 🤝 Contribuições

Este é um projeto acadêmico, mas sugestões e feedback são bem-vindos!

---

## 📞 Contato

**Instituição**: UniFECAF  
**Evento**: Expo Tech 2025  
**Curso**: Gestão Tecnologia da Informação  
**Ano**: 2025

---

<div align="center">

### Desenvolvido com ❤️ por Diego Gomes, Gustavo Santos e Ian Meirelles

**UniFECAF - Expo Tech 2025**

</div>
