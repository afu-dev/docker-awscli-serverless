# Docker AwsCli + Serverless

A docker image for running serverless command (with aws-cli) available on [DockerHub](https://hub.docker.com/r/chtiadrien/awscli-serverless).

## Packages Versions

```bash
$ node --version
v15.8.0

$ serverless --version
Framework Core: 2.44.0
Plugin: 5.2.0
SDK: 4.2.3
Components: 3.11.0

$ aws --version
aws-cli/2.2.9 Python/3.8.8 Linux/5.10.25-linuxkit exe/x86_64.debian.9 prompt/off
```

## Usage

Don't forget to populate the `.aws` folder with your configuration and credentials. Or you can run `aws configure` from the container.

```console
# Populate config files (from the container)
$ cat <<EOT > ~/.aws/config
[default]
region = eu-west-3
output = json
EOT
$ cat <<EOT > ~/.aws/credentials
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
