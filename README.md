# Ourion Frontend

## Project Overview
The OpenCV Ourion project aims to leverage computer vision and machine learning techniques to enhance recycling efficiency. This repository contains the **React Frontend** interface.

## Running Locally

### 1. Install Dependencies
Open a terminal in the repository root (WSL or PowerShell) and run:
```
npm install
```
### 2. Start the React App
```
npm start
```
The frontend will be available at:
http://localhost:3000

### 3. Connecting to the Backend
Ensure your Backend API is running. By default, this frontend expects the backend at http://localhost:5000. If you are deploying to production (e.g., Render), update your API URL variable to the live server address.

## Development Environment & Set Up (Node.js)

This guide describes how to set up the development environment using WSL and Node.js.

1. Install WSL (Ubuntu)

(Skip if you already have WSL installed)

- Open PowerShell as Administrator.

- Run: wsl --install

- Restart your machine if prompted and create a Linux user account.

2. Install Node.js in WSL

We use nvm (Node Version Manager):

- Install nvm:
```
curl -o- [https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh](https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh) | bash
```

- Load nvm (or restart terminal):

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

- Install Node.js (LTS):
```
nvm install --lts
nvm use --lts
nvm alias default lts/*
```

- Verify Installation:
```
node -v
npm -v
```
3. Configure Git + SSH

- Set Username/Email:
```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
- Generate SSH Key:
```
ssh-keygen -t ed25519 -C "your.email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
- Add to GitHub: Copy the key (cat ~/.ssh/id_ed25519.pub) and add it to GitHub Settings → SSH and GPG keys.

4. Clone the Repository
```
git clone [https://github.com/YOUR_USERNAME/ourion.git](https://github.com/mmurata22/ourion.git)
```