This script will take ebs backup of Windows instance

Before you can even successfully run this script, you need to install the Amazon EC2 Command Line Tools
http://nitheeshp.blogspot.in/2014/01/configuring-and-installing-new-aws.html
Make sure that %JAVA_HOME%\bin and %EC2_HOME%\bin get added to your PATH system variable.

Once you are able to successfully run ec2-describe-snapshots from a cmd prompt, you should be set to schedule this script.

Configure the script

Change the AWS_HOME variable to a directory that can hold temporary text files that the script needs to create.
Change the AWS_VOLUME variable to the volume-id of the volume that you want to snapshot.
Change the AWS_SNAPSHOT_KEEP variable to the number of snapshots you want to keep

Schedule the script

You can use windows task scheduler 

Once scheduled, the batch script will take care of creating snapshots and rotating out old ones
