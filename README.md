# Node.js Service Template

A Backstage template for creating Node.js microservices.

## Features

This template creates a new Node.js service with:
- Basic Express.js setup
- Package.json with common dependencies
- Backstage catalog-info.yaml for service registration
- Ready-to-deploy structure

## Using this Template

This template is automatically discovered by Backstage through GitHub integration.

### Prerequisites
- Backstage instance with GitHub integration
- GitHub App configured for repository creation

### Parameters

- **Name**: The name of your service (will be used in package.json and catalog-info.yaml)
- **Repository Location**: Where to create the new repository (defaults to open-service-portal organization)

## Development

To test changes to this template locally:

1. Reference it in your Backstage app-config.yaml:
```yaml
catalog:
  locations:
    - type: url
      target: https://github.com/open-service-portal/service-nodejs-template/blob/main/template.yaml
      rules:
        - allow: [Template]
```

2. Navigate to `/create` in your Backstage instance
3. The template should appear in the template list

## Template Structure

```
.
├── template.yaml          # Template definition
├── content/              # Files to be scaffolded
│   ├── catalog-info.yaml # Backstage catalog info
│   ├── package.json      # Node.js package definition
│   └── index.js          # Main application file
└── README.md            # This file
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.