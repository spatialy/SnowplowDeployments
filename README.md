# SnowplowDeployments
Files needed to deploy Snowplow to docker
## Building
To build the docker containers you should check out snowplow from github. And next to snowplow you should check out this repo.
### Building scala-collector
Build the scala-collector by following the instructions in the project.
Move into the scalacollector directory of this repo.
Do a `docker run -t scala-collector .`


### Building stream enricher 
Build the stream enricher by following the instructions in the project.
Move into the stream-enrich directory of this repo.
Do a `docker run -t stream-enrich .`

## Deploying the iglu repo
The iglu repo can be added to s3 and exposed as a website. Whereever you deploy this should be configured in the stream-enrich/configuration/enrichments/ directory

# tips and tricks
To compile snowplow I use 
https://github.com/paulp/sbt-extras/
`~/bin/sbt -v -210 compile`
