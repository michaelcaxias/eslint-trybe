# ESLINT - CONFIGURAÇÕES

### Primeiramente, para instalar o **eslint** utilize o comando abaixo:

````shell
npm install eslint --save-dev
````

### Agora para instalar e configurar utilize o comando abaixo:

````shell
./node_modules/.bin/eslint --init
````

---

### 1. Escolha a opção **To check syntax and find problems**. Isso possibilitará ao nosso arquivo de configuração encontrar problemas e corrigir a sintaxe de nossos arquivos JavaScript
![image](https://course.betrybe.com//real-life-engineer/es-lint/images/question-1.png)

### 2. Escolha a opção **JavaScript modules (import/export)**, pois essa é a opção mais atualizada de importação.
![image](https://user-images.githubusercontent.com/79621661/136702857-f2acd66e-4d09-4c57-9812-95ceb79a5573.png)

### 3. Escolha a opção que seu projeto está utilizando.

![image](https://user-images.githubusercontent.com/79621661/136702916-19d04f77-57a1-4fc6-b6f9-7dbbff977f82.png)

### 4. Agora especifique se seu projeto usa ou não TypeScript.
![image](https://user-images.githubusercontent.com/79621661/136702964-d90c5efc-263e-4084-a869-5cda558ac9d6.png)

### 5. Nessa parte você pode selecionar o local onde seu código está rodando. Faça a seleção utilizando a barra de espaço para selecionar um ou os dois.
![image](https://course.betrybe.com//real-life-engineer/es-lint/images/question-5.png)

### 6. Escolha o formato JSON.
![image](https://user-images.githubusercontent.com/79621661/136703188-3965313d-5a44-41e7-a3cf-e76421ac6491.png)

---

### Agora escolha qual configuração da Trybe você deseja utilizar

- Fundamentals: `eslint-config-trybe-fundamentals` (JavaScript, CSS e HTML)
- Front-end: `eslint-config-trybe-frontend` (React e CSS)
- Back-end: `eslint-config-trybe-backend`


### Após a seleção, utilize o comando abaixo para instalar de acordo com a opção que você escolheu.
````shell
  npm install (opção selecionada)
````

### Feito a instalação, vá até o arquivo ``.eslintrc.json`` e substitua a configuração inicial da chave ``extends`` para:
(o valor do extends deve estar de acordo com a opção selecionada, no caso abaixo foi utilizado a opção 'frontend')

````json
  "extends": "trybe-frontend",
````

---

## Configurações recomendadas do arquivo ``.eslintrc.json`` para cada opção selecionada.

### - Se você selecionou a opção **frontend** apenas copie o conteúdo abaixo e cole, substituindo todo o seu arquivo ``.eslintrc.json``:
  ````json
  {
    "env": {
      "browser": true,
      "es2020": true
    },
    "extends": "trybe-frontend",
    "parser": "babel-eslint",
    "parserOptions": {
      "ecmaFeatures": {
        "jsx": true
      },
      "sourceType": "module"
    },
    "plugins": ["react", "sonarjs"]
  }
  
  ````

