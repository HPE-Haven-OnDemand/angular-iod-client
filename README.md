**Note:** this README is still a work in progress. To contribute to it, fork this repo and submit a pull request. Sections that have 'TO DO' require updates.

# Angular wrapper for Haven OnDemand

Official Angular wrapper to help with calling [Haven OnDemand APIs](http://havenondemand.com).

Information can be found on the project homepage [here](http://hpe-idol.github.io/angular-iod-client)

[![Build Status](https://travis-ci.org/hpe-idol/angular-iod-client.svg?branch=develop)](https://travis-ci.org/hpe-idol/angular-iod-client)

## What is Haven OnDemand?
Haven OnDemand is a set of over 70 APIs for handling all sorts of unstructured data. Here are just some of our APIs' capabilities:
* Speech to text
* OCR
* Text extraction
* Indexing documents
* Smart search
* Language identification
* Concept extraction
* Sentiment analysis
* Web crawlers
* Machine learning

For a full list of all the APIs and to try them out, check out https://www.havenondemand.com/developer/apis

## Installation
To install, run the following command
```
TO DO
```

To install the latest version from this github repo

```
TO DO
```

## Importing into your app and initializing the client
Place the following where you are including libraries
```angular
TO DO
```
where you replace "API_KEY" with your API key found [here](https://www.havenondemand.com/account/api-keys.html). `version` is an *optional* parameter which can be either `"v1"` or `"v2"`, but defaults to `"v1"` if not specified.

If operating behind a firewall, specify a proxy when initiating the client. Here is an example:
```angular
TO DO
```

## Sending requests to the API - POST and GET
You can send requests to the API with either a POST or GET request, where POST requests are required for uploading files and recommended for larger size queries and GET requests are recommended for smaller size queries.

### POST request
```angular
TO DO
```

### GET request
```angular
TO DO
```

## Synchronous vs Asynchronous
Haven OnDemand's API can be called either synchronously or asynchronously. Users are encouraged to call asynchronously if they are POSTing large files that may require a lot of time to process. If not, calling them synchronously should suffice. For more information on the two, see [here](https://dev.havenondemand.com/docs/AsynchronousAPI.htm).

### Synchronous
To make a synchronous GET request to our Sentiment Analysis API
```angular
TO DO
```

### Asynchronous
To make an asynchronous POST request to our Sentiment Analysis API
```angular
TO DO
```
which will return back the job ID of your call.

#### Getting the results of an asynchronous request - Status API and Result API

##### Status API
The Status API checks to see the status of your job request. If it is finished processing, it will return the result. If not, it will return you the status of the job.

```angular
TO DO
```

To get the status, or job result if the job is complete
```angular
TO DO
```

##### Result API
The Result API checks the result of your job request. If it is finished processing, it will return the result. If it not, the call the wait until the result is returned or until it times out. **It is recommended to use the Status API over the Result API to avoid time outs**

```angular
TO DO
```

To get the result
```angular
TO DO
```

## POSTing files
TO DO

## Examples

### Synchronous Sentiment Analysis GET request
TO DO

### Asynchronous Sentiment Analysis POST request checking response with Result API
TO DO

### Asynchronous Speech Recognition POST request checking response with Status API
*Note: Larger files POSTed to the APIs take some time to process, so if you call the* `get_job_status` *API immediately afterwards, it will respond back with a* `Processing` *result. Allow the API enough time for the completed response.*

TO DO

### Synchronous OCR Document GET request with callback function
TO DO

## License
Licensed under the MIT License.
