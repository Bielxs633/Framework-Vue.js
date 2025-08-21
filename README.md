# Vue.js Project

Este guia fornece instruções detalhadas para configurar um projeto Vue.js do zero, incluindo dependências essenciais e configurações recomendadas. E também algumas informações sobre a FrameWork.

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:
- **Node.js** (versão 16.8 ou superior)
  - Download: [https://nodejs.org/](https://nodejs.org/)
  - Verifique a instalação: `node --version`
- **npm** (geralmente vem com Node.js)
  - Verifique a instalação: `npm --version`
- **Editor de código** recomendado: Visual Studio Code

| Software    | Versão Mínima | Comando de Verificação |
|-------------|---------------|-----------------------|
| **Node.js** | 16.8+         | `node --version`      |
| **npm**     | 7.0+          | `npm --version`       |
| **Editor**  | VS Code       | ---                   |

---

## 🚀 Passo a Passo de Instalação

### 1. Instalação do Vue CLI
Recomendamos usar o Vue CLI para criar e gerenciar projetos Vue.js:
```bash
# Instalação do Vue CLI
npm install -g @vue/cli
# Verifique a instalação
vue --version
```

### 2. Atualizar o Vue CLI
```bash
# Atualização do Vue CLI
npm update -g @vue/cli
# Verifique a atualização
vue --version
```

### 3. Criação do Projeto
```bash
1. # Crie uma pasta para seu projeto

2. # Abra o terminal dessa mesma pasta

3. # Criar novo projeto
    npm criar vue@latest

    - Este comando irá instalar e executar criar-vue, a ferramenta oficial de andaimes do projeto Vue. Você será apresentado com prompts para vários recursos opcionais, como TypeScript e suporte a testes como:
✔ Project name: … <your-project-name>
✔ Add TypeScript? … No / Yes
✔ Add JSX Support? … No / Yes
✔ Add Vue Router for Single Page Application development? … No / Yes
✔ Add Pinia for state management? … No / Yes
✔ Add Vitest for Unit testing? … No / Yes
✔ Add an End-to-End Testing Solution? … No / Cypress / Nightwatch / Playwright
✔ Add ESLint for code quality? … No / Yes
✔ Add Prettier for code formatting? … No / Yes
✔ Add Vue DevTools 7 extension for debugging? (experimental) … No / Yes
Scaffolding project in ./<your-project-name>...
Done.

4. # Navegue para o diretório do projeto
cd <nome-projeto>

5. # Crie a build do projeto
npm install

6. # Gera o link
npm run dev

Agora você deve ter seu primeiro projeto Vue em execução!!
```

### IDE Recomendada ( Ambiente Integrado de Desenvolvimento Recomendado )

A configuração IDE recomendada é [Visual Studio Code](https://code.visualstudio.com) + [Vue Extensão oficial](https://marketplace.visualstudio.com/items?itemName=Vue.volar).

### 🔧 Ferramentas

Mais detalhes de ferramentas, incluindo integração com estruturas de back-end, são discutidos no [Guia Ferramentaria](https://vuejs.org/guide/scaling-up/tooling.html).

## 🖥️ Consumo de API

Para consumir uma API, primeiro é necessário instalar o [Axios](https://axios-http.com/ptbr/docs/intro), que facilitará as requisições. Para o instalar, rode no terminal o seguinte comando:
```bash
# Instalação do Axios
npm install axios
```

### Estrutura
Em seguida, é recomendado criar uma pasta "services" no diretório "src". Depois, crie um arquivo chamado "api.js" ou qualquer outro nome que facilite seu entendimento.
- A estrutura de pastas se parecerá assim:
```bash
meu-projeto/
├─ node_modules/ 
├─ public/
│   └─ favicon.ico
├─ src/
│   ├─ assets/
│   │   └─ vue.svg
│   ├─ components/
│   │   └─ HelloWorld.vue
│   ├─ services/
│   │   └─ api.js
│   ├─ App.vue
│   ├─ main.js
├─ .gitignore
├─ index.html
├─ package.json
├─ vite.config.js
```
Dentro do seu arquivo da api (nesse caso, o "api.js") você precisa importar o Axios, que instalamos anteriormente.
```bash
# Import do Axios
import axios from "axios"
```

### Consumindo a API
Daqui pra frente, tem várias formas de codificar esse arquivo, mas aqui está como fizemos considerando a [Dog API](https://dog.ceo/dog-api/documentation/random) usando estrutura try-catch:

#### Imagens Aleatórias:
```javascript
// Função que retorna imagem aleatória de um cachorro
export async function getRandomDog() {
  try {
    const res = await axios.get(`https://dog.ceo/api/breeds/image/random`);

    return res.data;
  } catch (error) {
    console.error("Erro ao buscar cachorro:", error)
    return null
  }
}
```

### Mais informações sobre o Consumo de API:
[Consumindo uma API com Vue.js e Axios](https://www.devmedia.com.br/consumindo-uma-api-com-vue-js-e-axios/42974)


### Autores
🔗 <img src="https://img.icons8.com/color/48/000000/linkedin.png" width="20" td align="center"/> ⇒
    [Gabriel Soares](https://www.linkedin.com/in/gabriel-soares-3098782b0/)<br>
🔗 <img src="https://img.icons8.com/fluent/48/000000/github.png" width="20" td align="center"/> ⇒
    [Gabriel Soares](https://github.com/Bielxs633)

🔗 <img src="https://img.icons8.com/color/48/000000/linkedin.png" width="20" td align="center"/> ⇒
    [Ana Julia](https://www.linkedin.com/in/gabriel-soares-3098782b0/)<br>
🔗 <img src="https://img.icons8.com/fluent/48/000000/github.png" width="20" td align="center"/> ⇒
    [Ana Julia](https://github.com/Bielxs633)

🔗 <img src="https://img.icons8.com/color/48/000000/linkedin.png" width="20" td align="center"/> ⇒
    [Nicolas Silva](https://www.linkedin.com/in/gabriel-soares-3098782b0/)<br>
🔗 <img src="https://img.icons8.com/fluent/48/000000/github.png" width="20" td align="center"/> ⇒
    [Nicolas Silva](https://github.com/Bielxs633)

🔗 <img src="https://img.icons8.com/color/48/000000/linkedin.png" width="20" td align="center"/> ⇒
    [Heloysa Vilela Santos](https://www.linkedin.com/in/gabriel-soares-3098782b0/)<br>
🔗 <img src="https://img.icons8.com/fluent/48/000000/github.png" width="20" td align="center"/> ⇒
    [Heloysa Vilela Santos](https://github.com/Bielxs633)

---