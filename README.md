# digital-library-dockerizer

1. Clone everything recursively
2. Create /home/${yourUser}/volumes/development/solr and apply proper permissions
3. Create /home/${yourUser}/volumes/development/fedora and apply proper permissions
3. Start
4 Create "openaccess" core within the solr docker container (bash into the container and)
    solr create -c openaccess

Using solr UI, you are able to perform the search across everything, however when you start
specifying phrases for query, you will notice that you can search only one field at the time.

In order to search multiple fields at once, you need to use DisMax query parses in following manner:
http://localhost:8984/solr/newcore/select?defType=dismax&q=iPod&qf=features+text+name&fl=*,score