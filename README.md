# Nimbus Beacon docker fork

## CI Instructions
- To trigger the CI, go to actions > workflows on the left > Build nimbus-eth2 docker image > Run workflow > enter values and hit run


To get Nimbus running in Docker, from arbitrary source checkout.

Custom configuration can be added with `-d:const_preset=/root/config.yaml` in the dockerfile.

Adapted from the Nimbus Dockerfile.

*Experimental software, use at own risk*

Git clone nimbus into `./nimbus-eth2`

Example usage:

```bash
cd nimbus-eth2
git checkout stable
git pull
make -j8 update
cd ..
docker build -t protolambda/nimbus:latest .
```


