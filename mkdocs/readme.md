# Mkdocs #
[mkdocs](http://www.mkdocs.org/) is a python based documentation system that utilizes a series of markdown files to build a well formated site that is focused on documentation.

## Run ##
This requires the use of volumes to mount the document folder.
```shell
docker run --name documents -v /path/to/documents:/documents moird/mkdocs
```

## Mkdocs Initialization ##
Mkdocs can be initialized with the container, it doesn't need to be started first.
```shell
docker run -v /documents moird/mkdocs mkdocs new .
```

## Mkdocs Configuration ##
the mkdocs.yaml file is the primary source of configuration for mkdocs, you can specify the pages layout, and additional settings like port.  It is suggested to set at least the dev_addr to 9010:
```shell
dev_addr: 0.0.0.0:9010
```

For example the entire file might look like this:
```yaml
site_name: Dockerfile Documentation
repo_url: https://github.com/moird/dockerfiles
dev_addr: 0.0.0.0:9010

pages:
  - index.md
```
