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

* Basic 32-bit Amazon Linux AMI 2011.02.1 Beta (AMI Id: ami-8c1fece5)
* Basic 64-bit Amazon Linux AMI 2011.02.1 Beta (AMI Id: ami-8e1fece7)

When launching your EC2 instance, merely specify a UserData of
something like...

    #include
    https://raw.github.com/couchbaselabs/cloud-init/master/membase-server-community_x86_64_1.7.0.rpm.install

Or like...

    #include
    https://raw.github.com/couchbaselabs/cloud-init/master/couchbase-single-server-community_x86_64_2.0.0-dev-preview-3.rpm.install

# More info

* https://help.ubuntu.com/community/CloudInit
* http://docs.amazonwebservices.com/FeaturedArticles/latest/index.html?cloudformation-waitcondition-article.html
* http://aws.amazon.com/articles/2944359479955804

Also, to launch more than just single nodes and instead launch
auto-joined, "N-pack" clusters of Membase servers, please consider the
CloudFormation templates at...

* https://github.com/couchbaselabs/cloud-formation

# License

* MIT - Made It Trivial for you to use.

