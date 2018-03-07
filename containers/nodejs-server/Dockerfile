FROM node:latest

RUN mkdir -p /var/www/api

# Copy source code
COPY ./src /var/www/api

WORKDIR /var/www/api

# Install dependencies
RUN cd /var/www/api; npm install
RUN chmod -R 755 /var/www/api

EXPOSE 5003
CMD ["npm", "start"]
