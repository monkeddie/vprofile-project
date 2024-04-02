FROM nginx
LABEL "Project"="Vprofile"
LABEL "Author"="Eddie"

RUN rm -rf /etc/nginx/conf.d/vproapp.conf
# Copy your custom configuration file into the container and rename it
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf