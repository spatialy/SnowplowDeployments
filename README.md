# SnowplowDeployments
Files needed to deploy Snowplow to docker
## Building
To build the docker containers you should check out the snowplow submodule from github.
### Building scala-collector
Build the scala-collector by following the instructions in the project.
Do a `docker build  -f Dockerfile-scalacollector -t scala-collector . `


### Building stream enricher 
Build the stream enricher by following the instructions in the project.
Move into the stream-enrich directory of this repo.
Do a `docker build  -f Dockerfile-stream-enrich -t stream-enrich .`

## Deploying the iglu repo
The iglu repo can be added to s3 and exposed as a website. Whereever you deploy this should be configured in the stream-enrich/configuration/resolver.json

# tips and tricks
To compile snowplow I use 
https://github.com/paulp/sbt-extras/
`~/bin/sbt -v -210 assembly`
