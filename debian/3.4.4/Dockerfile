FROM debian:stretch
LABEL maintainer="stevenbetancurt@hotmail.com"

# Install Dependences
# More info https://cran.r-project.org/bin/linux/debian/
RUN apt-get update \ 
	&& apt-get install -y --no-install-recommends \
		apt-utils \		
		wget \		
		dirmngr \
		gnupg \		
	&& echo "deb http://cloud.r-project.org/bin/linux/debian stretch-cran34/" >> /etc/apt/sources.list \
	&& apt-key adv --keyserver hkp://keys.gnupg.net:80 --recv-key 'E19F5F87128899B192B1A2C2AD5F960A256A04AF' \
	&& apt-get update \ 
	&& apt-get install -y --no-install-recommends \	
		r-base \
		r-base-dev \
	&& mkdir /root/project

# docker image build .\debian\ --tag stevensotelo/r_debian:3.4.4
# docker container run -it --name r_base stevensotelo/r_debian:3.4.4