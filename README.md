# GoogleCloud
Repository for all sorts of useful info like uploading to a bucket then a VM and things like that: 

How to stop a VM instance

	 gcloud compute instances stop bucket_name-vm-1 --discard-local-ssd --zone=us-east4-c

# Copying local files to a GCP bucket

Use this to upload a single file from your local computer to a bucket

	 gsutil cp /path/to/file gs://name-of-bucket/
  
Use this to upload many files from your local computer to a bucket

	 gsutil -m cp *fastq.gz gs://name-of-bucket/

# Bucket to VM
Use this to upload files from a bucket to the VM in your current working directory

	 gsutil cp gs://name-of-bucket/path/*fastq.gz .
