# Roger.io 👀

> If you are a failing pod, Roger.io is watching you!


Rogerio is a small and lightweight system for checking faults on kubernetes services based on health checks

## How it works

Roger.io will keep watching the kuberbetes services you define in configuration file, it will keep calling a predefined health check endpoint, or running some kind of request, looking for a well defined result.

There is a set of cases where Roger.io will unsderstand an application as failed:

* The service didn't answer in a given timetout
* The response is different from the expected
* The status code is different from the expected

When a fault is detected, Roger.io will send a request to an API that you can define in configuration file. This is designed to interate with [Pombo Correio notification system](https://github.com/neurono-ml/pombo-correio).


