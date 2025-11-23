# AutoFlowLabs Homebrew Tap

## Install BridgeLink

```bash
brew tap AutoFlowLabs/tap
brew install bridgelink
```

# 🍺 AutoFlowLabs Homebrew Tap

Official Homebrew tap for AutoFlowLabs projects.

## 📦 Available Formulas

### BridgeLink

CLI tool to expose Android devices remotely via NativeBridge.

[![PyPI version](https://badge.fury.io/py/bridgelink.svg)](https://badge.fury.io/py/bridgelink)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🚀 Installation

### Quick Install

```bash
brew install AutoFlowLabs/tap/bridgelink
```

### Or Add Tap First

```bash
# Add the tap
brew tap AutoFlowLabs/tap

# Install BridgeLink
brew install bridgelink
```

## ✅ Verify Installation

```bash
bridgelink --version
```

## 🔧 Post-Installation Setup

### 1. Get Your API Key

Get your API key from [NativeBridge Dashboard](https://nativebridge.io/dashboard/api-keys)

### 2. Set Environment Variable

```bash
# Add to your ~/.zshrc or ~/.bash_profile
export NB_API_KEY='Nb-kNGB.your-api-key-here'
```

### 3. Add Your First Device

```bash
# Connect Android device via USB with debugging enabled
bridgelink devices add <device-serial>
```

### 4. Access Remotely

```bash
adb connect bridgelink.nativebridge.io:<port>
```

## 📋 Available Commands

```bash
# Device Management
bridgelink devices add <serial>           # Add device
bridgelink devices add <serial> --auto-activate  # Add with auto-reconnect
bridgelink devices list                   # List all devices
bridgelink devices activate <serial>      # Activate existing device
bridgelink devices deactivate <serial>    # Deactivate device
bridgelink devices remove <serial>        # Remove device

# Auto-Activation
bridgelink devices set-auto-activate <serial> on   # Enable auto-reconnect
bridgelink devices set-auto-activate <serial> off  # Disable auto-reconnect

# Daemon Management
bridgelink daemon status                  # Check tunnel status
bridgelink daemon logs <serial>           # View logs
bridgelink daemon stop <serial>           # Stop tunnel
```

## 🔄 Updating

```bash
brew update
brew upgrade bridgelink
```

## 🗑️ Uninstalling

```bash
brew uninstall bridgelink
brew untap AutoFlowLabs/tap  # Optional: remove tap
```

## 🆘 Troubleshooting

### Formula Not Found

```bash
# Update Homebrew and tap
brew update
brew tap AutoFlowLabs/tap
```

### Permission Issues

```bash
# Fix Homebrew permissions
sudo chown -R $(whoami) $(brew --prefix)/*
```

### ADB Not Found

```bash
# Install Android Platform Tools
brew install android-platform-tools
```

## 📚 Documentation

- [BridgeLink GitHub](https://github.com/AutoFlowLabs/bridgelink)
- [BridgeLink Documentation](https://github.com/AutoFlowLabs/bridgelink#readme)
- [NativeBridge Platform](https://nativebridge.io)
- [Auto-Activation Feature](https://github.com/AutoFlowLabs/bridgelink/blob/main/docs/AUTO_ACTIVATION_FEATURE.md)

## 🐛 Issues

Report issues at: https://github.com/AutoFlowLabs/bridgelink/issues

## �� License

MIT License - see [LICENSE](https://github.com/AutoFlowLabs/bridgelink/blob/main/LICENSE)

---

**Maintained by [AutoFlowLabs](https://github.com/AutoFlowLabs)**
