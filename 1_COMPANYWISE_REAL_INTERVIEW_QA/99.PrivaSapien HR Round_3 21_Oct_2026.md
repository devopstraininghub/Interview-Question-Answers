# DevOps Interview Questions and Answers (4 Years Experience)
### Q1. How many years of experience do you have?
**Ans:** Four years.
### Q2. Where have you been working until now?
**Ans:** VSL Infotech is my first company.
### Q3. Where is the company based?
**Ans:** Bangalore.
### Q4. What skills have you gained over the last four years?
**Ans:** My main reason for looking for a change is career and technical growth. I have spent more than four years building experience in AWS, Kubernetes, Terraform, CI/CD, security, and production operations. Now I want to take on more challenging responsibilities.
### Q5. Why do you want to leave your current job and join PrivaSapien?
**Ans:** My main reason is career and technical growth. I am interested in PrivaSapien because your work combines DevOps with privacy, security, and AI workloads.
### Q6. What does PrivaSapien do?
**Ans:** From my understanding, PrivaSapien focuses on privacy-enhancing and responsible AI technology. Your platform helps organizations identify and manage privacy risks in data and AI systems.
### Q7. Name any two privacy-enhancing technologies.
**Ans:** Differential privacy and data anonymization.
### Q8. What is data anonymization?
**Ans:** Data anonymization is the process of removing or transforming personally identifiable information so that the data cannot reasonably be linked back to a specific individual.
For example, we can remove a customer's name and email address.
### Q9. What does K-anonymity mean?
**Ans:** To be honest, I haven't heard about K-anonymity.
### Q10. Your GitLab is throwing errors. Images are not getting pulled, and there are problems with merging. What could be the probable causes?
**Ans:** I would first investigate GitLab.
For container image pull failures, I would check:
- Registry authentication or expired credentials.
- Incorrect image name or tag.
- Registry availability.
- Network or DNS connectivity.
- Access permissions.
For merge failures, I would check the merge-related issues.
I would also check disk space, storage availability on the GitLab server, and GitLab error logs.
### Q11. If GitLab storage increases from a few GB to 100 GB and then to 1 TB, what will be the cost implication?
**Ans:** Yes, the storage cost will increase significantly.
### Q12. What would be your solution to reduce GitLab backup storage costs?
**Ans:** I would avoid repeated full backups of unchanged data.
For repositories and critical GitLab metadata, I would maintain regular backups based on the required RPO.
For large container images, artifacts, and packages, I would use S3 object storage with versioning and lifecycle policies instead of including all the data in every server backup.
For underlying storage, I would use incremental snapshots wherever supported. This stores only the changed blocks after the initial backup.
This reduces backup size and storage costs while maintaining the required recovery capability.
### Q13. What should be backed up and what should not be backed up in GitLab?
**Ans:** I would categorize GitLab data based on criticality, recoverability, and retention requirements.
I classify the following as critical:
- PostgreSQL database.
- Git repositories.
- GitLab configuration and secrets.
- Uploads and keys.
I would back these up frequently according to the required RPO and keep copies outside the GitLab server.
I classify container images and required artifacts as large persistent objects. I would keep these in object storage such as S3 and protect them using versioning.
I classify runner workspace, Docker layer caches, CI caches, temporary files, and build files as disposable. I would not back these up because they can be recreated whenever required.
### Q14. As a newly onboarded DevOps Engineer, how would you plan your first 30 days?
**Ans:** I would plan the first five days to understand the product, the team, and the project.
I would also understand the complete delivery flow from source code to production.
I would then move on to experimenting in a sandbox environment, understanding the CI/CD pipeline, and validating deployments.
### Q15. What do you know about security, and which tools have you worked with?
**Ans:** I have worked with SonarQube and Trivy.
At the cloud level, I use IAM least-privilege rules instead of long-lived access keys.
For Kubernetes and EKS, I use RBAC, namespace isolation, and service accounts with controlled AWS permissions.
In CI/CD, I keep secrets out of source code, restrict pipeline permissions, use approval gates for production, and integrate SonarQube and Trivy to check code quality and container vulnerabilities before deployment.
### Q16. What is the difference between SonarQube and Linting?
**Ans:** Linting is mainly used for fast, language-specific checks while developers write or commit code. It detects issues such as syntax problems and formatting violations.
SonarQube is used for static code analysis and centralized quality control.
It analyzes bugs, vulnerabilities, code smells, code duplication, and test coverage.
### Q17. How would you define a quality gate in SonarQube?
**Ans:** I define a quality gate as a set of conditions that must be satisfied before code is allowed to progress through the CI/CD pipeline.
I normally apply the gate to new code. I check conditions such as new vulnerabilities, reliability issues, maintainability issues, and duplicated code.
For example, I can require no new high-severity security issues, sufficient test coverage, and duplication below an agreed threshold.
I can use the built-in Sonar Way quality gate or create a custom quality gate based on product standards.
### Q18. How would you introduce SonarQube into a team that already has a lot of legacy code? How would you prevent quality gates from stopping existing development work?
**Ans:** I would not apply strict quality gates to the entire legacy codebase immediately because existing technical debt could block every build, even when developers have not introduced those issues.
I would define a quality gate as a clear pass-or-fail policy for code quality.
For new code, I would start with practical conditions such as:
- No new critical vulnerabilities.
- All new security hotspots must be reviewed.
- At least 80% test coverage on new code.
- Duplicated code below 3%.
I would not enable strict blocking on the first day for an existing application.
First, I would deploy SonarQube and connect one representative repository. I would configure the correct language rules and run a baseline scan to understand the existing technical debt.
### Q19. What is the difference between a vulnerability and a security hotspot?
**Ans:** A hotspot identifies security-sensitive code that requires human review. It does not automatically mean the code is vulnerable.
After reviewing the context, I mark the hotspot as safe or identify the security problem and fix it.
### Q20. Have you worked with Trivy?
**Ans:** Yes. I have worked with Trivy, mainly for container image vulnerability scanning.
### Q21. Are you comfortable working from the Bangalore office five days a week and on alternate Saturdays?
**Ans:** Yes, I am comfortable working alternate Saturdays.
### Q22. Are you comfortable working occasional night shifts when required for releases?
**Ans:** Yes, I am comfortable working occasional night shifts.
### Q23. When can you join?
**Ans:** I can join immediately.
### Q24. Why can't you join from next Monday?
**Ans:** My brother is leaving for Canada, so I have a few things to complete here.
### Q25. Are you comfortable travelling for an in-person interaction with one of the DevOps engineers?
**Ans:** The transcript does not contain a clear answer from Vineet.
### Q26. Have you worked on on-premises environments and bare-metal servers?
**Ans:** Yes. I have worked with on-premises environments, mainly around Jenkins and Linux servers.
I have handled server configuration, CI/CD integration, network checks, service troubleshooting, and monitoring.
### Q27. What is your current CTC, and what are your salary expectations?
**Ans:** My current CTC is 7.8 LPA, and I am expecting between 11 and 12.5 LPA based on current market standards.
### Q28. If selected, what will my roles and responsibilities be during the first three months?
**Ans:** I would like to understand my roles and responsibilities, priorities during the first three months, and what ownership would be expected from me as a DevOps Engineer.
### Q29. Is this an ongoing project or a new project?
**Ans:** The interviewer explained that the company is hiring me as part of its permanent team, not for a specific project.
The company has multiple clients and projects. Depending on the workload, I may be assigned to a client project or the internal team.

