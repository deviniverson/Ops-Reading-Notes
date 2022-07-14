Devin Iverson
03/21/22

# Importance of Virtualization in the Amazon EC2 Cloud

Virtualization is the creation of a virtual, rather than actual, version of something.

Amazon IaaS cloud service model is characterized by delivering virtualized computer infrastructure in the form of a service. A good example of the virtualization of Amazon AWS services is Amazon Elastic Compute Cloud (EC2). It is essentially an IaaS service that provides virtual servers based on the Xen hypervisor.

The diagram shows the architecture of EC2 host virtualization. The diagram shows the crucial role that hypervisor in virtualization itself. It acts a virtual machine manager that sits on top of the host system where all the customer virtual machines run. “The relationship of the hypervisor to the host operating system and the virtual machine is one of the key distinguishing characteristics of the different virtualization systems.”

image 1

Another critical part of the entire process of virtualization in Amazon EC2 is Amazon Machine Image (AMI), which is also a virtual appliance. However, AMI is mainly responsible for creating on-demand virtual machines within the Amazon Elastic Compute Cloud. The next diagram is an illustration of the importance of Amazon AMI in the process of VM creation in Amazon EC2 and shows how it generates the various EC2 instances on demand.

image 2

The next diagram demonstrates the high-level architecture of Amazon EC2 and relation of EC2 instances to availability zones in various regions. EC2 instances use the storage through either Ephemeral (temporary) or Elastic Block Storage snapshots stored in Amazon S3; and observe how CloudWatch monitors AWS cloud resources and how EC2 web traffic is load balanced as well as how it passes through various security rules.

image 3

“In summary, cloud computing leverages virtualization technology to achieve the goal of providing computing resources as a utility.” (Zhang, Cheng, and Boutaba, 2010)