# Home Assistant Fork - macOS ARM64 lru-dict Compatibility Fix

[English](#english) | [中文](#中文)

## English

### Overview

This is a fork of Home Assistant that addresses macOS ARM64 lru-dict compilation issues by removing problematic dependencies. It supports multiple Home Assistant versions with optimized branch structure for different Python environments.

**Originally created for [LifeSmart Integration](https://github.com/MapleEve/lifesmart-HACS-for-hass) - A comprehensive Home Assistant integration for LifeSmart smart home devices!**

### Branch Structure

| Branch | Home Assistant Version | Python Version | Purpose |
|--------|----------------------|----------------|---------|
| `macos-fix-branch` | 2023.6.0 | 3.11 | Main macOS ARM64 fix for Python 3.11 environments |
| `py310-fix-branch` | 2022.10.0 | 3.10 | macOS ARM64 fix for Python 3.10 environments |

### Key Changes

- **lru-dict dependency removal**: Eliminates compilation issues on macOS ARM64
- **Package constraints optimization**: Updated dependency management for better compatibility
- **Multi-version support**: Separate branches for different HA/Python combinations

### Usage

#### For Python 3.11 + HA 2023.6.0:
```bash
pip install git+https://github.com/MapleEve/homeassistant-lru-dict-macos-fix.git@macos-fix-branch
```

#### For Python 3.10 + HA 2022.10.0:
```bash
pip install git+https://github.com/MapleEve/homeassistant-lru-dict-macos-fix.git@py310-fix-branch
```

### Companion Repository

This fork works in conjunction with:
- [pytest-homeassistant-custom-component-fixed](https://github.com/MapleEve/pytest-homeassistant-custom-component-fixed)

### 🏠 Featured Project: LifeSmart Integration

This fork was specifically created to support comprehensive testing of the **[LifeSmart Integration for Home Assistant](https://github.com/MapleEve/lifesmart-HACS-for-hass)**.

#### What is LifeSmart Integration?
A powerful Home Assistant integration that brings LifeSmart smart home ecosystem to your Home Assistant setup:

- **🔌 Comprehensive Device Support**: Lights, switches, sensors, climate control, covers, and more
- **☁️ Multi-Connection Methods**: Local TCP, WebSocket, and OpenAPI support
- **🎯 Advanced Features**: Scene management, real-time status updates, and device discovery
- **🧪 Robust Testing**: Multi-environment CI/CD testing across HA versions 2022.10.0 to latest
- **📱 Easy Installation**: Available through HACS (Home Assistant Community Store)

**[⭐ Star the LifeSmart Integration Repository](https://github.com/MapleEve/lifesmart-HACS-for-hass)** to stay updated with the latest features and improvements!

### Original Repository

Based on [home-assistant/core](https://github.com/home-assistant/core)

---

## 中文

### 概述

这是一个 Home Assistant 分支，通过移除有问题的依赖解决了 macOS ARM64 环境下 lru-dict 编译问题。支持多个 Home Assistant 版本，针对不同 Python 环境优化了分支结构。

**最初为 [LifeSmart 集成](https://github.com/MapleEve/lifesmart-HACS-for-hass) 而创建 - 一个全面的 Home Assistant LifeSmart 智能家居设备集成！**

### 分支结构

| 分支 | Home Assistant 版本 | Python 版本 | 用途 |
|------|-------------------|-------------|------|
| `macos-fix-branch` | 2023.6.0 | 3.11 | Python 3.11 环境的主要 macOS ARM64 修复 |
| `py310-fix-branch` | 2022.10.0 | 3.10 | Python 3.10 环境的 macOS ARM64 修复 |

### 主要更改

- **移除 lru-dict 依赖**: 消除 macOS ARM64 上的编译问题
- **优化包约束**: 更新依赖管理以提高兼容性
- **多版本支持**: 为不同 HA/Python 组合提供独立分支

### 使用方法

#### Python 3.11 + HA 2023.6.0:
```bash
pip install git+https://github.com/MapleEve/homeassistant-lru-dict-macos-fix.git@macos-fix-branch
```

#### Python 3.10 + HA 2022.10.0:
```bash
pip install git+https://github.com/MapleEve/homeassistant-lru-dict-macos-fix.git@py310-fix-branch
```

### 配套仓库

此分支与以下仓库配合使用:
- [pytest-homeassistant-custom-component-fixed](https://github.com/MapleEve/pytest-homeassistant-custom-component-fixed)

### 🏠 重点项目：LifeSmart 集成

此分支专门为支持 **[LifeSmart Home Assistant 集成](https://github.com/MapleEve/lifesmart-HACS-for-hass)** 的全面测试而创建。

#### 什么是 LifeSmart 集成？
一个强大的 Home Assistant 集成，将 LifeSmart 智能家居生态系统带入您的 Home Assistant 设置：

- **🔌 全面的设备支持**: 灯光、开关、传感器、气候控制、窗帘等
- **☁️ 多种连接方式**: 支持本地 TCP、WebSocket 和 OpenAPI
- **🎯 高级功能**: 场景管理、实时状态更新和设备发现
- **🧪 健壮的测试**: 跨 HA 版本 2022.10.0 到最新版本的多环境 CI/CD 测试
- **📱 简易安装**: 通过 HACS (Home Assistant Community Store) 可用

**[⭐ 为 LifeSmart 集成仓库点星标](https://github.com/MapleEve/lifesmart-HACS-for-hass)** 以获取最新功能和改进！

### 原始仓库

基于 [home-assistant/core](https://github.com/home-assistant/core)

---

### Technical Details | 技术细节

#### Changes Made | 所做更改

1. **lru-dict Dependency Removal | lru-dict 依赖移除**
   - Removed from `requirements.txt`
   - Removed from `homeassistant/package_constraints.txt`
   - Prevents compilation conflicts on macOS ARM64

2. **Version-Specific Optimization | 版本特定优化**
   - `py310-fix-branch`: Based on HA 2022.10.0 tag
   - `macos-fix-branch`: Based on HA 2023.6.0 with fixes

#### Compatibility Matrix | 兼容性矩阵

| Environment | Branch | pytest Plugin | Status |
|-------------|--------|---------------|--------|
| macOS ARM64 + Python 3.10 | `py310-fix-branch` | `py310-fix-branch` | ✅ Working |
| macOS ARM64 + Python 3.11 | `macos-fix-branch` | `macos-fix-branch` | ✅ Working |

#### Used by LifeSmart Integration Testing | 用于 LifeSmart 集成测试

This dual-fork solution enables comprehensive testing of the LifeSmart integration across:
- **5 different HA versions**: 2022.10.0, 2023.6.0, 2024.2.0, 2024.12.0, latest
- **4 Python versions**: 3.10, 3.11, 3.12, 3.13
- **Multiple test categories**: Unit tests, integration tests, platform-specific tests

此双分支解决方案支持 LifeSmart 集成的全面测试：
- **5 个不同的 HA 版本**: 2022.10.0, 2023.6.0, 2024.2.0, 2024.12.0, latest
- **4 个 Python 版本**: 3.10, 3.11, 3.12, 3.13  
- **多种测试类别**: 单元测试、集成测试、平台特定测试

### Contributing | 贡献

This fork is specifically designed for LifeSmart integration testing. For general Home Assistant contributions, please use the [official repository](https://github.com/home-assistant/core).

If you're interested in LifeSmart devices and Home Assistant, check out the **[LifeSmart Integration project](https://github.com/MapleEve/lifesmart-HACS-for-hass)**!

此分支专为 LifeSmart 集成测试设计。如需对 Home Assistant 进行一般性贡献，请使用[官方仓库](https://github.com/home-assistant/core)。

如果您对 LifeSmart 设备和 Home Assistant 感兴趣，请查看 **[LifeSmart 集成项目](https://github.com/MapleEve/lifesmart-HACS-for-hass)**！