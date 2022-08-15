FROM proactivehk/grails

MAINTAINER Rodrigo Cantero "rodrigo@mbkj.dev"

# Update aptitude with new repo
RUN apt-get update

# Install software 
# RUN apt-get install -y git
# Make ssh dir

# Copy over private key, and set permissions
# Warning! Anyone who gets their hands on this image will be able
# to retrieve this private key file from the corresponding image layer
# ADD id_ed25519 /root/.ssh/id_rsa

# Create known_hosts
# RUN touch /root/.ssh/known_hosts
# Add bitbuckets key
# RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

# Clone the conf files into the docker container
# RUN git clone git@github.com:mbkjdev/gow-api.git

# RUN cd gow-api
# RUN grails run-app

# CMD ["grails", "run-app"]