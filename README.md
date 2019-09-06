# docker-registry-cleanup
Cleanup your docker registry and only keep the 3 (can be configured) latest images.

## Installation
There are 2 cronjobs, one which will use [Deckschrubber](https://github.com/fraunhoferfokus/deckschrubber) to annotate images for deletion and one to run the Docker registry garbage-collect on a different time.

! Note that this will keep only the 3 latest tag of each registry image. You can change this in the cleanup-tags.yml file.

```
kubectl apply -f kubernetes/
```
