# VUEdashboard

Questo progetto è stato generato utilizzando claude e questo prompt:

```text
puoi scrivermi un progetto minimale VUE, composto da una prima maschera di login, che interroga il servizio https://reqres.in/api/login passando un json composto da due parametri "email" e "password" e in caso di risposta con codice 200 mi permetta di accedere ad un  backend composto da: un pannello a sinistra con un menu e un pannello centrale nel quale visualizzare dei dati. Nel pannello di sinistra deve essere riportato il tasto di logout
```

## Project setup

```
npm install -g @vue/cli
vue create vuedashboard
cd vuedashboard
yarn add axios
yarn serve
```

### Compiles and hot-reloads for development

```bash
yarn serve
```

<http://localhost:8080/>

### Compiles and minifies for production

```bash
yarn build
```

### Lints and fixes files

```bash
yarn lint
```
