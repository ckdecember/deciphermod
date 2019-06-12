# Decipher Mod

## Overview

Original Decipher project https://github.com/mevanoff24/HandwritingDetection
Modified to code to allow for easy switching between multiple models to predict images into text.

## ... but why?

To create a framework to help people extend the design even further.  To act as a guideline for future projects for more extensible ML code.

## General Solution
Using CI/CD we can speed up the deployment of different models.  With some code modifications, environment variables, a CI/CD system, and a method to record data we can build this extensible framework.

## Dependencies
- Decipher
- jenkins
- and much much more!

## Workflow (SPOILERS for this awesome drama on HBO)
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
