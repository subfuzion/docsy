---
title: "Deployment with Firebase and Cloud Build"
linkTitle: "Deployment with Firebase"
weight: 3
description: >
  Continuous deployment of your Docsy site with Firebase and Cloud Build
---

This tutorial explains how to continuously deploy your site whenever new changes
are committed to the `master` branch.

## Services to use

+ Firebase
+ Cloud Build
+ Artifact Registry

## General steps

+ Generate a CI Token
+ Store the secret in GCP Secret Manager
+ Write your builder docker file
+ Submit your docsy builder to the registry
+ Write your Cloud Build config file.
  This is a 2-step build: Generate static content, deploy to firebase
+ Create a Cloud Build trigger, to monitor Github branch
+ Profit!
