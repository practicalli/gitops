# Introdution

This is a placeholder for the GitOps Overview page


TODO:rewrite blurb from GitLab to something Practicalli

https://about.gitlab.com/topics/gitops/

GitOps is an operational framework that takes DevOps best practices used for application development such as version control, collaboration, compliance, and CI/CD tooling, and applies them to infrastructure automation. While the software development lifecycle has been automated, infrastructure has remained a largely manual process that requires specialized teams. With the demands made on today’s infrastructure, it has become increasingly crucial to implement infrastructure automation. Modern infrastructure needs to be elastic so that it can effectively manage cloud resources that are needed for continuous deployments.

Modern applications are developed with speed and scale in mind. Organizations with a mature DevOps culture can deploy code to production hundreds of times per day. DevOps teams can accomplish this through development best practices such as version control, code review, and CI/CD pipelines that automate testing and deployments.

GitOps is used to automate the process of provisioning infrastructure. Similar to how teams use application source code, operations teams that adopt GitOps use configuration files stored as code (infrastructure as code). GitOps configuration files generate the same infrastructure environment every time it’s deployed, just as application source code generates the same application binaries every time it’s built.

## How do teams put GitOps into practice?

GitOps is not a single product, plugin, or platform. GitOps workflows help teams manage IT infrastructure through processes they already use in application development.

GitOps requires three core components:

    GitOps = IaC + MRs + CI/CD

IaC: GitOps uses a Git repository as the single source of truth for infrastructure definitions. Git is an open source version control system that tracks code management changes, and a Git repository is a .git folder in a project that tracks all changes made to files in a project over time. Infrastructure as code (IaC) is the practice of keeping all infrastructure configuration stored as code. The actual desired state may or may not be not stored as code (e.g., number of replicas or pods).

MRs: GitOps uses merge requests (MRs) as the change mechanism for all infrastructure updates. The MR is where teams can collaborate via reviews and comments and where formal approvals take place. A merge commits to your main (or trunk) branch and serves as an audit log.

CI/CD: GitOps automates infrastructure updates using a Git workflow with continuous integration (CI) and continuous delivery (CI/CD). When new code is merged, the CI/CD pipeline enacts the change in the environment. Any configuration drift, such as manual changes or errors, is overwritten by GitOps automation so the environment converges on the desired state defined in Git. GitLab uses CI/CD pipelines to manage and implement GitOps automation, but other forms of automation, such as definitions operators, can be used as well.

{% youtube %}
https://youtu.be/JtZfnrwOOAw
{% endyoutube %}

## GitOps challenges

With any collaborative effort, change can be tricky and GitOps is no exception. GitOps is a process change that will require discipline from all participants and a commitment to doing things in a new way. It is vital for teams to write everything down.

GitOps allows for greater collaboration, but that is not necessarily something that comes naturally for some individuals or organizations. A GitOps approval process means that developers make changes to the code, create a merge request, an approver merges these changes, and the change is deployed. This sequence introduces a “change by committee” element to infrastructure, which can seem tedious and time-consuming to engineers used to making quick, manual changes.

It is important for everyone on the team to record what’s going on in merge requests and issues. The temptation to edit something directly in production or change something manually is going to be difficult to suppress, but the less “cowboy engineering” there is, the better GitOps will work.


## What makes GitOps work?

As with any emerging technology term, GitOps isn’t strictly defined the same way by everyone across the industry. GitOps principles can be applied to all types of infrastructure automation including VMs and containers, and can be very effective for teams looking to manage Kubernetes-based infrastructure.

While many tools and methodologies promise faster deployment and seamless management between code and infrastructure, GitOps differs by focusing on a developer-centric experience. Infrastructure management through GitOps happens in the same version control system as the application development, enabling teams to collaborate more in a central location while benefiting from Git’s built-in features.
