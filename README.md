# Firefly Framework - IDP - AWS Cognito

[![CI](https://github.com/fireflyframework/fireflyframework-idp-aws-cognito/actions/workflows/ci.yml/badge.svg)](https://github.com/fireflyframework/fireflyframework-idp-aws-cognito/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Java](https://img.shields.io/badge/Java-21%2B-orange.svg)](https://openjdk.org)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-green.svg)](https://spring.io/projects/spring-boot)

> AWS Cognito implementation of the Firefly IDP adapter for user management and authentication.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## Overview

Firefly Framework IDP AWS Cognito implements the `IdpAdapter` interface using Amazon Cognito as the identity provider. It provides user management, authentication, token operations, and role management through the AWS Cognito User Pools API.

The module includes `CognitoIdpAdapter` as the main adapter implementation, backed by `CognitoUserService` for user operations and `CognitoAdminService` for administrative functions. It features automatic secret hash calculation for Cognito app clients with client secrets and configurable Cognito client factory for connection management.

## Features

- Full `IdpAdapter` implementation using AWS Cognito User Pools
- User creation, update, and password management via Cognito API
- Authentication with username/password and token refresh
- Admin service for user management operations
- Configurable Cognito client factory with connection pooling
- Automatic secret hash calculation for app client authentication
- Configurable via `CognitoProperties`

## Requirements

- Java 21+
- Spring Boot 3.x
- Maven 3.9+
- AWS account with Cognito User Pool configured

## Installation

```xml
<dependency>
    <groupId>org.fireflyframework</groupId>
    <artifactId>fireflyframework-idp-aws-cognito</artifactId>
    <version>26.02.07</version>
</dependency>
```

## Quick Start

```xml
<dependencies>
    <dependency>
        <groupId>org.fireflyframework</groupId>
        <artifactId>fireflyframework-idp</artifactId>
    </dependency>
    <dependency>
        <groupId>org.fireflyframework</groupId>
        <artifactId>fireflyframework-idp-aws-cognito</artifactId>
    </dependency>
</dependencies>
```

## Configuration

```yaml
firefly:
  idp:
    cognito:
      user-pool-id: us-east-1_xxxxxxxxx
      client-id: your-app-client-id
      client-secret: your-app-client-secret
      region: us-east-1
```

## Documentation

No additional documentation available for this project.

## Contributing

Contributions are welcome. Please read the [CONTRIBUTING.md](CONTRIBUTING.md) guide for details on our code of conduct, development process, and how to submit pull requests.

## License

Copyright 2024-2026 Firefly Software Foundation.

Licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE) for details.
