# n8n Automation Workflows

A collection of custom n8n automation workflows I've built for various personal and professional use cases.

## About

This repository contains workflow definitions that can be imported directly into [n8n](https://n8n.io/), an open-source workflow automation tool. Each workflow is designed to solve specific automation challenges and can be adapted for your own needs.

## Workflows

### [No Limits Track Days Events Aggregator](./workflows/nolimits-track-days-aggregator/)

Automated daily aggregation of UK track day availability from No Limits Track Days. Monitors 10 racing circuits, validates event data, and sends a formatted HTML email digest with availability alerts.

## Getting Started

### Prerequisites

- An n8n instance (self-hosted or cloud)
- Basic understanding of n8n workflows

### Importing Workflows

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select the `.json` workflow file from this repository
4. Configure any required credentials (SMTP, API keys, etc.)
5. Update workflow-specific settings (email addresses, endpoints, etc.)
6. Test the workflow before activating

## Structure

```
n8n-automations/
├── workflows/
│ └── [workflow-name]/
│ ├── README.md # Workflow documentation
│ └── [workflow-name].json # n8n workflow definition
└── README.md # This file
```

## Notes

- **Credentials:** Workflow files do not contain actual credentials. You'll need to configure your own API keys, SMTP settings, etc.
- **Personal Information:** Email addresses and other personal data have been replaced with placeholders
- **Customization:** All workflows are designed to be easily customized for your specific needs

## Contributing

Feel free to fork this repository and adapt these workflows for your own use. If you create improvements or interesting variants, pull requests are welcome!

## License

MIT License - see [LICENSE](./LICENSE) file for details. Feel free to use, modify, and distribute these workflows as needed.
