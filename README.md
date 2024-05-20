
# Rocket Bank UI

This project serves as the GUI for the [Rocket Bank Spring Boot API](https://github.com/TevinDeale/rocket-bank-spring-boot-banking-api), and uses the [Proxy-Cognito Auth Server](https://github.com/TevinDeale/proxy-cognito-authentication-server) to authenticate users and send requests to the API. 


## Tech Stack

![My Skills](https://skillicons.dev/icons?i=js,vue,docker,sass,pinia&perline=5)

## Features

- Create customer account
- Open savings or checking Account
- List accounts w/ balance
- Account overview dashboard
- Deposit or Withdraw Cash


## Demo

![Rocket Bank UI Demo](https://github.com/TevinDeale/rocket-bank-front-end/blob/main/readme_assets/rocketbankui_demo.gif)


## Deployment

This project can be ran locally or in a Docker container. Clone the repository and run the following commands.

#### Docker

```bash
  docker build -t rocketbankui:dev .
```
```bash
  docker run -p 5173:5173/tcp rocketbankui:dev .
```

#### Locally

```bash
  pnpm install
```
```bash
  pnpm dev
```

## Contributing

Contributions are always welcome!

If you would like to contribute, reach out via X [@FiinnDev](https://x.com/FiinnDev)


