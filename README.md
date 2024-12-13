# How to Install Nexus CLI using GitHub Codespaces 🚀
A step-by-step guide for developers

## Step 1: Access GitHub Codespaces
1. Go to github.com
2. Login to your GitHub account
3. Click the "+" icon in the top right
4. Select "New codespace"

## Step 2: Configure Your Codespace
1. Choose your repository or select "blank" template
2. Machine type: 2-core (default is fine)
3. Click "Create codespace"
4. Wait for the environment to load

## Step 3: Install Required Dependencies
Open the terminal in Codespaces and run:
```bash
# Update package list
sudo apt update
sudo apt upgrade -y

# Install essential packages
sudo apt install -y build-essential
sudo apt install -y pkg-config
sudo apt install -y libssl-dev
sudo apt install -y libcrypto++-dev
sudo apt install -y gcc
sudo apt install -y libc6-dev
sudo apt install -y zlib1g-dev
```

## Step 4: Install Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
# Choose option 1 for default installation
source "$HOME/.cargo/env"
```

## Step 5: Install Nexus CLI
```bash
curl https://cli.nexus.xyz/ | sh
```

## Step 6: Verify Installation
```bash
# Check Rust installation
rustc --version
cargo --version

# Run Nexus
nexus
```

## Common Issues & Solutions

### If cargo not found:
```bash
source "$HOME/.cargo/env"
```

### If SSL errors occur:
```bash
sudo apt install --reinstall libssl-dev
```

### If compilation fails:
```bash
sudo apt install --reinstall build-essential
```

## Pro Tips 💡
1. Codespaces auto-saves your work
2. Use the built-in VS Code terminal
3. You can access your codespace from any device
4. Environments persist until you delete them



#GitHub #Codespaces #Development #Tutorial

Note: Free GitHub accounts get 120 core-hours/month!
