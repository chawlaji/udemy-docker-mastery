# create your custom drupal image here, based of official drupal

FROM drupal:8.2

Run apt-get update && apt-get install -y git \ 
    && rm -rf /var/lib/apt/lists/*

# "\" is used to continue command in next line
#  "&&" execute next command if previous runs successfully

WORKDIR /var/www/html/themes

#git options for absolutly latest branch 
#with no previous record for commits and changes,saves space and time
RUN git clone --branch 8.x-3.x --single-branch \
 --depth 1 https://git.drupal.org/project/bootstrap.git \
 && chown -R www-data:www-data bootstrap
# chown -> change owner  -r -> all files
WORKDIR /var/www/html 

