---
title: "Using S3"
weight: 7
chapter: false
pre: " <b> 5.7. </b> "
---

#### Amazon S3 (Simple Storage Service)

**Amazon S3** is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere.

#### What You'll Learn

In this section, you will learn how to:

- Create an S3 bucket
- Upload and manage objects
- Configure bucket permissions
- Enable versioning and lifecycle policies
- Set up static website hosting
- Implement security best practices

#### Key Concepts

**S3 Bucket**: A container for storing objects in Amazon S3. Each bucket has a globally unique name.

**Objects**: Files stored in S3, consisting of data and metadata. Each object is identified by a unique key within a bucket.

**Storage Classes**: Different options for storing data based on access patterns:

- S3 Standard: Frequent access
- S3 Intelligent-Tiering: Automatic cost optimization
- S3 Standard-IA: Infrequent access
- S3 Glacier: Long-term archive

#### Creating an S3 Bucket

1. **Navigate to S3 Console**

   - Open the AWS Management Console
   - Search for "S3" and click on the S3 service
     ![Creating an S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B1.png)

2. **Create a New Bucket**

   - Click **Create bucket**
     ![Creating an S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B2.png)
   - Enter a unique bucket name (must be globally unique)
   - Select your AWS Region
   - Configure additional settings:
     - Object Ownership
     - Block Public Access settings (keep enabled by default)
     - Bucket Versioning
     - Encryption
       ![Creating an S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B3.png)

3. **Click Create Bucket**
   ![Creating an S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B4.png)

#### Uploading Objects to S3

1. **Select Your Bucket**

   - Click on your bucket name from the list
     ![Uploading Objects to S3](/5-Workshop/5.6-S3-img/S3-P2B1.png)

2. **Upload Files**

   - Click **Upload**
     ![Uploading Objects to S3](/5-Workshop/5.6-S3-img/S3-P2B2.png)
   - Click **Add files** or drag and drop files
   - Configure permissions and properties
   - Click **Upload**
     ![Uploading Objects to S3](/5-Workshop/5.6-S3-img/S3-P2B3.png)

3. **View Object Details**
   - Click on the object name to view properties
   - Copy the object URL for access
     ![Uploading Objects to S3](/5-Workshop/5.6-S3-img/S3-P2B4.png)

#### Configuring Bucket Permissions

##### Using Bucket Policies

Bucket policies are JSON-based access policy language to manage permissions.

Example policy to allow public read access:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```

##### Using Access Control Lists (ACLs)

- Set permissions at bucket or object level
- Grant access to specific AWS accounts

#### Enabling Versioning

Versioning keeps multiple variants of an object in the same bucket.

1. Go to your bucket **Properties**
2. Find **Bucket Versioning**
3. Click **Edit**
4. Select **Enable**
5. Click **Save changes**
   ![Enabling Versioning](/5-Workshop/5.6-S3-img/S3-P4B1.png)
   ![Enabling Versioning](/5-Workshop/5.6-S3-img/S3-P4B1.1.png)

Benefits:

- Recover from accidental deletions
- Retrieve previous versions
- Maintain backup history

#### Setting Up Lifecycle Policies

Automate transitioning objects between storage classes or deleting them.

1. Go to **Management** tab
2. Click **Create lifecycle rule**
3. Configure:
   - Rule name
   - Rule scope (entire bucket or filter by prefix/tags)
   - Lifecycle rule actions:
     - Transition to different storage classes
     - Expire objects after specified days
     - Delete incomplete multipart uploads

#### Static Website Hosting

Host a static website using S3:

1. Go to **Properties** tab
2. Find **Static website hosting**
3. Click **Edit**
4. Select **Enable**
5. Configure:
   - Index document (e.g., index.html)
   - Error document (e.g., error.html)
6. Click **Save changes**

Your website endpoint will be: `http://bucket-name.s3-website-region.amazonaws.com`

#### Next Steps

After completing this section, you should be able to:

- Create and configure S3 buckets
- Upload and manage objects efficiently
- Implement security best practices
- Optimize costs using lifecycle policies
- Use S3 for various real-world applications
