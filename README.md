# 💾 local-storage: Aplicação de Notas com Armazenamento Local

![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Expo](https://img.shields.io/badge/Expo-1B1F23?style=for-the-badge&logo=expo&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)

Este repositório contém o código-fonte de um aplicativo móvel simples para gerenciamento de notas, desenvolvido em **React Native** e focado na demonstração de diferentes métodos de **armazenamento de dados local** no ambiente mobile.

O projeto explora a persistência de dados utilizando tanto o `AsyncStorage` quanto o `Expo-SQLite`, servindo como um excelente ponto de partida para desenvolvedores que desejam implementar soluções de armazenamento offline em seus próprios aplicativos.

## 🚀 Tecnologias Utilizadas

O projeto foi construído com as seguintes tecnologias e bibliotecas:

*   **React Native:** Framework para desenvolvimento de aplicações móveis multiplataforma.
*   **Expo:** Conjunto de ferramentas e serviços para facilitar o desenvolvimento de aplicativos React Native.
*   **`@react-native-async-storage/async-storage`:** Sistema de armazenamento de chave-valor simples, assíncrono e persistente.
*   **`expo-sqlite`:** Módulo para acessar o banco de dados SQLite nativo no dispositivo.

## 📁 Estrutura do Projeto

A estrutura de diretórios do projeto é organizada da seguinte forma:

```
local-storage/
├── App.js
├── app.json
├── package.json
├── src/
│   ├── componentes/
│   │   ├── Nota.js
│   │   └── NotaEditor.js
│   └── servicos/
│       ├── Notas.js
│       └── SQLite.js
└── ... (outros arquivos de configuração)
```

### Componentes Principais

| Arquivo | Descrição |
| :--- | :--- |
| `App.js` | Componente raiz que configura a tela e renderiza o `NotaEditor`. |
| `src/componentes/NotaEditor.js` | Interface de usuário (UI) que permite ao usuário digitar e salvar o conteúdo de uma nota. **Utiliza `AsyncStorage`** para persistir o texto. |
| `src/componentes/Nota.js` | Componente destinado a exibir uma nota individual (presumivelmente). |

### Serviços de Armazenamento

| Arquivo | Descrição |
| :--- | :--- |
| `src/servicos/SQLite.js` | Responsável por abrir e manter a conexão com o banco de dados SQLite (`db.db`) usando `expo-sqlite`. |
| `src/servicos/Notas.js` | Contém a lógica para a criação da tabela `Notas` no banco de dados SQLite, com colunas para `id`, `titulo`, `categoria` e `texto`. |

## 🛠️ Como Executar o Projeto

Para rodar este projeto em seu ambiente local, siga os passos abaixo:

### Pré-requisitos

Certifique-se de ter o Node.js, npm/yarn e o Expo CLI instalados em sua máquina.

```bash
# Instale o Expo CLI globalmente, se ainda não o tiver
npm install -g expo-cli
```

### Instalação

1.  Clone o repositório:

    ```bash
    git clone https://github.com/Lucas-dirbal/local-storage.git
    cd local-storage
    ```

2.  Instale as dependências do projeto:

    ```bash
    npm install
    # ou
    yarn install
    ```

### Execução

Inicie o servidor de desenvolvimento do Expo:

```bash
expo start
```

Após a execução, o Expo abrirá uma nova janela no seu navegador. Você pode escanear o código QR com o aplicativo Expo Go (disponível para Android e iOS) para visualizar o aplicativo em seu dispositivo móvel.

## 📝 Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

*README.md gerado por Manus AI.*
