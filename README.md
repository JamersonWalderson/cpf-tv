# CPF TV - Display de Notícias (Preact.js)

Uma aplicação web desenvolvida em **Preact.js** que exibe notícias da UOL Televisão em formato de display fullscreen com rotação automática.

## 🚀 Tecnologias Utilizadas

- **Preact 10.x** (via CDN) - Apenas ~3KB!
- **Preact Hooks** - useState, useEffect, useCallback
- **Tailwind CSS** - Utility-first CSS framework
- **Babel Standalone** (transformação JSX no browser)
- **HTML5 & CSS3**
- **JavaScript ES6+**
- **RSS/XML Parsing**

## 📋 Como executar

### Pré-requisitos
- Node.js instalado (>= 14.0.0)
- Yarn ou npm

### Instalação das dependências
```bash
yarn install
# ou
npm install
```

### Executar o projeto
```bash
# Servidor básico na porta 8080
yarn start

# Com abertura automática do browser
yarn dev

# Servidor sem cache (desenvolvimento)
yarn serve
```

A aplicação estará disponível em: **http://localhost:8080**

## ⚡ Funcionalidades

- ✅ **Display fullscreen** de notícias da UOL Televisão
- ✅ **Rotação automática** a cada 5 segundos entre notícias
- ✅ **Atualização automática** do feed a cada 5 minutos
- ✅ **Interface responsiva** com design moderno
- ✅ **Imagens de fundo dinâmicas** das notícias
- ✅ **Tratamento robusto de erros** com feedback visual
- ✅ **Loading states** e indicadores visuais
- ✅ **Componentização React** com hooks customizados

## 🏗️ Arquitetura Preact

### Por que Preact?

- **🔥 Ultra-leve**: Apenas ~3KB vs 42KB do React
- **⚡ Performance**: Renderização mais rápida
- **🔄 Compatibilidade**: API quase idêntica ao React
- **📦 Zero configuração**: Funciona direto no browser

### Componentes Principais

- **`NewsDisplay`** - Componente principal da aplicação
- **`Header`** - Cabeçalho com branding CPF TV
- **`BackgroundImage`** - Gerencia imagem de fundo dinâmica
- **`SourceBar`** - Barra de fonte (UOL) com logo
- **`NewsFooter`** - Rodapé com título da notícia atual
- **`LoadingSpinner`** - Indicador de carregamento

### Hooks Customizados

- **`useNewsData`** - Gerencia busca e cache das notícias RSS
- **`useAutoRotation`** - Controla rotação automática entre itens

### Gerenciamento de Estado

- **Preact Hooks** (`useState`, `useEffect`, `useCallback`)
- **Estado local** para notícias, loading e erros
- **Rotação automática** com limpeza de intervalos
- **Performance otimizada** com memoização

## 📁 Estrutura do projeto

```
cpf-tv/
├── index.html          # App Preact + Tailwind CSS
├── package.json        # Dependências e scripts
└── README.md          # Documentação
```

## 🔧 Configurações

As configurações estão centralizadas no objeto `CONFIG`:

```javascript
const CONFIG = {
    API_URL: "https://rss.suatv.com.br/BBC/Convert/Brasil.php",
    ROTATION_INTERVAL: 5 * 1000,    // 5 segundos
    FETCH_INTERVAL: 5 * 60 * 1000   // 5 minutos
};
```

## 🛠️ Desenvolvimento

### Padrões de Código
- **Componentes funcionais** com hooks
- **Props tipadas** com PropTypes (implícito)
- **Separação de responsabilidades** clara
- **Hooks customizados** para lógica reutilizável
- **Error boundaries** via try/catch

### Performance Preact

- **🚀 Tamanho reduzido**: 93% menor que React (~3KB vs 42KB)
- **⚡ Renderização otimizada**: Virtual DOM mais eficiente
- **🎯 Memoização inteligente**: `useCallback` otimizado
- **🔄 Cleanup automático**: Limpeza de intervals no `useEffect`
- **📦 Loading states**: Estados de carregamento otimizados
- **🌐 Cache eficiente**: Requisições com cache de 5 minutos
- **💾 Footprint mínimo**: Ideal para dispositivos com recursos limitados

### Migração React → Preact

✅ **API Compatível**: Hooks e componentes idênticos
✅ **JSX Support**: Sintaxe JSX mantida  
✅ **Performance Boost**: Aplicação mais rápida
✅ **Bundle Size**: 93% de redução no tamanho
✅ **Zero Breaking Changes**: Código funciona sem alterações
