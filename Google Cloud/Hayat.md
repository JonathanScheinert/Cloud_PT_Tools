
## Hayat is an auditing & hardening script for Google Cloud Platform services 

Hayat - https://github.com/DenizParlak/hayat

**Prerequisites** 
* Hayat has been written in bash script using gcloud and it's compatible with Linux and OSX.

**Key features**
* Identity & Access Management
  * Ensure that corporate login credentials are used instead of Gmail accounts.
  * Ensure that there are only GCP-managed service account keys for each service account.
  * Ensure that ServiceAccount has no Admin privileges.
  * Ensure that IAM users are not assigned Service Account User role at project level.
* Logging and Monitoring 
  * Ensure that sinks are configured for all Log entries.
  * Ensure that object versioning is enabled on log-buckets.
* Virtual Machines
  * Ensure that instances are not configured to use the default service account with full access to all Cloud APIs.
  * Ensure "Block Project-wide SSH keys" enabled for VM instances.
  * Ensure oslogin is enabled for a Project.
  * Ensure 'Enable connecting to serial ports' is not enabled for VM Instance.
* Storage
  * Ensure that Cloud Storage bucket is not anonymously or publicly accessible.
  * Ensure that logging is enabled for Cloud storage bucket.

![Import Module]('https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Google Cloud/Screenshots/Hayat_1.png')
