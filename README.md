# DevDicas

## Dica 01 - Configurando jest-html-reporter para visualizar seus testes no navegador. 

`
npm install jest-html-repoter --save-dev
`
ou
`npm i -D jest-html-repoter`

Crie o arquivo jesthtmlreporter.json 

```
{
	"pageTitle": "React Wallet",  
	"outputPath": "test-report/index.html",  
	"includeFailureMsg": true 
}
```

Acrescente a linha abaixo no bloco scripts do pakage.json:
```
"scripts": {
    ...
    "html": "set CI=true &&react-scripts test --env=jsdom --testResultsProcessor=./node_modules/jest-html-reporter; google-chrome ./test-report/index.html",
    "html2": "set CI=true &&react-scripts test --env=jsdom --testResultsProcessor=./node_modules/jest-html-reporter "
    ...
  },
```
  
rode o comando  

`npm run html`

Ele vai cirar automaticamente o diretório test-report com o arquivo index.html que será renderizado. 

**Dicas de configurações opcionais**
- https://www.npmjs.com/package/jest-html-reporter

**Referências**
- https://medium.com/@biswa8998/jest-with-html-report-a884b08d6635



