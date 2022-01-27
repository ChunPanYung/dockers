# Build time Variables
ARG EMAIL=email@localhost.lan
ARG DOMAIN=localhost

# docker build --tag nextcloud:casc .
FROM nextcloud
USER root
COPY setssl.sh /usr/local/bin
RUN chmod u+x /usr/local/bin/setssl.sh
RUN /usr/local/bin/setssl.sh $EMAIL $DOMAIN

