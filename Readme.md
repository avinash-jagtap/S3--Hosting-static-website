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
1. In the AWS management console search bar, search -  S3.
2. Click on - S3
3. Click on - crate S3 bucket 
        
        // to begin creating new S3 bucket to upload and host your website

![Homepage-S3](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Home-S3.png)

 ###   Enter bucket name - s3-static-carvilla

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

![Bucket-created](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Bucket%20created-Successfully.png)

#### Successfully created bucket - s3-static-carvilla
# Step 3:- Upload your Website for hosting
_Your S3 bucket is created now you are able to uplod your objects._
1.Open bucket - s3-static-carvilla
2. Click on - Upload
3. Click on - Add folder

        // _select your website folder from your local machine_
4. Cross check your selected folder  
5. Click on "Upload"

![Object-Uploading](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Object%20ready%20to%20upload.png)

#### Your website folder successfully uploaded.
# Step 4:- Start website hosting
_After upload website files and foldres, now you are ready to host website, For the hosting process follow some steps which are mentioned in below-_

1. Select bucket -s3-static-carvilla
2. Click on 'Properties'
3. Scroll down and find out property - Static website hosting
4. Click on -Edit
5. Edit static website hosting from Disable to Enable
6. Select hosting type - Host a static website
7. Enter required path - index.html
8. Click on - save changes

![Enable-SWH](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Ststic%20website%20hosting%20enable.png)

##### Now you need enable public access of website objects.  
# Step 5:- Making Public access Using ACL
_To give the public access to your website you must need to make public access enable, because until you do not Enable public access, you will not able to access your website outside the AWS environment._

For the enable public access you need to follow some steps:-
#### Open bucket

![Bucket-open](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Bucket%20opened.png)

1. Select - Object (your website folder)
2. Click on - Actions
3. Scroll down and click on - make public using ACL
4. Click on - Make public

![Public-access-enable](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Public%20access%20Successfully.png)

#### Now you able to access your website outside the AWS environment.
# Step 6:- Test Static website 
_After your full steup you are able to access your website from outside the AWS environment, for the testing your setup follow some steps which are mentioned below._ 

1. Open bucket - s3-static-carvilla
2. Open folder - carvilla/
3. Select - index.html file 

![Select index.html](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Select%20index.html%20file.png)

4. Copy URL of - index.html
5. Open new tab/browser and paste copied URL
6. Check your output(Website homage)

![Output](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Website%20host%20Successfully.png)

#### Your S3 static website hosting is successful!
# Step 7:- Delete all resources and objects
after completion of the project you can delete your all resources
_Note :- you cannot delete bucket directly, firstly you need to make bucket empty_
### How to empty bucket ?
1. Select bucket 's3-static-carvilla'
2. Click on 'Empty bucket'
3. Empty panel is opened - Enter text _Permanently delete_ 
4. click on 'Empty'
Now you  able to delete bucket
### How to delete bucket ?
1. Select bucket 's3-static-carvilla'
2. Click one 'delete'
3. Enter bucket name 's3-static-carvilla'
4. Click on 'Delete bucket'

![Bucket-deleted](https://github.com/avinash-jagtap/S3--Hosting-static-website/blob/master/Images/Bucket%20Deleted%20Successfully.png)

#### Your S3 bucket is deleted.
# Summary
In this project you deploy infrastructure for how to host a static website on AWS using an S3 bucket. This consists of creating a bucket, uploading website files into it, granting public access through ACL, and configuring static website hosting settings. The site once hosted can be publicly accessible through the S3 URL. The resources can be cleaned after testing by emptying and deleting the bucket.