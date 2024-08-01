# Barbershop - scheduling system web-mobile-app using react

## Technologies

- React
- React Native
- Turbo build
- TypeScript
- NodeJs
- Prisma
- PostgreSQL

## Starting the project

We will use Turbo Build (https://turbo.build/) to start the project.
"Turbo is an incremental bundler and build system optimized for JavaScript and TypeScript, written in Rust."

To verify the documentation, open https://turbo.build/repo/docs

### Let's get started

Open https://turbo.build/repo/docs/getting-started/installation

Make sure you have NPM and NodeJs installed on your machine.

Open your terminal, cd to your repository directory. (E.g. ~/code/src/github/username/).
Run:

```Bash
npx create-turbo@latest <project name>
```

Type 'y' and with arrow keys, choose 'yarn', you may choose another option, but for this project, we will use yarn.

The command will create the project structure, download dependencies, etc.

Change directory (cd)  to `apps` directory and delete docs and web directories. They were created by default.

#### Frontend - NextJS

Open the project in your favorite code editor (or IDE).

Return to the terminal and cd to the project, then cd apps.
Run:

```bash
npx create-next-app@latest frontend
```

Type 'y' to all questions and type ENTER at What import alias would you like configured? … @/*.

#### Backend - NestJs

Open https://docs.nestjs.com/

Run in the apps directory:

```bash
sudo npm i -g @nestjs/cli
nest new backend
```

If nest new backend doesn't work, run ` npm i -g @nestjs/cli`

Select yarn.

#### Mobile - React Native

Open https://reactnative.dev/docs/environment-setup

Run in the apps/:

```bash
npx create-expo-app@latest mobile
```

#### Configuring package.json

In your code editor, open backend/package.json file.

Find     "start:dev": "nest start --watch", (usually line 12)
Replace start:dev to dev:     "dev": "nest start --watch",

Then go to mobile/package.json.

Find and duplicate the line containing    "ios": "expo start --ios", (usually line 9)

Replace the upper ios to dev:     "dev": "expo start --ios",

Now it is a good moment to commit to your Git repository.
If you get `error: 'apps/backend/' does not have a commit checked out
fatal: adding files failed`, remove the .git directory at backend/ and try again.

