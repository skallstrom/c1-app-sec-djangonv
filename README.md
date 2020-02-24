# app-protect-djangonv-mac

Sample Django application for Cloud One Application Security demos, build and deployable to kubernetes with Jenkins.

## Detailed Description

This is a sample, vulnerable-on-purpose, Django application that can be used to demo Cloud One Application Security.

django-nV was created by the fine folks over at nVisium.

See:  http://github.com/nVisium/django.nV

## Pre-Requisites for Usage

* Docker
* A Cloud One Application Security account
* MOADSD-NG, Jenkins and Kubernetes

### Usage Instructions w/ MOADSD-NG

1. Create the Pipeline within Jenkins

2. Access the demoapp URL provided by MOADSD-NG

### Usage Instructions w/ Docker only

1. Download & run the container:

    ```
    docker run --rm -d -p 8000:8000 --name djangonv-app-protect -e TREND_AP_KEY=<KEY> -e TREND_AP_SECRET=<SECRET> howiehowerton/djangonv-app-protect
    ```

2. Access the app on port 8080

### Exploit

1. Follow the instructions in [exploits.md](exploits.md) to exploit the application.  Demonstrate that the exploits work against the vulnerable app.

2. Switch Cloud One Application Security rules from "Report" to "Mitigate".

3. Follow the instructions in [exploits.md](exploits.md) again. Demonstrate that the exploits **no longer** work.
