# Building the build container

```
docker build -t wpcd-builder -f Dockerfile.build .
docker run --rm -ti -v $PWD:/usr/src/wordpress-cd-s3 wpcd-builder python setup.py sdist
docker build -t rossigee/wordpress-cd-s3 .
docker push rossigee/wordpress-cd-s3
```

