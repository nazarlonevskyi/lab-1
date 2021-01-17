***
**1.** Read about docker-compose
***
**2.** Read about flask
***
**5.** Create my_app , tests Read what in files
***
**6.** Start project by this commands `pipenv --python 3.8` `pipenv install -r requirements.txt` `pipenv run python app.py`
***
**7.** Delete Pipfiles.
***
**8.** Makefile has some rules #app - run docker build for the Dockerfile.app #tests - run docker build for Dockerfile.tests #test-app - run test-app container #run - create network for docker container and run redis and app containers too. #docker-prune - removes and cleans unused containers, networks, volumes, images
***
**9.** Build and run app. Site works [link](https://prnt.sc/x2ig92) [link2](https://prnt.sc/x2iv84) [link3](https://prnt.sc/x2iv84)
***
**10.** Cleaned all resources in project using make docker-prune
***
**11.** Created pushing images to the Dockerhub `docker-push: @docker push $(REPO):app \&& docker push $(REPO):tests`
***
**12.** Created rule witch delete images `images-delete: @sudo docker image rm --force $(shell sudo docker images -q)`
***
**13.** Created docker-compose.yml
***
**14.** Run docker-compose using sudo docker-compose up
***
**15.** Page work on localhost:80
***
**16.** docker-compose has created image
***
**17.** sudo docker-compose down
***
**18.** Push images to DockerHub sudo docker-compose push
***
**19.** Docker-compose is better for using. This way is more for docker context and do more docer functions.
***
**20.** Create docker-compose for Lab_4 of Django project. Pushed to Docker hub lab-5
***
**21.** Fill README File and create pull request.
***

