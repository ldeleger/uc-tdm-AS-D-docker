# uc-tdm-AS-D-docker

This component is the workflow for the OpenMinTeD AS-D use case.

## test-data
The test-data folder contains data to run the workflow. More specifically:
* corpus/ contains text samples that can be used as input.
* output/ is where the output of the workflow will be created.

## Run in command-line

To run the workflow (from the folder containing the README):

```docker run -i --rm -v $PWD/test-data/:/as-d/data ldeleger/uc-tdm-as-d-docker alvisnlp -J-Xmx30g -alias input /as-d/data/corpus/test.xml -outputDir /as-d/data/output plans/tag_pubmed.plan```

## OpenMinteD metadata

The OpenMinteD metadata are recorded in the following [XML file](as-d.metadata.xml)

## Re-build the docker image

```docker build . -t ldeleger/uc-tdm-as-d-docker -f Dockerfile```
