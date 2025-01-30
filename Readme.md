# hosting your static website in S3 bucket
Hello, in this project you are going to create S3 bucket and host static website, This project focuses on hosting a static website using Amazon Web Services (AWS).
## Learning Objective
Upon completion of this project you will be able to create bucket and host any static website and other resources that need for static website host
- S3 bucket
- Public access
- Object ownership
- Bucket versioning
- Object upload
- Object Public access using ACL
- Static website hosting 
- Test hosted website
## Prerequisites
- Conceptual understanding of Simple Storage Service (S3)  
- Manage Public access
- Strong understanding of Static Website hosting
# Step 1:- Logging in to the Amazon Web Services Console
Login to your AWS account using your AWS credentials
# Step 2:- Creating S3 Bucket
Amazon Simple Storage Service (Amazon S3) enables to create your resources into S3 which you defined
1. In the AWS management console search bar, search S3 and click on the S3 service
2. Click on the 'crate S3 bucket' to begin creating new S3 bucket to upload and host your website
 ###   Enter bucket name "s3-static-carvilla"

        // _Note:- bucket name should be unique._

        // _bucket name can be between 3 and 63 characters long._

        // _bucket name can contain only lower-case characters, numbers, periods, and dashes._

        // _bucket name must start with a lowercase letter or number._

 ###   Select Object Owenrship "ACLs Enabled"
_Access Control List are needed for static website hosting in AWS S3 to grant public read access to the content in the bucket._
 ###   Uncheck "Block all public access" for this bucket.
 _We need to uncheck "Block all public access" for static website hosting in AWS S3 to allow public access to the content in the bucket._
###     Enable "Bucket versioning"
_Bucket versioning is not required for static website hosting, but it helps to recover previous versions of website files in case of accidental changes or deletions._
###     Click on "Create bucket"
_Successfully created bucket "s3-static-carvilla"_
# Step 3:- Upload your Website for hosting
Now your bucket is  ready to "Host website" and store any other objects.

1. Click on "Upload"
2. Click on "Add folder" 
        // _select your website folder from your local machine_
3. Crosscheck your selected folder after and scroll down and click on "Upload"

Now your website Objects successfully uploaded 
# Step 4:- Start website hosting
Now your website is uploaded in the bucket "s3-static-carvilla".
next step is Host your website, for the hosting website:-
1. Select the bucket 's3-static-carvilla'
2. Click on 'Properties'
3. Scroll down and find out 'Static website hosting'
4. Click on 'Edit'
5. Edit static website hosting from Disable to 'Enable'
6. Select hosting type - Host a static website
7. Enter required path - 'index.html'
8. Click on 'save changes'

Hosting website successfully 
Now we need enable public access to website 
# Step 5:- Making Public access Using ACL
To enable the public access to your object you must need to make public access enable, because until you do not Enable public access, you will not able to access your website outside the AWS environment.

For the enable public access you need to follow some steps:-
1. Select 'Object'
2. Click on 'Actions'
3. Scroll down and click on 'make public using ACL'
4. 'Successfully edited public access'

Now you able to access your website outside the AWS environment.
# Step 6:- Test your  hosted Static website
after upload objects and configure all resources, permissions and properties 

now you can access your website outside the AWS environment 
1. Open bucket 's3-static-carvilla'
2. Open folder 'carvilla/'
3. Select 'index.html' file 
4. Copy URL 'index.html'
5. Open new tab and paste copied URL
6. Check output after link open 
# Step 7:- Output
# Step 8:- Delete all resources and objects
after completion of the project you can delete your all resources
_Note :- you cannot delete bucket directly, firstly you need to make bucket empty_
### How to empty bucket
1. Select bucket 's3-static-carvilla'
2. Click on 'Empty bucket'
3. Empty panel is opened - Enter text _Permanently delete_ 
4. click on 'Empty'
Now you  able to delete bucket
### How to delete bucket
1. Select bucket 's3-static-carvilla'
2. Click one 'delete'
3. Enter bucket name 's3-static-carvilla'
4. Click on 'Delete bucket'
# Summary
In this project you deploy infrastructure for how to host a static website on AWS using an S3 bucket. This consists of creating a bucket, uploading website files into it, granting public access through ACL, and configuring static website hosting settings. The site once hosted can be publicly accessible through the S3 URL. The resources can be cleaned after testing by emptying and deleting the bucket.