# Driven.t

<img width="800" alt="Captura de Tela 2023-09-09 às 00 35 36" src="https://github.com/natividadesusana/drivent-frontend/assets/95102911/e3bb4593-d756-4571-ab73-5de3b7878f3a">
<img width="800" alt="Captura de Tela 2023-09-09 às 00 42 57" src="https://github.com/natividadesusana/drivent-frontend/assets/95102911/13dd7836-08f6-4764-818f-31a4136c013a">
<img width="800" alt="Captura de Tela 2023-09-09 às 00 43 34" src="https://github.com/natividadesusana/drivent-frontend/assets/95102911/245a36a6-8896-4bab-a360-79fbdd731503">
<img width="800" alt="Captura de Tela 2023-09-09 às 00 44 13" src="https://github.com/natividadesusana/drivent-frontend/assets/95102911/ab52f288-c3cd-4969-b874-8d4b6013d1e5">
<img width="800" alt="Captura de Tela 2023-09-09 às 00 44 29" src="https://github.com/natividadesusana/drivent-frontend/assets/95102911/78b8d399-ea2d-487f-b728-917992ee1281">
<img width="800" alt="Captura de Tela 2023-09-09 às 00 47 35" src="https://github.com/natividadesusana/drivent-frontend/assets/95102911/781d676d-6609-493d-97ab-ba641135ec0f">
<img width="800" alt="Captura de Tela 2023-09-09 às 00 48 28" src="https://github.com/natividadesusana/drivent-frontend/assets/95102911/df38017b-9a65-4bb2-834c-a65278427458">

</br></br>

🔸 **Demo:** https://drivent-frontend-kohl.vercel.app/

🔸 **Driven.t Organization:** https://github.com/drivent-ed

<hr/>

## ℹ️ About

The Driven.t project's mission is to create an event management system, focusing on providing a customizable application for each specific event. Using the White Label concept, Driven.t allows customers to have a unique application for each event they want to manage. The system has a timer that releases access on the start date of event registration and offers features such as registration (online or in person), choice of accommodation for in-person events, payment options, selection of activities at the event and the issuance of certificates of participation. The application is a web application and its development can be started by following the configuration and execution instructions in the development environment provided in the project repository.

<hr/>

## ⚙️ How to run for development

1. Clone this repository
2. Install all dependencies

```bash
npm i
```

3. Populate `.env` file based on `.env.example`. `REACT_APP_API_BASE_URL` should point to your API server (driven.t-back)

4. Run the back-end in a development environment:

```bash
npm run start
```

<hr/>

## 🛠️ Building and starting for production

```bash
npm run build
npm start
```

<hr/>

## 🚀 Running application locally or inside docker

`.env.development` and `.env.test` must be changed if you and to run the application locally or inside docker. You can populate files based on `.env.example` file, but you need to consider the following:

- Running application locally (postgres and node):

Add your postgres credentials and make sure to create given database before running the application.

- Running application inside docker (postgres and node):

Set `POSTGRES_HOST` to `drivent-postgres-development` for `.env.development` and `drivent-postgres-test` for `.env.test` file. It is the name of the postgres container inside docker-compose file. Docker Compose will start the postgres container for you, create the database and host alias for you.

- Running application locally (node) but postgres is running inside docker:

Set `POSTGRES_HOST` to `localhost` for `.env.development` and `localhost` for `.env.test` file. Docker compose is configured to expose postgres container to your localhost.

<hr/>

## 🖇 What to do when add new ENV VARIABLES

Please notice that every ENV that should be available on browser should start with `REACT_APP_` prefix. There are several things you need to do when you add new ENV VARIABLES:

- Add them to `.env.example` file
- Add them to your local `.env` file
- Add them to your docker-compose.yml file (just the name, not the value). Only envs listed in the environment section will be exposed to your docker container.
- Add them (prod version) to your github repo secrets. They will be used to generate the `.env` file on deploy.

<hr/>

## How to Contribute
Contributions are always welcome! If you find any bugs or have suggestions for new features, feel free to open an issue or pull request.
