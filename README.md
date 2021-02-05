# dockerImageReader
Docker Registry Image Reader (Postman)

## Scope
Mini-project done for a Postman hackaton https://postman-hack.devpost.com/
It is a simple Postman Collection that can be runned in a Postman Monitor (scheduled API calls) to read image data from a Docker Registry.

## Inspiration
I felt the necessity to automate some checks that can be done on a private Docker registry given the growth of the number or docker images/version in each company in the latest years. I've created just a couple of automated request but I think the results could already be effective

## What it does
This project interacts with the Docker Registry HTTP API (v2), allowing the management of docker images on your registry via Rest API instead of docker command.

This may be useful if you can't use the docker command directly in some environments, or if you want some automation to check/pull images when a new version is released on your registry. By using a Postman Monitor, the first scheduled request will fetch all images from your registry and then the second request will run in a loop, sending the images current tag to a webhook of your choice.
