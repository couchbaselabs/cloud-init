Scripts to use Couchbase software via CloudInit (cloud-init).

# Important

Change the passwords!

That is - fork this project, change the passwords, push to your own S3
bucket, etc.  Or at least change them quickly after launching your
servers.

# Usage

You can use these scripts with any CloudInit-compatible VM's, via the
"#include" UserData directive.  The Default Amazon Linux AMI's on EC2,
for example, are CloudInit-compatible...

* Basic 64-bit Amazon Linux AMI 2012.03 (AMI Id: ami-aecd60c7)
* Basic 64-bit Amazon Linux AMI 2011.09 (AMI Id: ami-1b814f72)

When launching your EC2 instance, merely specify a UserData text of...

    #include
    https://raw.github.com/couchbaselabs/cloud-init/master/couchbase-server-enterprise_x86_64_1.8.1.rpm.install

The script creates 500M bucket by default, which might exceed the system memory if you plan to use a small instance.
In this case, change the following parameters to reflect your needs

    COUCHBASE_MAX_RAM_MB_PER_SERVER=500
    COUCHBASE_MAX_RAM_MB_FOR_DEFAULT_BUCKET=500

The script takes awhile to download the relevant packages, so please
be patient before accessing your server at...

    http://HOST:8091

# More info

* https://help.ubuntu.com/community/CloudInit
* http://docs.amazonwebservices.com/FeaturedArticles/latest/index.html?cloudformation-waitcondition-article.html
* http://aws.amazon.com/articles/2944359479955804

Also, to launch more than just single nodes and instead launch
auto-joined, "N-pack" clusters of Couchbase servers, please consider the
CloudFormation templates at...

* https://github.com/couchbaselabs/cloud-formation

# License

* MIT - Made It Trivial for you to use.

