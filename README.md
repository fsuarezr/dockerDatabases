# Database Dockerization Template
**Yo devs! 👋**

This template's your **one-stop shop** for spinning up **PostgreSQL, MongoDB, MySQL or Redis** databases in Docker containers in a flash. 

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

#### 🚨 **Heads-up: Platform Configuration**
The `platform` flag in the `docker-compose.yml` file is configured for **Apple devices with M1/M2/M3 chips** (`linux/arm64`). If you're using a different architecture, here’s what you need to do:

- **Windows users:** Comment out the `platform` option in the file for each service. Example:
  ```yaml
  # platform: linux/arm64
  ```
- **Linux or other devices:** Check the appropriate platform configuration for your architecture in the [official Docker documentation](https://docs.docker.com/build/building/multi-platform/).

Not configuring this correctly may cause compatibility issues when running the containers.

To access the databases directly from your computer, adjust file permissions for the Docker user:
   ```
   sudo chgrp docker data/postgres data/mongo data/mysql data/redis
   ```

   ```
   sudo chmod +rwx data/postgres data/mongo data/mysql data/redis
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

#### Future improvements: 🌐 Multi-platform builds
For users working with multiple architectures (e.g., ARM and x86), Docker provides tools to build and run images on multiple platforms. If you're interested in adapting this project for multi-platform compatibility, check out the [official Docker guide for multi-platform builds](https://docs.docker.com/build/building/multi-platform/).


### Extra tips 📌📌

- Think about what you might use this for (e.g., local development, testing).
- Remember to keep your passwords strong and secure!
- You can access container logs or interact with them using `docker-compose exec`.

I hope this makes setting up your databases with Docker a breeze!
⭐ **If you found this helpful, don’t forget to give the repo a star on [GitHub](https://github.com/fsuarezr/dockerDatabases)!** ⭐

***
## Autor ✒️

* **Franz Suárez** - *Backend Developer* - [fsuarezr](https://github.com/fsuarezr)

🧑‍💻 Made with ❤️ by [fsuarezr](https://github.com/fsuarezr) 🤘 