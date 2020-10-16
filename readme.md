# Comandos BACKEND NODE

yarn init -y

yarn add express

yarn add typescript -D

yarn tsc --init  "Atualização do es5"

yarn add ts-node-dev -D  "Conseguir executar nosso projeto"

*Flags do ts-node-dev*
*--transpile-only*, *--ignore-watch node_modules*

# Banco de Dados

yarn add typeorm sqlite3

1step Intalar typeorm e sqlite.
2step criar diretorio data base e fazer a connection createConnection do typeorm dentro diretorio database.

# Migrations

Vamos utilizar migrations.

Criar diretorio dentro da pasta database chamado migrations

Criar script "typeorm": "ts-node-dev ./node_modules/typeorm/cli.js", para dizer pro typeorm entender js

## Config ormconfig.json
`{
    "type": "sqlite",
    "database": "./src/database/database.sqlite",
    "migrations": [
        "./src/database/migrations/*.ts"
    ],
    "cli": {
        "migrationsDir": "./src/database/migrations"
    }
}`

Criar primeira tabela
yarn typeorm migration:create -n create_orphanages

## Lidando com upload de images
yarn add multer

*OBS ESTUDAR ARQUITETURA MVC*

## Lidando com erros no express
yarn add express-async-errors

## Validação
yarn add yup


## Para aplicação poder ser consumida

yarn add cors

