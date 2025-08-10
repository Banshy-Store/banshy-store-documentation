# How to install HeidiSQL

Here’s a step-by-step guide to downloading and installing MariaDB and HeidiSQL.

## Download and Install MariaDB

### Download MariaDB
- Visit the official MariaDB website: [MariaDB downloads](https://mariadb.org/download/).
- Select your operating system (Windows, Linux, macOS).
- Download the recommended stable version.

### Run the Installer
- Open the downloaded file and start the installation process.
- Accept the terms and conditions.

### Configuration During Installation
- Select Components: ensure "MariaDB Server" and "Command Line Tools" are selected for installation.
- User Setup: set a password for the `root` user (administrator). Save this password securely.
- Connection Port: the default port for MariaDB is `3306`. Keep this default unless another service is using the same port.

### Complete the Installation
- Follow the installer’s instructions to finish the setup.
- MariaDB will be installed as a service and will start automatically.

## Download and Install HeidiSQL

### Download HeidiSQL
- Visit the official HeidiSQL website: [HeidiSQL downloads](https://www.heidisql.com/download.php).
- Download the latest version for Windows.

### Run the Installer
- Open the downloaded file and start the installation process.
- Follow the standard steps (accept terms, choose folder, etc.).

## Set Up a Connection in HeidiSQL
- Open HeidiSQL after installation.
- Click "New" to create a new connection.
- Fill in the fields as follows:
  - **Network Type**: MySQL (TCP/IP)
  - **Hostname/IP**: `localhost` (or your server's IP)
  - **User**: `root`
  - **Password**: use the password you set during the MariaDB installation
  - **Port**: `3306` (or the port you configured for MariaDB)
- Click "Save" and then "Open" to connect.

## Visual guide with video
If you haven't done it yet, here is a short installation guide for MariaDB and HeidiSQL. (Video guide to be added here.)

## Media
- Screenshots: [Placeholder – HeidiSQL new session setup]


