CloudInit scripts for Couchbase software.

= Important

Change the passwords!  Fork this project && do the needful.

= Usage

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

= More info

* https://help.ubuntu.com/community/CloudInit
* http://docs.amazonwebservices.com/FeaturedArticles/latest/index.html?cloudformation-waitcondition-article.html
* http://aws.amazon.com/articles/2944359479955804

= License

* MIT - Made It Trivial for you to use.

