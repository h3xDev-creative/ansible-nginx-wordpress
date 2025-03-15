
# 🐳 Ansible WordPress with NGINX Setup 🚀

Welcome to the **Ansible WordPress with NGINX** project! This project uses Ansible to deploy a WordPress site with an NGINX container, and it’s as easy as pie! 🍰

## 🛠️ Requirements

Before you start, make sure you have the following:

- **Ansible** (obviously 😉)
- **Docker** (for containerizing NGINX and WordPress 🐋)
- **Git** (to clone WordPress from the repo 📂)

---

## 💻 Installation

### 1️⃣ Install Ansible

#### On Ubuntu:
```bash
sudo apt update
sudo apt install ansible
```

#### On macOS (using Homebrew):
```bash
brew install ansible
```

#### On Windows (via WSL or Cygwin):
Follow the [Windows installation guide for Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

---

### 2️⃣ Install Docker

Follow the official instructions for [Docker installation](https://docs.docker.com/get-docker/).

---

### 3️⃣ Clone the Repository

Now, let’s get the project on your local machine! Clone the repo with Git:

```bash
git clone https://github.com/your-username/ansible-wordpress-nginx.git
cd ansible-wordpress-nginx
```

---

## 🔑 Set Environment Variables

To ensure everything runs smoothly, you’ll need to set some environment variables for your WordPress database. These variables will be used within the Ansible playbook to configure the Docker container.

### 1️⃣ Set Environment Variables

You can either set these variables in your shell or export them for the session.

#### Temporary (for the current session):
```bash
export WORDPRESS_DB_HOST=localhost
export WORDPRESS_DB_NAME=wordpress_db
export WORDPRESS_DB_USER=wp_user
export WORDPRESS_DB_PASSWORD=wp_password
```

#### Permanent (add to `~/.bashrc` or `~/.zshrc`):
```bash
echo 'export WORDPRESS_DB_HOST=localhost' >> ~/.bashrc
echo 'export WORDPRESS_DB_NAME=wordpress_db' >> ~/.bashrc
echo 'export WORDPRESS_DB_USER=wp_user' >> ~/.bashrc
echo 'export WORDPRESS_DB_PASSWORD=wp_password' >> ~/.bashrc
source ~/.bashrc
```

Now your environment is ready to go! 😎

---

## 🚀 Running the Playbook

Once everything is set up, run the playbook to deploy the NGINX container with WordPress. You can do this by running:

```bash
ansible-playbook site.yml
```

This will pull the necessary NGINX Docker image, clone WordPress, and configure everything! 🎉

---

## 🔧 Customizing the Setup

You can customize this setup by modifying the playbook `site.yml` or the environment variables, depending on your preferences. 📝

---

## 🔒 Security Tips

- Consider using **Ansible Vault** to securely store sensitive data like passwords. 🔐
- Use a production database instead of the local MySQL setup if you're deploying live. 🌐

---

## 🎉 You Did It!

Congrats on setting up your WordPress site with NGINX and Ansible! 🎉 You now have a fully automated, containerized WordPress setup that you can easily manage and scale. 🚀

---

## 🧑‍💻 Contributing

Feel free to fork this project and make improvements! Pull requests are always welcome. 🤝

---

## 💬 Questions or Issues?

If you have any questions or run into any issues, feel free to open an issue on the GitHub repository. 💡

Happy automating! 🤖
