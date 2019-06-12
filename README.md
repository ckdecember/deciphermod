# Decipher

## Overview

Dockerized and AWS hosted Flask app to decipher messy handwriting to predict most likely word choice. Please [contact me](mailto:mevanoff24@gmail.com) if you need to use the deployed application, since the EC2 instance is currently down.  

You can see my presentation [here](https://docs.google.com/presentation/d/1zYfLiZooCKe1LT3e8FkTNU39ZUZoNQfaUbTzMXQ1yn4/edit#slide=id.p)


## Motivation for this project
Have you ever read handwritten text when you came across an indecipherable word? This is a big issue in pharmacies mis-prescribing medicine, maintenance workers mis-communicating results, or even reading lecture notes. The use cases for predicting messy handwriting is far and wide. 


## Solution
I have utilized an [Optical Character Recognition](https://en.wikipedia.org/wiki/Optical_character_recognition) and [context2vec](https://u.cs.biu.ac.il/~melamuo/publications/context2vec_conll16.pdf) models with a custom weighing algorithm results from each model to decipher messy handwriting to predict most likely text. 

## Dependencies
- Decipher
- jenkins

## Workflow
docker run \
  --rm \
  -u root \
  -p 8080:8080 \
  -v jenkins-data:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v "$HOME":/home \
  jenkinsci/blueocean

[somehow end it? or background this process]
cat /var/jenkins_home/secrets/initialAdminPassword
for initial administrator password


