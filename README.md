# spectr-build-docker
Dockerfile for creating a Docker image in which to build spectr.

To build docker image:
```
sudo docker image build -t mriffle/build-spectr ./
```
To build spectr:
```
sudo docker run --rm -it --user $(id -u):$(id -g) -v `pwd`:`pwd` -w `pwd` --env HOME=. --entrypoint ant mriffle/build-spectr -f ant_build_all_create_download_zip_file.xml
```
