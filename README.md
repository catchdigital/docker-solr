# Docker Solr

This is currently version 4.5.1 of Solr to match the version Acquia uses. It
has a core available called collection1.

You must symlink the config files to the container for your project. See example below.

## Adding to docker-compose.yml

```
solr:
    image: catchdigital/solr:4.5.1
    volumes:
      - ./docroot/modules/contrib/search_api_solr/solr-conf/4.x:/opt/solr/example/solr/collection1/conf:cached
    ports:
      - 8983:8983
```
  