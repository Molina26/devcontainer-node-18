# Use an official Node runtime as the base image
FROM node:18-alpine

# Update the package list and install the following dependencies
RUN apk update

# install git, curl, wget, and unzip
RUN apk add --no-cache git curl wget unzip less man-db

# install neovim
RUN apk add --no-cache neovim

# install bash
RUN apk add --no-cache bash

# Install Starship
RUN sh -c "$(curl -fsSL https://starship.rs/install.sh)" -- -y

# Copy config/starship.toml to the container
COPY config/starship.toml ~/.config/starship.toml

RUN echo 'eval "$(starship init bash)"' >> ~/.bashrc

# Set the working directory in the container to /app
WORKDIR /app

# Add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# this section you can add any other global packages you want to install
# npm install -g <package-name>

# Copy package.json and package-lock.json to the working directory
COPY package*.json /app/

# Copy the current directory contents into the container at /app
COPY . /app
