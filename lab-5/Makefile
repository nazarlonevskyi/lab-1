STATES := app tests
REPO := nazarlonevskyi/lab-5

.PHONY: $(STATES)

$(STATES):
	@sudo docker build -f Dockerfile.$(@) -t $(REPO):$(@) .

run:
	@docker network create --driver=bridge appnet \
	&& docker run --rm --name redis --net=appnet -d redis \
	&& docker run --rm --name app --net=appnet -p 5000:5000 -d $(REPO):app

test-app:
	@ sudo docker run --rm -it --name test --net=appnet $(REPO):tests

docker-prune:
	@sudo docker rm $$(sudo docker ps -a -q) --force || true \
	&& sudo docker container prune --force \
	&& sudo docker volume prune --force \
	&& sudo docker network prune --force \
	&& sudo docker image prune --force

docker-push:
	@docker push $(REPO):app \
	&& docker push $(REPO):tests

images-delete:
	@sudo docker image rm --force $(shell sudo docker images -q)

