FROM nginx:alpine

# Remove default config
RUN rm /etc/nginx/conf.d/default.conf

# Add our custom config
COPY nginx/default.conf /etc/nginx/conf.d/default.conf

# Copy CA cert into web folder
COPY certs/ca.crt /usr/share/nginx/html/ca.crt

EXPOSE 80