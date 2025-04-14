<div align="center">
  <img src="https://cdn.yobc.de/assets/np-poster.png" alt="nodepass" width="500">

[![GitHub release](https://img.shields.io/github/v/release/yosebyte/nodepass)](https://github.com/yosebyte/nodepass/releases)
[![Go Report Card](https://goreportcard.com/badge/github.com/yosebyte/nodepass)](https://goreportcard.com/report/github.com/yosebyte/nodepass)
![GitHub last commit](https://img.shields.io/github/last-commit/yosebyte/nodepass)

English | [简体中文](README_zh.md)
</div>

NodePass is an elegant, efficient TCP tunneling solution that creates secure communication bridges between network endpoints. By establishing a TCP control channel, NodePass facilitates seamless data transfer through otherwise restricted network environments while offering configurable security options for the data channel. Its server-client architecture allows for flexible deployment scenarios, enabling access to services across firewalls, NATs, and other network barriers. With its intelligent connection pooling, minimal resource footprint, and straightforward command syntax, NodePass provides developers and system administrators with a powerful yet easy-to-use tool for solving complex networking challenges without compromising on security or performance.

## 📋 Key Features

- **🔀 Multiple Operating Modes**
  - Server mode accepting incoming tunnels with configurable security
  - Client mode for establishing outbound connections to tunnel servers
  - Master mode with RESTful API for dynamic instance management

- **🌍 Protocol Support**
  - TCP tunneling with persistent connection handling
  - UDP datagram forwarding with configurable buffer sizes
  - Intelligent routing mechanisms for both protocols

- **🛡️ Security Options**
  - TLS Mode 0: Unencrypted mode for maximum speed in trusted networks
  - TLS Mode 1: Self-signed certificates for quick secure setup
  - TLS Mode 2: Custom certificate validation for enterprise security

- **⚡ Performance Features**
  - Smart connection pooling with real-time capacity adaptation
  - Dynamic interval adjustment based on network conditions
  - Minimal resource footprint even under heavy load
  - Automatic recovery from network disruptions

- **🧰 Simple Configuration**
  - Zero configuration files required
  - Simple command-line parameters
  - Environment variables for fine-tuning performance
  - Intelligent defaults for most use cases

## 📋 Quick Start

### 📥 Installation

- **Pre-built Binaries**: Download from [releases page](https://github.com/yosebyte/nodepass/releases).
- **Go Install**: `go install github.com/yosebyte/nodepass/cmd/nodepass@latest`
- **Container Image**: `docker pull ghcr.io/yosebyte/nodepass:latest`
- **Management Script**: `bash <(curl -sL https://cdn.yobc.de/shell/nodepass.sh)`

### 🚀 Basic Usage

**Server Mode**
```bash
nodepass "server://:10101/127.0.0.1:8080?log=debug&tls=1"
```

**Client Mode**
```bash
nodepass client://server.example.com:10101/127.0.0.1:8080
```

**Master Mode (API)**
```bash
nodepass "master://:10101/api?log=debug&tls=1"
```

## 🔧 Common Use Cases

- **Remote Access**: Securely access internal services from external locations
- **Firewall Bypass**: Navigate through restrictive network environments
- **Secure Microservices**: Establish encrypted channels between distributed components
- **Database Protection**: Enable secure database access while keeping servers isolated
- **IoT Communication**: Connect devices across different network segments

## 📚 Documentation

Explore the complete documentation to learn more about NodePass:

- [Installation Guide](/docs/en/installation.md)
- [Usage Instructions](/docs/en/usage.md)
- [Configuration Options](/docs/en/configuration.md)
- [API Reference](/docs/en/api.md)
- [Examples](/docs/en/examples.md)
- [How It Works](/docs/en/how-it-works.md)
- [Troubleshooting](/docs/en/troubleshooting.md)

## 👥 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

## 💬 Discussion

Join our [discussions](https://github.com/yosebyte/nodepass/discussions) to share your experiences and ideas.

## 📄 License

Project `NodePass` is licensed under the [MIT LICENSE](LICENSE).

## ⭐ Stargazers

[![Stargazers over time](https://starchart.cc/yosebyte/nodepass.svg?variant=adaptive)](https://starchart.cc/yosebyte/nodepass)
