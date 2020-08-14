# Required Software
* Node.js 14.x.x
* npm
* PostgreSQL 12

# Web
[@comet-app/web](https://github.com/comet-app/web) runs the frontend website. The project is written in [Vue.js](https://vuejs.org/) and uses [Nuxt.js](https://nuxtjs.org/) for server-side rendering.

To run a development server, use `npm run dev`

To run a production server, use `npm run build` then `npm run start`

You need to set an environment variable `BASE_URL` with the address of the server running the backend. For a development environment, this should be your local IP address with port 4000. Example: https://api.getcomet.net

# Server
[@comet-app/server](https://github.com/comet-app/server) runs the backend server. The project is written in [TypeScript](https://www.typescriptlang.org/). [TypeORM](https://typeorm.io/#/) is used for the database and [TypeGraphQL](https://typegraphql.com/) is used for the GraphQL API.

To run a development server, use `npm run dev`

To run a production server, use `npm run tsc` then `npm run start`

## Environment variables
`ACCESS_TOKEN_SECRET` (Required): a secure password used for encrypting JWT tokens
`DATABASE_URL` (Required in production): URL for the PostgreSQL 12 database
`ORIGIN_URL` (Required in production): the URL of the server running `web`. Example: https://www.getcomet.net
`AWS_ACCESS_KEY_ID` (Optional, needed for image upload and thumbnails): your AWS access key ID
`AWS_SECRET_ACCESS_KEY` (Optional, needed for image upload and thumbnails): your AWS secret access key
`COMET_BOT_PASSWORD` (Optional, needed if running bot): Password to login to the Comet bot
`DISCORD_TOKEN` (Optional, needed for report button and feedback): Token for Discord bot

## Dev Database
Your local PostgreSQL 12 database is expected to have the following credentials:
`port: 5432`
`username: postgres`
`password: password`
`database: postgres`

# What type of contributions are desired?
Bug fixes are appreciated and will likely be merged. If you are interested in implementing a new feature or making a major change, please contact Dan#7457 on [our Discord](https://discord.gg/NPCMGSm).
