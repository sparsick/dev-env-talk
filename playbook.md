# Playbook for Demo

## Installation

### NVM (Node Version Manager)

```shell
nvm install --lts --save //--save creates .nvmrc
nvm install 21.0.0
nvm use 21
nvm use --lts
nvm use default
nvm use // use version in .nvmrc
```


### SDKman!

```shell
```

### Prettier

```shell
 pnpm add --save-dev --save-exact prettier
 pnpm exec prettier src --write //or
 pnpm prettier // custom command defined in package.json
```

### Google Java Format
- Intellji Plugin

### Spotless
- Spotless Maven Plugin

```shell
mvn spotless:check
mvn spotless:apply
```


## Local Testing

### Docker Compose

#### Preparation

Build Docker Images for demo:

```shell
cd frontend
pnpm build image
cd ..
cd backend
mvn clean verify
```

#### Ramp up local testing environment

```shell
docker compose up
cd frontend
pnpm dev
cd ..

docker compose down
docker compose up database
cd backend
mvn spring-boot:run

```

Bruno

## Devcontainers

- backend-without-db
- backend-with-db
- backend-with-docker
- frontend

## DevBox


```shell
cd backend
mv .sdkmanrc .sdkmanrc-bck
devbox init
devbox search java
devbox search jdk --show-all
devbox add jdk@21.0.5+11
devbox search maven
devbox add maven@3.9.9
devbox shell

// direnv support

devbox generated direnv
//IDE

```

Add own scripts


## direnv

```shell
# Create a new folder for demo purposes.
cd ~/direnv-demo

# Show that the FOO environment variable is not loaded.
$ echo ${FOO-nope}

# Create a new .envrc. This file is bash code that is going to be loaded by
# direnv.
echo export FOO=foo > .envrc

# The security mechanism didn't allow to load the .envrc. Since we trust it,
# let's allow its execution.
direnv allow .

# Show that the FOO environment variable is loaded.
echo ${FOO-nope}

# Exit the project
cd ..

# And now FOO is unset again
echo ${FOO-nope}
```
