# .NET Core 3.1 on Google Cloud Run

[![Run on Google Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run)

.NET Core 3.1 was [released](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-1/) on December 3rd, 2019 and is a LTS release, supported for three years.

## Deploy to Cloud Run

[Cloud Run](https://cloud.run) allows you to run your .NET Core 3.1 app in a fully managed serverless environment.

To deploy to Cloud Run, use the button above, or the following steps:

* Build with `gcloud builds submit --tag gcr.io/[your-project]/dotnetcore31`
* Deploy with `gcloud run deploy --image gcr.io/[your-project]/dotnetcore31`

Replacing `[your-project]` with your Google Cloud project ID.

## Running locally

* Build with `docker build -t dotnetcore31 .`
* Start with `docker run -p 8080:8080 dotnetcore31`
* Open in your browser at `http://localhost:8080`