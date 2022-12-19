# Express React Project

This is the starter for the Express React project.

## Getting started

1. Clone this repository (only this branch)

   ```bash
   git clone https://github.com/grau-maus/express-react-starter-flyio.git
   ```

2. Install dependencies

   ```bash
   npm install
   ```

3. Create a **.env** file based on the example with proper settings for your
   development environment
4. Setup your PostgreSQL user, password, and database and make sure it matches your **.env** file

5. Migrate your database, seed your database, and run your express app

   ```bash
   npx dotenv sequelize db:migrate
   ```

   ```bash
   npx dotenv sequelize db:seed:all
   ```

   ```bash
   npm start
   ```

6. To run the React App in development, checkout the [README](./react-app/README.md) inside the `react-app` directory.

## Deploy to Fly.io

1. Before you deploy, don't forget to navigate into your `frontend` directory and run the following command in order to create a production build for deployment.

   ```bash
   npm run build
   ```

2. Install the [flyctl CLI](https://fly.io/docs/hands-on/install-flyctl/)

3. Run:

   ```bash
   fly auth login
   ```

4. Launch your app:

   ```bash
   fly launch
   ```

5. Type in your app name (or leave blank to generate a random app name)

6. Select a region for deployment (preferably the nearest location unless a majority of your users are based in another region)

7. Select `y` if the CLI asks you if you would like to set up a Postgresql database

8. Select `N` if the CLI asks you if you would like to set up an Upstash Redis database

9. Select `N` if the CLI asks you if you would like to deploy

10. Set up your secret key by running:

    ```bash
    fly secrets set JWT_SECRET=<your secret key> JWT_EXPIRES_IN=604800
    ```

11. Deploy your app:

    ```bash
    fly deploy
    ```

12. profit

### For M1 Mac users

(WIP)
