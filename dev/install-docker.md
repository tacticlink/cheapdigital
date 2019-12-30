## Install docker with scripts

- Step1: Copy the scripts,make a new file named 'docker.sh'
- Step2: Make the newly created file excutable.
- Step3: Run scripts.

	# or install on Ubuntu Linux with scripts

	#!/bin/sh

	set -eu

	# Docker
	sudo apt remove --yes docker docker-engine docker.io \
	&& sudo apt-get update \
	&& sudo apt-get --yes --no-install-recommends install \
	apt-transport-https \
	ca-certificates \
	&& wget --quiet --output-document=- https://download.docker.com/linux/ubuntu/gpg \
	| sudo apt-key add - \
	&& sudo add-apt-repository \
	"deb [arch=$(dpkg --print-architecture)] https://download.docker.com/linux/ubuntu \
	$(lsb_release --codename --short) \
	stable" \
	&& sudo apt-get update \
	&& sudo apt-get --yes --no-install-recommends install docker-ce \
	&& sudo usermod -aG docker $USER \
	&& sudo systemctl enable docker \
	&& printf '\nDocker installed successfully\n\n'

	printf 'Waiting for Docker to start...\n\n'
	sleep 3


	# First save scripts 'docker.sh' in a directory, then in that directory,run

	sudo chmod +x docker.sh

	# Run the script 
	sudo ./docker.sh  
