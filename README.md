# Docker AwsCli + Serverless

A docker image for running serverless command (with aws-cli) available on [DockerHub](https://hub.docker.com/r/chtiadrien/awscli-serverless).

## Packages Versions

```bash
$ node --version
v12.16.1

$ serverless --version
Framework Core: 1.67.0
Plugin: 3.6.3
SDK: 2.3.0
Components: 2.28.0

$ aws --version
aws-cli/2.0.6 Python/3.7.3 Linux/4.19.76-linuxkit botocore/2.0.0dev10
```

## Usage

Don't forget to populate the `.aws` folder with your configuration and credentials. Or you can run `aws configure` from the container.

```console
# Populate config files (from the container)
cat <<EOT > ~/.aws/config
[default]
region = eu-west-3
output = json
EOT
cat <<EOT > ~/.aws/credentials
[default]
aws_access_key_id = my-access-key
aws_secret_access_key = my-secret-key
EOT

# or run the configure command (also from the container)
$ aws configure
AWS Access Key ID [None]: my-access-key
AWS Secret Access Key [None]: my-secret-key
Default region name [None]: eu-west-3
Default output format [None]: json
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md)
