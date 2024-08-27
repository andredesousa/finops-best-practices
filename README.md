# FinOps Best Practices

FinOps is an operational framework and cultural practice that enhances the business value derived from cloud technology.
These tips are based on Nest documentation, books, articles and professional experience.

## Table of Contents

1. [Implement cost visibility and transparency]()
2. [Map spending data to the business]()
3. [Create showbacks and chargebacks]()
4. [Ensure reports are timely]()
5. [Do budgeting and forecasting]()
6. [Set tag strategy and compliance]()
7. [Identify untagged/untaggable resources]()
8. [Do Resource utilization monitoring]()
9. [Allocate shared costs equitably]()
10. [Dynamically calculate custom rates and amortizations]()
11. [Analyze trending and variance]()
12. [Create scorecards]()
13. [Benchmark against industry peers]()
14. [Focus on business value]()
15. [Understand support costs]()
16. [Identify anomalies]()
17. [Identify redundant resources]()
18. [Find and report on underutilized services]()
19. [Evaluate centralized RI or CUD]()
20. [Use SP and RI]()
21. [Leverage Spot Instances]()
22. [Use services from multiple clouds]()
23. [Regularly review cloud pricing tables]()
24. [Compare prices and workload placement]()
25. [Do vendor management]()
26. [Establish metrics and KPIs]()
27. [Embrace automation]()
28. [Build a culture of cost awareness]()
29. [Do cloud policy and governance]()
30. [Have clear ownership]()
31. [Establish clear roles and responsibilities]()
32. [Deliver spend data to stakeholders]()
33. [Make cultural changes to align with goals]()
34. [Choose appropriate storage options]()
35. [Right-size your resources to your workloads]()
36. [Rightsize instances and services]()
37. [Automate resource optimization]()
38. [Automate shutdowns of unused environments]()
39. [Do auto-scaling]()
40. [Eliminate shadow cloud]()
41. [Integrate recommendations into workflows]()
42. [Delete old backups and review retention timelines]()
43. [Limit data transfer fees]()
44. [Limit spending on software licenses]()
45. [Proactive cost alerting]()
46. [Implement a cloud native design]()
47. [Optimize cloud costs at every development]()
48. [Use of well-architected frameworks]()
49. [Do risk management]()
50. [Do continuous improvement]()

## Implement cost visibility and transparency

By embracing FinOps principles, you’re equipped with the capability to illuminate the intricacies of your organization’s cloud spending, tracking costs with accuracy and granularity.
This knowledge empowers you to make informed decisions, align technology initiatives with budgetary constraints, and foster a culture of financial responsibility across your technical teams.

## Map spending data to the business

Before you can implement accurate chargeback, you must properly map spend data to the organizational hierarchy by cost centers, applications, and business units.
Tags and accounts set up by engineering teams are often not aligned to the view of the world that finance teams need, nor do they include the proper rollups that executives require.

## Create showbacks and chargebacks

As organizations adopt the FinOps model of pushing spend accountability to the edges of the organization, they are finding that chargeback and showback models are becoming increasingly important to driving ownership of spending and recovering costs.

## Ensure reports are timely

Monitoring, and enhancing real-time FinOps reports, team members should provide consistent visibility into their cloud expenditure to all organization levels.
This includes processing and sharing FinOps data as soon as possible for prompt decisions and forecasting.
Also, reports should be designed to convert raw data into comprehensible insights.

## Do budgeting and forecasting

Accurate forecasting minimizes potential cost deviations and bolsters strategic planning.
You can control costs by ensuring all parties know the goals and budgets of each project.
With a comprehensive understanding of cloud costs and usage patterns, organizations can make more accurate predictions about future costs.
This can help organizations plan and budget more effectively and avoid unpleasant surprises down the line.

## Set tag strategy and compliance

Use tagging strategies to allocate costs accurately across different projects, departments, or business units, facilitating detailed financial tracking and accountability.
By strategically implementing a robust tagging and labeling system, you’re effectively annotating your cloud infrastructure, allowing you to trace costs back to specific projects, departments, or teams.

## Identify untagged/untaggable resources

Some organizations have untagged resources and others think they have tagged resources.
Assigning untagged resources to teams or workloads and applying a meta layer of allocation to untaggable ones is critical to proper chargeback, visibility, and later optimization.

## Do Resource utilization monitoring

Observability tools can provide insights into resource utilization metrics, such as CPU usage, memory usage, and network throughput.
By analysing these metrics in conjunction with cost data, organizations can identify underutilized resources that can be downsized or terminated to reduce costs.
[Grafana](https://grafana.com/) is a good choice in many scenarios because of its long list of supported data sources.

## Allocate shared costs equitably

Shared costs like support and shared services should be allocated at the appropriate ratio to responsible teams.
There are a few methods of doing this, including sharing them equally or assigning them based on a usage metric like spend or compute hours.
Leaving them in a central bucket is generally less desirable, as teams then don’t see the true cost of their applications.

## Dynamically calculate custom rates and amortizations

Accurate spend visibility requires companies to take in account in any custom negotiated rates, that discounts from RIs/CUDs (Reserved Instances/Committed Use Discounts) are applied, and that amortized prepayments from RIs/CUDs are applied.
This ensures teams are tracking to the right spend numbers and aren’t surprised if their finance team’s bill doesn’t match their daily spend reporting.

## Analyze trending and variance

Identifying spend drivers often requires ad hoc comparisons of time periods and the ability to report at a high level (e.g., cost center) all the way down to resources (or containers, functions, etc.) to understand cost drivers.
You can create custom dashboards to help you make these comparisons easily.
Tools like [Grafana](https://grafana.com/) or [Power BI](https://www.microsoft.com/power-platform/products/power-bi) can help you with this task.

## Create scorecards

A scorecard is a collection of performance metrics that are designed to reflect the strategic goals of your business unit or organization.
Scorecards let the FinOps team benchmark how different project teams are doing in terms of optimizing cost, speed, and quality.
They’re a quick way of looking for areas that can be improved, which should be done using the fully loaded and properly allocated cost.

## Benchmark against industry peers

Benchmarking is the practice of comparing business processes and performance metrics to industry bests and best practices from other companies.
Building on the concept of internal scorecards, more advanced FinOps teams extend their benchmarking to make comparisons with other industry peer-level spend data to identify their relative efficiency using a normalized set of spend characteristics.

## Focus on business value

FinOps is not just about managing cloud costs, but also about making the most of cloud to increase business value.
Understanding and deriving value from cloud costs is paramount.
This not only involves evaluating spending but analysing the tangible and intangible returns from those investments.
You can develop metrics to measure the business value derived from cloud investments, including impact on revenue growth, customer satisfaction, and operational efficiency.

## Understand support costs

Premium support plans with dedicated contacts and troubleshooting steps add reassurance, but they can also be significant contributors to your monthly bill.
If you rarely call upon support, you could consider switching to an alternative plan, requesting a long-term arrangement to reduce your costs, or dropping premium support altogether.
A competitive SLA is more important than direct support access.

## Identify anomalies

Anomaly detection isn’t just about identifying expense thresholds.
It’s also important to identify unusual spikes in usage.
Given the dramatic rise in the variety of variably charged services available from cloud providers, anomaly detection that watches for any deviations in spend helps you find the needle in the haystack that may need quick remediation.

## Identify redundant resources

One of the most common ways that cloud costs balloon is when you’re paying for redundant resources.
Old resources that are left over from past workloads or administration activities don’t deliver value to your organization but will still contribute to your bill.
You should regularly audit the resources in your cloud accounts so you can spot and remove unnecessary items.

## Find and report on underutilized services

Once teams can see their properly allocated spend and usage, they can start to identify unused resources across all major drivers of spend (e.g., compute, data‐ base, storage, or networking).
You can measure potential savings based on generated recommendations that engineering teams will use during the operate phase, following a predefined process to rightsize resources.

## Evaluate centralized RI or CUD

As a cost-reduction measure, the FinOps team can evaluate metrics on existing AWS/Azure RIs or GCP CUDs to make sure the ones they have are effective and then look for opportunities to buy more.
They track commitments and reservations, analysing the entire portfolio across the enterprise to account for and understand the efficiency of usage and cost-avoidance actuals, complete with visibility into upcoming expirations.

## Use SP and RI

There are many procurement options for cloud compute, including On-Demand, Scheduled, Reserved Instances, Savings Plans, and Spot Instances.
Savings Plans (SP) and Reserved Instances (RI) are ideal for long-running and steady state workloads.
SPs and RIs are prepaid compute instances that offer significant pricing discounts. When purchasing these models from a cloud provider, you select an instance type and typically a region or availability zone and commit to using the instance for a period of 1 or 3 years.

## Leverage Spot Instances

Spot Instances (SI) allow you to bid for unused cloud provider capacity at a significant discount, compared to on-demand instances.
While these instances can be interrupted or reclaimed by the provider, they can be an effective cost-saving measure for workloads that are non-critical and flexible.
With proper management, spot instances can be a cost-effective part of your cloud cost optimization strategy.

## Use services from multiple clouds

Using one provider for all your services can increase your costs, in addition to creating a potential redundancy issue.
Don’t blind yourself to what’s available from alternative providers.
If you want to start using a new type of cloud resource, such as a managed database or storage solution, then it could make operational and financial sense to go multi-cloud and select a service from another cloud provider.

## Regularly review cloud pricing tables

Cloud providers regularly change their pricing, so it’s worth reviewing their offerings periodically to check if you could switch and save.
You might be able to reduce your bill by choosing a slightly different service from the same provider or by migrating to a similar solution in a rival cloud.
To simplify cost comparisons, you can use IaC-linked tools like [Infracost](https://www.infracost.io/) to evaluate what you’d pay for your infrastructure across different cloud platforms.

## Compare prices and workload placement

Workload placement is another cost reduction measure.
Once the FinOps team understands engineering’s infrastructure requirements, they can look at multiple cloud vendors and compare pricing options.
Observability tools can provide insights into resource utilization metrics, such as CPU usage, memory usage, and network throughput.

## Do vendor management

By embracing vendor management within the FinOps framework, you’re orchestrating a thorough evaluation of cloud providers’ offerings, pricing models, and service levels.
This involves assessing the cost-effectiveness of different service tiers, negotiating contracts that align with your usage patterns, and staying attuned to potential cost-saving opportunities like Reserved Instances or Savings Plans.

## Establish metrics and KPIs

Define clear metrics and key performance indicators (KPIs) for monitoring and evaluating the effectiveness of FinOps practices.
Common metrics might include cost savings achieved, percentage of budget used, and cost per service unit.
FinOps framework offers a list of [FinOps KPIs](https://www.finops.org/wg/finops-kpis/) that can be used by all organizations, regardless of cloud service provider, industry, size, or FinOps maturity.

## Embrace automation

Use automated tools to help manage cloud resources more efficiently, such as automatically shutting down unused instances and scaling services based on-demand.
Also, implement automated governance mechanisms to enforce policies around provisioning and usage, ensuring compliance with [FinOps principles](https://www.finops.org/framework/principles/) without manual overhead.

## Build a culture of cost awareness

No cloud optimization project is effective if you do not have all parties on board.
FinOps promotes transparency in financial management. By making financial data and insights accessible to all relevant stakeholders, it ensures that everyone has the information they need to make informed decisions.
These reports can help expose hidden waste and dangerous spend patterns.

## Do cloud policy and governance

A Cloud Policy is a clear statement of intent, describing the execution of specific cloud-related activities in accordance with a standard model designed to deliver some improvement of business value.
Cloud Governance encompasses a spectrum of responsibilities, from defining who has access to cloud resources to establishing guidelines for resource provisioning, security protocols, and cost management practices.

## Have clear ownership

Every individual wielding the power to influence costs should be acutely aware of their footprint.
This goes beyond just knowing the costs. It’s about recognizing how individual decisions, like infrastructural choices, affect the financial health of the organization.
Tags and labels make identifying resources and their owners throughout their lifecycle easier.

## Establish clear roles and responsibilities

Implementing FinOps requires many stakeholders, or [Personas](https://www.finops.org/framework/personas/), in an organization to work collaboratively with the FinOps team.
It is not only the FinOps team who perform FinOps activities.
All FinOps Personas involved in using, tracking, managing, or directing the use of cloud will benefit from working together using the FinOps Framework as an operating model.
Ensure that each role has clear responsibilities related to financial management of the cloud.

## Deliver spend data to stakeholders

Creating the Prius Effect requires stakeholders to regularly see how they’re tracking against their budgets.
Daily or weekly visibility gives them a feedback loop that enables them to make the right decisions for the business.
During the operate phase you focus on how these reports are delivered to stakeholders, building out the processes and automation to generate the reports and make them available.

## Make cultural changes to align with goals

Teams are educated and empowered to understand, account for, and partner with other organizational teams to drive innovation.
Finance teams are empowered to be bold change agents who move out of blocking investment and into partnering with the business/tech teams to encourage innovation.
Each team must constantly and iteratively improve their understanding of cloud and level up their reporting efficiency.

## Choose appropriate storage options

Storage for cloud-native apps comes in different solutions.
Object storage, network storage mounts, and block volume disks that mount directly to compute instances are all viable options that you can choose between.
Apps often support multiple storage types, so you have flexibility in selecting the right one for your environment.
Evaluating different types of storage can lead to significant cost savings.
It’s also important to use an appropriate storage class for each of your data types.

## Right-size your resources to your workloads

Underutilized resources are another prevalent cause of excess cloud costs.
Provisioning large compute resources won’t provide an advantage for apps that can’t utilize the available CPU and memory capacity, but you’ll still be paying more for the privilege.
Storage volumes that are sized much larger than your data result in the same problem.
Right-sizing is the process by which resource capacity is matched to resource utilization.
You can use cloud mechanisms such as auto-scaling to dynamically right-size on-demand, based on actual resource utilization.

## Rightsize instances and services

During the optimize phase, you might discover that you’re paying for more powerful compute resources than you need.
Recommendations that have been generated are acted upon during the operate phase.
Engineers review the recommendations and, where appropriate, make adjustments, for example, switching to less powerful, less expensive instances; replacing unused storage with smaller sizes; or using hard drive rather than SSD-based storage for some projects.
Mature FinOps teams do this across all major drivers of spend.

## Automate resource optimization

Non-optimized resources don’t deliver value to your organization but will still contribute to your bill.
Mature teams move toward programmatic detection of changes needed for incorrectly sized resources and offer the ability to automatically clean up underutilized ones.

## Automate shutdowns of unused environments

Self-service test, staging, and QA environments can tighten the software development lifecycle (SDLC) by letting developers preview changes in production-like environments.
However, these ostensibly transient environments can be forgotten after the work is completed, causing unexpected costs to accrue.
These situations can usually be resolved by integrating tooling into your development pipeline that automatically shuts down development environments after the relevant code has been merged into your project’s main branch.

## Do auto-scaling

Auto-scaling is a cloud computing technique for dynamically allocating computational resources.
Auto-scaling empowers your applications to automatically adjust resources in response to fluctuations in demand, ensuring you only use what’s needed at any given moment, thereby avoiding unnecessary expenses during periods of low activity.

## Eliminate shadow cloud

Shadow IT describes the unauthorized use of apps, devices, and compute infrastructure that occurs without an administrator’s knowledge.
Shadow IT can evolve into shadow cloud when team members are given access to cloud computing environments.
Preventing a shadow cloud can stop charges for mysterious unknown activities from appearing on your bill.
To do this, you should systemize your process and ensure that all developer interactions with cloud resources are managed through a consistent platform.

## Integrate recommendations into workflows

Applying recommendations to projects can be a time-consuming operation, no matter how simple it is.
Bureaucracy can be an obstacle to improving processes.
Mature teams stop requiring application owners to log in to see recommendations and begin pushing items like rightsizing recommendations into sprint planning tools such as [JIRA](https://www.atlassian.com/software/jira).

## Delete old backups and review retention timelines

Unnecessary data retention can cause gradual increases in cloud costs, especially when an inappropriate storage type is being used.
You can prevent this by periodically auditing your data catalog and deleting anything that doesn’t need to be kept.
Old backups, log files, and crash dumps are some of the data types to look at.
You can prevent excess storage consumption by configuring appropriate data retention timelines, and then using automated processes to prune your storage as records become outdated.

## Limit data transfer fees

Migrating data to and from a public cloud can be expensive.
Cloud vendors often charge data egress fees to shift data from their platforms and sometimes between regions. 
ou can reduce cloud costs by avoiding unnecessary data transfers.
Assess your cloud vendor’s transfer fees and adjust the cloud architecture to minimize the necessary data transfers.

## Limit spending on software licenses

Cloud cost budgets should also account for any proprietary software subscriptions or licenses that your deployments depend on.
These could be deployed manually or via the service marketplaces that are integrated into cloud provider control panels.
Pruning the number of licensed software subscriptions, you use could be a viable way to reduce your total bill, especially where good free or open-source (FOSS) alternatives are available.

## Proactive cost alerting

Proactive cost alerting is the practice of implementing automated systems or processes to monitor financial data, identify potential issues or anomalies, ensure compliance, and alert relevant stakeholders before problems escalate.
You can set alerts to notify you when you approach or exceed expected spending thresholds.
[Prometheus](https://prometheus.io/) is a good option for implementing proactive alerts.

## Implement a cloud native design

[Cloud Native](https://www.cncf.io/) is the software approach of building, deploying, and managing modern applications in cloud computing environments.
Replace existing cloud systems with more cost-efficient ones to leverage cloud-specific capabilities.
For example, you can design a system with auto-scaling to ensure you only pay for the servers you use.

## Optimize cloud costs at every development

Cloud cost optimization shouldn’t be an afterthought.
Instead, it should be a continuous effort integrated throughout your software development lifecycle, embedding cost-efficiency into your company’s DNA.
You can do several things, such as developing with cost-efficiency in mind, aiming to create lightweight and scalable applications.

## Use of well-architected frameworks

By embracing well-architected frameworks, you’re essentially adopting proven design principles that encompass operational excellence, cost optimization, security, reliability, and performance efficiency.
This approach not only ensures that your cloud resources are provisioned optimally but also safeguards against unnecessary expenses that might arise from overprovisioning or suboptimal configurations.

## Do risk management

By embracing risk management within the FinOps framework, you’re essentially conducting a thorough analysis of factors that could impact your cloud expenditure adversely, such as budget overruns, unexpected surges in usage, or misallocated resources.
This process enables you to foresee potential pitfalls and establish controls that minimize the likelihood of these risks materializing.

## Do continuous improvement

By embracing continuous improvement within the context of FinOps, you’re committing to regular assessments of your cloud environment, cost patterns, and optimization strategies.
This entails gathering feedback from teams, analysing data-driven insights, and leveraging lessons learned to iteratively enhance your cloud operations.

## Bibliography

- [10 Best Practices for FinOps](https://www.densify.com/resources/cloud-cost-management-best-practices/)
- [10 Best Practices to Reduce Your Cloud Bill](https://www.digitalocean.com/resources/articles/cloud-cost-optimization)
- [15 Best Practices to Reduce Your Cloud Bill](https://spot.io/resources/cloud-cost/cloud-cost-optimization-15-ways-to-optimize-your-cloud/)
- [15 Essential FinOps Best Practices to Know](https://solutionsreview.com/cloud-platforms/the-long-list-essential-finops-best-practices-to-know/)
- [17 Cloud Cost Optimization Best Practices](https://spacelift.io/blog/cloud-cost-optimization)
- [20 FinOps Best Practices](https://redblink.com/finops-best-practices/)
- [6 FinOps Principles & Best Practices](https://blog.economize.cloud/finops-principles/)
- [8 FinOps Best Practices](https://www.nops.io/blog/top-finops-practices-to-effectively-manage-cloud-costs/)
- [Cloud FinOps, 2nd Edition](https://www.oreilly.com/library/view/cloud-finops-2nd/9781492098348/)
- [The 25+ Best Cloud Cost Management Tools](https://www.cloudzero.com/blog/cloud-cost-management-tools/)
