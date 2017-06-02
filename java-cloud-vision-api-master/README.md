# java-cloud-vision-api

## General

Google [Cloud Vision API](https://cloud.google.com/vision/) enables developers to understand the content of an image by encapsulating powerful machine learning models in an easy to use REST API. It quickly classifies images into thousands of categories (e.g., "sailboat", "lion", "Eiffel Tower"), detects individual objects and faces within images, and finds and reads printed words contained within images. You can build metadata on your image catalog, moderate offensive content, or enable new marketing scenarios through image sentiment analysis. Analyze images uploaded in the request or integrate with your image storage on Google Cloud Storage. 

## Pre-requisit

### Create Google Account

If you don't already have a Google Account (Gmail or Google Apps), you must create one. Sign-in to Google Cloud Platform console ([console.cloud.google.com](console.cloud.google.com)) and create a new project.

Remember the project ID, a unique name across all Google Cloud projects (the name above has already been taken and will not work for you, sorry!). It will be referred to later in this codelab as PROJECT_ID.

Next, you'll need to enable billing in the Developers Console in order to use Google Cloud resources like Cloud Datastore and Cloud Storage.

New users of Google Cloud Platform are eligible for a $300 free trial.

### Create Credentials

The application needs to be authenticated. The simplest authentication mechanism involves passing an API key directly to the service. In using the Vision API, we recommend that you enable an API key for testing purposes, and a service account for production usage.

    Visit Google Developers Console.
    Navigate to the project you created.
    From the left navigation, click API Manager > Credentials.
    Click Create credentials > API key.
    Choose Browser key, enter a name for this key and click Create.
    Copy the key from the dialog box and keep it secure.

### Enable Cloud Vision API

The credentials you created allow your application to authenticate with Google Cloud Vision API. Enable the Cloud Vision API:

    From the left navigation, click API Manager > Overview, search for the "Cloud Vision API".
    Click on Cloud Vision API.
    Click Enable API.

### Execute Java Class
In order to interact with and test Google Cloud Vision APi, you just need to run GoogleTest Java class.

`java -cp . GoogleTest`

### Command Line (CLI)
The [gcloud beta ml](https://cloud.google.com/sdk/gcloud/reference/beta/ml/) vision command group is now available. These command allow you to analyze images with Google Cloud Vision:
```
gcloud beta ml vision detect-documents
gcloud beta ml vision detect-faces
gcloud beta ml vision detect-image-properties
gcloud beta ml vision detect-labels
gcloud beta ml vision detect-landmarks
gcloud beta ml vision detect-logos
gcloud beta ml vision detect-safe-search
gcloud beta ml vision detect-text
gcloud beta ml vision detect-web
```
