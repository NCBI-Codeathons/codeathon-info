# GCP resources for NCBI codeathon participants

## GCP Quickstart guide to help beginners
If you provide a Google enabled email account to the codeathon organizers and indicate interest in a cloud account, you will receive an email with login instructions. If you are new to GCP. Here are some resources to help you get started. 

[GCP Quickstart guide to help beginners](https://cloud.google.com/docs/tutorials)
This guide provides a step-by-step introduction to GCP, covering essential concepts and tasks. It's a great starting point for those unfamiliar with cloud computing or GCP specifically.

Key topics covered in the Quickstart guide include creating a GCP account, creating a project, creating a compute instance, connecting to the instance, running a basic command.

## More GCP Tutorials
These tutorials will guide you through using specific GCP services that might be relevant to the codeathon.

[Creating a Compute Engine Instance](https://cloud.google.com/compute/docs/instances/create-start-instance): This tutorial guides you through creating a virtual machine (VM) on Google Cloud Platform (GCP). Ideal for tasks requiring significant processing power or memory, such as running complex applications or data analysis pipelines.

[Using Cloud Storage](https://cloud.google.com/storage/docs/overview): This overview provides information on storing and accessing data in Google Cloud Storage. Suitable for storing files of any size, such as images, videos, documents, and data backups.

[Creating a Bucket](https://cloud.google.com/storage/docs/creating-buckets): A bucket is a container for objects in Cloud Storage. This tutorial explains how to create one. Used to organize data within Cloud Storage, enabling efficient management and access.

[Transferring Data to Cloud Storage](https://cloud.google.com/blog/topics/developers-practitioners/how-transfer-your-data-google-cloud): This blog post outlines several methods for transferring data to Cloud Storage, including Cloud Storage transfer tools, Storage Transfer Service, Transfer Appliance, and BigQuery Data Transfer Service.

[Creating a Cloud SQL Instance](https://cloud.google.com/sql/docs/mysql/create-instance): Cloud SQL is a managed relational database service. This tutorial demonstrates how to create a MySQL instance. Ideal for storing and managing structured data for web applications or other applications.


## Additional Security Considerations

[Adding Keys to Instances](https://cloud.google.com/compute/docs/instances/ssh): Before accessing compute engine instances, it's essential to configure secure access using SSH keys. This document explains the process.

[Setting Up BigQuery Access](https://cloud.google.com/bigquery/docs/control-access-to-resources-iam#create): BigQuery offers granular access control to ensure data security. This documentation covers creating and managing access permissions.


## GCP Security Reminder for NCBI Codeathon Participants
During the NCBI codeathon, it's important to prioritize the security of your Google Cloud Platform (GCP) account. This includes keeping your GCP account credentials, such as your API keys or project IDs, private. Sharing this information publicly could lead to unauthorized access to your GCP resources and potential financial charges.

Here are some common ways GCP account credentials might accidentally be made public:

- **Uploading code to GitHub**: If your code includes GCP project IDs, API keys, or other sensitive information, uploading it to a public GitHub repository could expose your credentials to anyone with internet access.

- **Sharing configuration files**: Configuration files used for GCP projects might contain API keys or other sensitive details. Be mindful of who you share these files with and avoid posting them online.

- **Embedding credentials in logs**: Logs generated during development or testing might contain snippets of code that include GCP credentials. Make sure to remove these sensitive details before sharing logs publicly.
