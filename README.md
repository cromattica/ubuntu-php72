# Docker Image Ubuntu 18.04 

[![](https://images.microbadger.com/badges/version/cromattica/ubuntu-php72.svg)](https://microbadger.com/images/cromattica/ubuntu-php72 "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/cromattica/ubuntu-php72.svg)](https://microbadger.com/images/cromattica/ubuntu-php72 "Get your own image badge on microbadger.com")


Docker image based on Ubuntu 18.04 with PHP-7.2

## Getting Started

Use this image to test Symfony Project in Bitbucket Pipelines with all the packages you need already installed.

### Prerequisites

Enable Bitbucket Pipelines and add the file `bitbucket-pipelines.yml` to the root of your project.

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```yml
image: cromattica/ubuntu-php72

pipelines:

  branches:
    develop:
      - step:
          caches:
            - composer
          deployment: test
          script:
            - composer install --no-interaction --no-progress --prefer-dist
            - ./vendor/bin/simple-phpunit
```

### Test locally

If you want to test locally the image run the next command:

```
docker build ./
```

## Deployment

If you want to fork it and to add something else, you also have to upload to Docker Hub.

## Contributing

Please feel free to open an issue or a pull request.

## Authors

- **Miguel Ángel Martín** - [@miguelbemartin](https://twitter.com/miguelbemartin)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
