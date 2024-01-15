# Introduction

This article shows the basic steps for deployment of the PostgreSQL on Ubuntu v22

# Deployment

## Deployment using APT-GET

Source documentation for intall
Source documentation for install can be found by the link
https://www.postgresql.org/download/ with selection of the required operational system or directly for Ubuntu by the link https://www.postgresql.org/download/linux/ubuntu/

Must have requirement is the functional internet connection.
Then the following steps should be taken

### Create the file repository configuration:

''' sudo sh -c 'echo "deb https://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list '''

### Import the repository signing key:

''' wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add - '''

### Update the package lists:

''' sudo apt-get update '''

### Install the latest version of PostgreSQL.

If you want a specific version, use 'postgresql-12' or similar instead of 'postgresql':
''' sudo apt-get -y install postgresql '''
