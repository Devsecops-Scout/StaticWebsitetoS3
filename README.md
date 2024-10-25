# StaticWebsitetoS3

## How to Deploy Static Website to AWS S3
1. ## Add a workflow file to repository
   
   - 
2. ## Create an S3 bucket:

- Go to the AWS Management Console.
- Create a new S3 bucket.
- Under "Permissions", ensure that you allow public read access (for web hosting).
- Edit "Object Ownership" to enable ACLs and acknowledge ACLs will be restored.
3. ## Enable static website hosting:

- In the "Properties" tab of your S3 bucket, enable "Static website hosting".
- Set the "index document" to index.html.
4. ## Create IAM User in AWS:
  
  - Create user, attach policies directly and give S3 access.
  - Create user access keys and add to github Secret Actions.
5. ## Add S3 Policy to the created bucket:

  - Under "Permission" edit 'bucket policy' and Policy generator.
  - Select S3 Bucket Policy for type.
  - Add the user's ARN to the Principal.
  - Add the bucket's ARN to the ARN section and click on "Add Statement".
  - Generate policy and add it to the bucket policy.
6. ## Upload your files:

- Upload the index.html file to your S3 bucket.
- If you have additional files like images, CSS, or JavaScript files, upload them as well.
7. ## Access your website:

- You will be provided with an endpoint URL after enabling static website hosting.
- Use this URL to access your website.
  
This index.html file is a starting point and can be further enhanced with JavaScript, CSS frameworks, or backend integration based on your specific needs.
