# Railway Discord4J (Maven / Spring) Template

This is a template for deploying Discord4J bots on Railway. It is based on the example Maven / Spring project from
the [example repository](https://github.com/Discord4J/example-projects)

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/GnBRzM?referralCode=Lelebees)

There are, also a few differences:

- Java version `17`
- Discord4J version `3.2.3`
- Built-in guild command support
- Environment variables supported through `.env`

## Guild commands

In order to add a guild command, you can add a folder to `src/main/resources/commands/guild/`,
which must be named with the ID of the guild you wish to register commands for.
Inside that folder, you can put normal `command.json` files.

## Setting up .env

It's quite normal to have a .env file in your project with all the environment variables that matter only for this
project,
so you can test locally.
I've done most of the work for you. you can simply create a file (called `.env`) and place it in the root folder of your
project (next to `Dockerfile` and `pom.xml`).
You can then reference this variable in `application.properties` like a real environment variable, and reference
the `application.properties` variable inside your code using the `@Value`-annotiation. You can find an example of this
inside the `Bot` class.

Never commit the `.env` file to git!

## More Help

You can find more help with using Discord4J and building Discord bots at the following resources:

- [The Discord4J docs](https://docs.discord4j.com/)
- [The Discord4J Discord server](https://discord.gg/NxGAeCY)
- [The Discord Developers Discord server](https://discord.gg/discord-developers)

Additionally, you can find help with using Railway at the following resources:

- [The Railway docs](https://docs.railway.app/)
- [The Railway forum](https://community.railway.app/)
- [The Railway Discord server](https://discord.gg/railway)