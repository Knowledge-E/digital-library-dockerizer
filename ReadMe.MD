1. Clone everything recursively
2. Create /home/${yourUser}/volumes/development/solr and apply proper permissions
3. Create /home/${yourUser}/volumes/development/fedora and apply proper permissions
3. Start
4 Create "openaccess" core within the solr docker container (bash into the container and)
    solr create -c openaccess

