<div align="center">

# OpenArmor Architecture

<img src="assets/openarmor_logo.gif" alt="OpenArmor HIDS Logo" width="200"/>

**Made with 🛡️ by the OpenArmor community**

[Website](https://www.theopenarmor.org) • [Docs](https://www.theopenarmor.org/docs/) • [Downloads](https://www.theopenarmor.org/downloads/) • [Community](https://discord.gg/BXzM75Xzq7)
</div>



This repository contains the architectural diagrams and documentation for the OpenArmor project, an advanced open-source security platform.

## 🏗️ Repository Structure

Our repository is organized into several key components:

- FIM/db
- centralized_configuration
- data_provider
- dbsync
- metrics
- openarmor-db
- router-pubsub
- syscollector
- vulnerability-scanner/policyManager
- wm_azure
- wm_ciscat
- wm_gcp
- wm_github
- wm_office365
- wm_sca

Each directory contains PlantUML files that describe the architecture and workflows of the respective components.

## 🚀 Getting Started

To view the architectural diagrams:

1. Clone this repository:
   ```
   git clone https://github.com/openarmor/openarmor-architecture.git
   ```
2. Navigate to the specific component you're interested in.
3. Open the PlantUML files using a PlantUML viewer or editor.

## 🛠️ Components Overview

- **FIM/db**: File Integrity Monitoring database architecture
- **centralized_configuration**: Centralized configuration management system
- **data_provider**: Data ingestion and processing pipeline
- **dbsync**: Database synchronization mechanisms
- **metrics**: Performance and operational metrics collection
- **openarmor-db**: Main database architecture for OpenArmor
- **router-pubsub**: Publish-subscribe routing system
- **syscollector**: System information collection module
- **vulnerability-scanner/policyManager**: Vulnerability scanning and policy management
- **wm_azure**, **wm_gcp**, **wm_github**, **wm_office365**: Cloud service integrations
- **wm_ciscat**: CIS-CAT (Center for Internet Security Configuration Assessment Tool) integration
- **wm_sca**: Security Configuration Assessment module

## 📚 Documentation

For detailed documentation on each component and the overall OpenArmor architecture, please visit our [official documentation](https://docs.openarmor.org).

## 🤝 Contributing

We welcome contributions to improve our architecture and documentation. Please see our [CONTRIBUTING.md](CONTRIBUTING.md) file for guidelines on how to submit changes.

## 📞 Contact

For questions or support, please join our community channels:

- [Discord](https://discord.gg/openarmor)
- [Slack](https://openarmor.slack.com) (Invite: slack@theopenarmor.org)

---

