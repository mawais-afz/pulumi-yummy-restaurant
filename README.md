
# Yummy Restaurant Cloud Infrastructure

A cloud infrastructure project for managing the Yummy Restaurant's cloud resources using Pulumi.

## Prerequisites

- [Pulumi CLI](https://www.pulumi.com/docs/get-started/install/)
- [Node.js](https://nodejs.org/) (version 14.x or later)
- Cloud provider credentials configured (AWS)

## Project Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/pulumi-yummy-restaurant.git
    cd pulumi-yummy-restaurant
    ```

2. Configure Pulumi stack:

    ```bash
    pulumi stack init dev
    ```

3. Set up configuration variables:

    ```bash
    pulumi config set cloud:region us-west-2  # Replace with your desired region
    ```

## Project Structure

```
pulumi-yummy-restaurant/
├── /www           # Main infrastructure code
├── package.json       # Project dependencies
├── tsconfig.json     # TypeScript configuration
├── Pulumi.dev.yaml       # Pulumi dev environment configuration
└── Pulumi.yaml       # Pulumi project configuration
```

## Available Commands

- Deploy infrastructure:

    ```bash
    pulumi up
    ```

- Destroy infrastructure:

    ```bash
    pulumi destroy
    ```

- View stack outputs:

    ```bash
    pulumi stack output
    ```

## Infrastructure Components

This project manages the following cloud resources:

- Amazon S3 Bucket configured as a static website
- S3 Bucket ownership controls and public access settings
- Synced folder configuration to manage website files
- Amazon CloudFront Distribution with:
  - Origin configuration pointing to S3 website
  - Default cache behavior with HTTPS redirect
  - Custom error responses
  - Viewer certificate
  - Geo-restriction settings
  - Price class configuration

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request
