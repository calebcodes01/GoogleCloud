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
#if using docker and get this error: 
docker: Error response from daemon: driver failed programming external connectivity on endpoint interesting_buck (7bf9cfbad45928b6622b4403e8c68b697dcd304441ae34166776175ac086ddad): Bind for 0.0.0.0:8080 failed: port is already allocated.

#list current docker containers
docker container ls
#rm container
docker rm -f a10bce797b60
