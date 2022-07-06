# k8s-s3-archive
Relay a POST request's attached file to an S3 bucket via a k8s deployment. 

## Usage 
2. Populate the environment variables in `k8s-s3-archive.yml`
3. Run: `kubectl apply -f k8s-s3-archive.yml`
4. Upload files with the following:
>```
>curl --verbose --header "Content-Type:multipart/form-data" --form "artifact=@/path/to/artifact.zip"  <http://deployment.ip/archive>
>```
