# 🌐 myLG - Network Diagnostics & Troubleshooting Toolkit

<div align="center">

[![Go Version](https://img.shields.io/badge/Go-1.12+-blue.svg)](https://golang.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Build Status](https://img.shields.io/travis/imransom29/mylg.svg)](https://travis-ci.org/imransom29/mylg)
[![Docker](https://img.shields.io/badge/Docker-Ready-blue.svg)](Dockerfile)

**A comprehensive open-source network diagnostic utility that combines multiple network probes into one powerful tool**

</div>

## 📋 Overview

myLG is an advanced network diagnostics and troubleshooting toolkit written in Go that consolidates various network monitoring and analysis functions into a single, efficient command-line interface. Designed for network administrators, DevOps engineers, and security professionals, myLG provides real-time insights into network performance, connectivity, and infrastructure health.

## ✨ Key Features

### 🔍 Network Diagnostics
- **Local ping and real-time traceroute** with visual feedback
- **HTTP/HTTPS ping** (GET, POST, HEAD methods) for web service monitoring
- **Packet analyzer** for TCP/IP and other network protocols
- **Port scanning** capabilities for security assessment
- **Network LAN Discovery** to identify devices on local networks

### 🌍 Global Network Intelligence
- **200+ countries DNS Lookup** information
- **Popular looking glasses** integration (Telia, Level3, NTT, Cogent, KPN)
- **BGP route visualization** through major network providers
- **RIPE database queries** (ASN, IP/CIDR information)
- **PeeringDB integration** for peering policy and network information

### 📊 Management & Monitoring
- **Quick NMS (Network Management System)** with SNMP support
- **Internet Speed Test** for bandwidth analysis
- **Web dashboard** for visual monitoring and analytics
- **Real-time network statistics** and performance metrics

### 💻 Advanced CLI Features
- **Interactive shell** with vi and emacs mode support
- **CLI auto-complete** and command history
- **Configurable options** for customization
- **Direct shell access** to all diagnostic commands
- **Colorized output** for enhanced readability

## 🚀 Quick Start

### Prerequisites
- Go 1.12 or higher
- libpcap-dev (for packet capture functionality)

### Installation

#### From Source
```bash
git clone https://github.com/mehrdadrad/mylg.git
cd mylg
go build -o mylg mylg.go
sudo ./mylg
```

#### Using Docker
```bash
docker build -t mylg .
docker run -it --privileged mylg
```

#### Using Go Get
```bash
go get github.com/mehrdadrad/mylg
mylg
```

## 📖 Usage Examples

### Basic Network Diagnostics
```bash
# Ping a host
mylg> ping google.com

# Trace route to destination
mylg> trace 8.8.8.8

# HTTP ping with custom method
mylg> http ping https://api.github.com -m POST
```

### Looking Glass Integration
```bash
# Use Telia looking glass
mylg> lg telia ping 1.1.1.1

# BGP route query through Level3
mylg> lg level3 bgp 192.168.1.0/24
```

### Advanced Features
```bash
# Network discovery
mylg> disc 192.168.1.0/24

# Port scanning
mylg> scan example.com 80,443,22

# DNS lookup across multiple countries
mylg> ns example.com all

# Packet capture and analysis
mylg> packet eth0 tcp port 80
```

### Web Dashboard
```bash
# Start web dashboard
mylg> web start

# Access dashboard at http://localhost:8080
```

## 🏗️ Architecture

myLG is built with a modular architecture consisting of:

- **CLI Interface** (`cli/`) - Interactive command-line interface
- **Network Probes** (`icmp/`, `http/`) - Ping, traceroute, HTTP monitoring
- **Looking Glasses** (`lg/`) - Integration with major network providers
- **Packet Analysis** (`packet/`) - Network packet capture and analysis
- **Services** (`services/`) - Web dashboard and HTTP API
- **Network Discovery** (`disc/`) - LAN device discovery
- **Speed Testing** (`speedtest/`) - Bandwidth measurement

## 🛠️ Development

### Project Structure
```
mylg/
├── cli/          # Command-line interface
├── icmp/         # ICMP operations (ping, traceroute)
├── http/         # HTTP/HTTPS monitoring
├── lg/           # Looking glass integrations
├── packet/       # Packet capture and analysis
├── nms/          # Network management system
├── ns/           # DNS and name services
├── disc/         # Network discovery
├── scan/         # Port scanning
├── services/     # Web services and dashboard
├── speedtest/    # Internet speed testing
└── whois/        # WHOIS queries
```

### Running Tests
```bash
go test ./...
```

### Building
```bash
go build -o mylg mylg.go
```

## 🐳 Docker Support

A Dockerfile is provided for containerized deployments:

```bash
docker build -t mylg .
docker run -it --net=host --privileged mylg
```

## 📊 Configuration

myLG supports configuration through:
- Command-line flags
- Configuration files
- Environment variables
- Interactive CLI settings

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Thanks to all the network providers for their looking glass services
- The Go community for excellent networking libraries
- Contributors who help improve this tool

## 📞 Support

- 📧 Email: imransom29@gmail.com
- 🐛 Issues: [GitHub Issues](https://github.com/imransom29/mylg/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/imransom29/mylg/discussions)

## 🔗 Related Projects

- [myLG Web Dashboard](https://github.com/mehrdadrad/mylg-web)
- [Network Monitoring Tools](https://github.com/mehrdadrad/netmon)

---

<div align="center">

**⭐ Star this repository if it helped you!**

Made with ❤️ by [imransom29](https://github.com/imransom29)

</div>




