# Database Dockerization Template
**Yo devs! 👋**

This template's your **one-stop shop** for spinning up **PostgreSQL, MongoDB, or MySQL** databases in Docker containers in a flash. 

Get everything up and running **smoothly in minutes** with Docker Compose, and enjoy easy management with just one command. Plus, it's customizable and works on any machine with Docker!

Need to tweak things a bit? No problem! You can easily adjust the database settings to perfectly fit your project's needs.

### What's included?
- `docker-compose.yml`: Orchestrates the database party.
- `.env.template`: Shows you how to configure your database settings.

***
## Getting Started 🚀
   
  1. Grab the essentials:
      * [Docker](https://docs.docker.com/desktop/)
      * [Docker Compose](https://docs.docker.com/compose/install/)

   2. Clone this repo:
      ````
      https://github.com/fsuarezr/dockerDatabases.git
      ````
   3. Create a `.env` file:
      - Copy `.env.template` to `.env.`
      - Fill in the blanks with your own database creds and ports.

***
### Running the show: 🔧

1. Open your terminal in the project directory.
2. Run this command:
   ```
   docker-compose -f docker-compose.yml up -d --build --force-recreate
   ```
   - This creates, builds, and starts all your database containers with your custom settings.

To access the databases directly from your computer, adjust file permissions for the Docker user:
   ```
   sudo chgrp docker data/postgres data/mongo data/mysql
   ```

   ```
   sudo chmod +rwx data/postgres data/mongo data/mysql
   ```
   #### Customization and stuff ⚙️

   - **Don't need all the databases?** Comment out the ones you're not using to save resources.
   - **Tweak the settings?** Just edit the `.env` file to your liking.
   - **Control your containers?** Use `docker-compose` commands like `up`, `down`, `stop`, and `logs`.

***
## Contributing and roadmap 📝
If you want to help make this even better, feel free to contribute! 

We also have some cool plans for the future, like:

* Expansion of support for new database platforms.
* Continuously improving and expanding the available documentation.

### Extra tips 📌📌

- Think about what you might use this for (e.g., local development, testing).
- Remember to keep your passwords strong and secure!
- You can access container logs or interact with them using `docker-compose exec`.

I hope this makes setting up your databases with Docker a breeze!

***
## Autor ✒️

* **Franz Suárez** - *Backend Developer* - [fsuarezr](https://github.com/fsuarezr)

🧑‍💻 Made with ❤️ by [fsuarezr](https://github.com/fsuarezr) 🤘 