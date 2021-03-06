#Introduction
Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web. S3 is a class of key value based object store that is hosted by AWS. 
Objects which are organized into buckets and each object is identified by a unique user-assigned key.

#Triggers
Amazon S3 supports webhook, enabling users to monitor the real-time events.

### Connect provides two triggers for AWS S3:
To begin your workflow, you will be given the option to choose one out of two trigger events.

1. **Object Created**

    Triggers when a new object is uploaded in a specified bucket.

2. **Object Deleted**

    Triggers when an object is deleted from the specified bucket.
![](img/AWSS3Trigger.png)
After the selection of Trigger, you need to set a connection for the AWS S3.

#Connection Guide

AWS S3 uses [BasicAuth](https://docs.aws.amazon.com/general/latest/gr/aws-security-credentials.html) to enable users to authorize its content. For the BasicAuth connection, the user needs to provide access key and secret access key to set up the connection.

To find your Access Key and Secret Access Key:

1. Use your AWS account email address and password to sign in to the [AWS Management Console](https://console.aws.amazon.com/) as the AWS account root user.
2. If you see a warning about accessing the security credentials for your AWS account, choose Continue to Security Credentials.
3. Expand the Access keys (access key ID and secret access key) section.
4. Choose Show Access Key to copy the access key ID and secret key from your browser window and paste it somewhere else.
5. During access key creation, AWS gives you one opportunity to view and download the secret access key part of the access key. If you don't download it or if you lose it, you can delete the access key and then create a new one.
6. A complete guide can be found [here](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys).

## Apply Selection Criteria
 When you set up the connection for the AWS S3 you can add a filter over the trigger to narrow down the event data.
![](img/AWSS3_selectioncriteria.png)

 Click here to know more [How Selection Criteria Works?](/docs/concepts/filters/index.md)


#Actions
1. **Upload Object or File**

    Upload file into the specified bucket via file contents.

## Data mapping and transformation
You can manually write data in action input fields or can map your trigger data. Click below link for details - [How to mapping and transformation works?](/docs/concepts/transformations/index.md)

#Use cases
Here are some use-cases of AWS S3 application with connect:

* Whenever a new object is created, a message can be sent via action to Gmail, outlook or slack.

* Whenever an object is deleted permanently the message can be sent via action to Gmail, outlook or slack.