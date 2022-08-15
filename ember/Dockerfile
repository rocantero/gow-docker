FROM node:12
MAINTAINER Rodrigo Cantero "rodrigo@mbkj.dev"

USER root

#============================================
# Cleanup
#============================================
RUN rm -rf /var/lib/apt/lists/* \
    /var/cache/apt/* 
#============================================
# Global Node.js packages
#============================================
# - ember-cli: the main protagonist of this
#     Docker image.
#============================================
RUN yarn global add ember-cli@2.17.2

# Install software 
RUN apt-get install -y git
# Make ssh dir
# RUN mkdir /root/.ssh/

# Copy over private key, and set permissions
# Warning! Anyone who gets their hands on this image will be able
# to retrieve this private key file from the corresponding image layer
#ADD id_ed25519 /root/.ssh/id_rsa

# Create known_hosts
#RUN touch /root/.ssh/known_hosts
# Add bitbuckets key
#RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

# Clone the conf files into the docker container
#RUN rm -rf /myapp/*
#RUN git clone -b demo git@github.com:mbkjdev/gow-web.git /myapp
WORKDIR /app
RUN chmod -R 777 .

# RUN rm -rf node_modules package-lock.json

#============================================
# Run the whole thing as non-root from now on
#============================================

#============================================
# Default working directory
#============================================
# RUN yarn
#============================================
# Ports being listened for connections
#============================================
# - 4200: devserver. You can access your app
#     here.
# - 7020: livereload. Your app, while on 
#     development, will try to connect to
#     this port. It will listen for a signal
#     coming from the server indicating that
#     something has changed and the browser
#     needs a refresh.
# - 7357: TestEm. You can connect to this
#     port with your preferred browser and
#     tests will run there automatically
#     (besides Google Chrome), 
#============================================
EXPOSE 4200 7020 7357

USER node

ENTRYPOINT ["tail", "-f", "/dev/null"]