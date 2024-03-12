# Self-Hosted Stack
[![Visit Website](https://img.shields.io/badge/Visit-Website-green.svg)](https://heimdall.hsay.in)

This project is a collection of self-hosted applications that I use on a daily basis. These applications are hosted on a small server and can be accessed via my own domain. The stack includes a variety of tools for note-taking, budget tracking, diagram creation, and more.

<p align="center">
  <img src="image.png" alt="Architecture" width="400">
</p>



## Application List

- **StackEdit:** A multi-functional markdown editor.
- **Flatnotes:** A minimal editor for day-to-day notes.
- **Draw.io:** A tool for generating flowcharts and schematics.
- **Actual Budget:** An application for tracking my budget.
- **Excalidraw:** A whiteboard tool with a hand-written feel.
- **PwPush:** A tool for generating and sharing passwords.
- **String-Is:** A utility for string manipulation functionalities.
- **Heimdall:** A front-page application for easy access to all the apps.

## Installation Guide

1. **Install Docker and Docker-Compose:**
   - Ensure that Docker and Docker-Compose are installed on your server or machine.

2. **Clone the Repository:**
   - Clone this repository and navigate into the project directory.
     ```bash
     git clone https://github.com/your-username/self-hosted-stack.git
     cd self-hosted-stack
     ```

3. **Configure the Docker File:**
   - Make necessary changes in the Docker file, such as credentials, volume mounts, etc.

4. **Start the Applications:**
   - Run the following command to start all the applications in detached mode:
     ```bash
     docker-compose up -d
     ```

## Hosting on a GCP Server (Optional)

If you want to host the entire suite on a minimal Google Cloud Platform (GCP) server with the applications accessible through an Nginx reverse proxy, follow these steps:

1. **Create Nginx Configuration Files:**
   - For each application, create configuration files in `/etc/nginx/sites-available/` with the format `sample.domain.tld`.

2. **Create Symlinks:**
   - Create symbolic links for each configuration file to the `/etc/nginx/sites-enabled/` directory.
     ```bash
     sudo ln -s /etc/nginx/sites-available/sample.domain.tld /etc/nginx/sites-enabled/
     ```

3. **Restart Nginx:**
   - Restart the Nginx service to apply the changes.
     ```bash
     sudo systemctl restart nginx
     ```

4. **Issue SSL Certificates:**
   - Obtain SSL certificates for your domain to ensure secure connections.

## Conclusion

This self-hosted stack provides a convenient way to access and manage personal applications on your own server. Feel free to customize and expand the stack based on your needs.