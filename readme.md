# Contact Management Rest API

Manage your contacts effortlessly with this RESTful API — handle users, contacts, and addresses with ease.

## API Specification Documentation

You can find it in the `docs` folder.

## Tech Stack

- Node.js + Express
- TypeScript
- Prisma + MySQL
- Jest (tests)
- Winston (logging)
- Zod (Validation)

## Run the app

1. Install dependencies

   ```shell
       npm install
   ```

2. Setup environments

   Create **.env** file in the root project and add the environment, Make sure you also set up and configure your database connection properly.

   ```env
       DATABASE_URL=mysql://USER:PASSWORD@HOST:PORT/DATABASE
   ```

3. Setup Prisma

   ```shell
        npx prisma migrate dev

        npx prisma generate
   ```

4. Run the app

   - Development Mode:

   ```shell
        npm run dev
   ```

   - Production Mode:

   ```shell
        npm run build

        npm run start
   ```

## Run the test

- Start the test

  ```bash
      npm run test
  ```
