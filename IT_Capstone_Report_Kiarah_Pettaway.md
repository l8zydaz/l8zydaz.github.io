Design and Implementation of a Security Monitoring Program for a Small
Game Development Studio

Kiarah T. Pettaway

Western Governors University

##  Table of Contents

[**Table of Contents 1**](#table-of-contents)

[Summary 3](#summary)

[Review of Other Work 3](#review-of-other-work)

> [Work 1 3](#)
>
> [Work 2 4](#)
>
> [Work 3 4](#)
>
> [How Each Work Supported the Implementation
> 4](#how-each-work-supported-the-implementation)

[Changes to the Project Environment
4](#changes-to-the-project-environment)

[Methodology 6](#methodology)

[Project, Goals, and Objectives 7](#project-goals-and-objectives)

[Project Timeline 7](#project-timeline)

[Unanticipated Scope Creep 8](#unanticipated-scope-creep)

[Conclusion 8](#conclusion)

[**References 11**](#references)

## Summary

This experiment with Ablique Game Studios aimed to implement a
centralized security monitoring solution to detect suspicious activity
in a simulated small game development office. Task 2 identified a lack
of centralized monitoring and alerting, which limits the detection of
illicit access, credential misuse, and abnormal behavior.

The project was carried out by deploying a cloud-based security
monitoring solution using Microsoft Sentinel. Log ingestion was
configured to collect authentication and system activity from endpoints
and servers within the simulated environment. Detection rules were then
created to discover suspicious behavior such as repeated authentication
failures, abnormal login patterns, and privilege escalation attempts.

Simulated unauthorized conduct validated the monitoring system. These
actions triggered alerts, enabling investigation and documentation. The
project demonstrates that centralized monitoring augments security
visibility and speeds identification of suspicious activity.

## Review of Other Work

### **Work 1**

*Microsoft Sentinel Best Practices Guide*

The Microsoft Sentinel documentation provides guidance on configuring
data connectors, analytics rules, and investigation workflows to improve
security monitoring capabilities. The documentation emphasizes
centralized log collection and automated alert generation as necessary
aspects of effective security operations.

### Work 2

*SANS SIEM Implementation Guide*

The SANS Institute provides guidance on implementing SIEM platforms to
improve threat identification and incident response. Their research
emphasizes the importance of establishing baseline behavior and
configuring detection rules to identify abnormal activity patterns.

### **Work 3**

*Microsoft Security Operations Documentation*

Microsoft security operations guidance describes the investigation
workflows administrators use to analyze alerts and detect possible
security incidents.

### How Each Work Supported the Implementation

The Microsoft Sentinel documentation supported the implementation of the
monitoring platform by providing guidance on configuring data connectors
and enabling log ingestion.

The SANS SIEM implementation guidance supported the development of
detection rules by describing how abnormal authentication behavior can
show potential security threats.

Microsoft security operations documentation supported the investigation
phase by outlining how alerts can be analyzed and interpreted during
incident response activities.

## Changes to the Project Environment

Following the implementation of Microsoft Sentinel, Ablique Game Studios
experienced several functional and cultural changes within its security
environment. Prior to the implementation, the organization lacked
centralized monitoring capabilities, meaning system activity and
authentication events were not actively analyzed for suspicious
behavior. This limited Ablique's ability to recognize potential security
incidents in a timely manner.

The introduction and implementation of Microsoft Sentinel established a
centralized security monitoring platform that aggregates authentication
and system activity logs from across the environment. This change
altered the organization's operational approach to security by enabling
administrators to continuously monitor system activity, investigate
alerts, and handle potential incidents more effectively.

From a strategic standpoint, implementing Sentinel shifted the
organization from a largely reactive security posture to a more
proactive one. Admins can now identify abnormal login behavior,
investigate alerts, and take action before suspicious activity escalates
into a larger security incident.

Additionally, the implementation supports a more extensive
organizational shift towards security awareness within Ablique, with
monitoring and alerting capabilities in place, making security an
ongoing operational function rather than a reactive process performed
only after incidents occur.

Overall, the implementation of Microsoft Sentinel strengthened Ablique's
security environment by improving visibility, supporting proactive
threat detection, and integrating monitoring into the organization's
daily security operations.

## Methodology

This project followed a staged implementation methodology aligned with
the waterfall model. Each stage was executed sequentially to ensure the
monitoring system was configured and validated in a structured manner.

The first phase entailed preparing the monitoring environment by
creating a cloud-hosted Microsoft Sentinel workspace and enabling log
ingestion from system and authentication logs.

The second phase comprised generating baseline activity within the
simulated environment to establish normal behavioral patterns.

The third phase consisted of configuring detection rules to discover
suspicious behavior, including repeated authentication failures and
abnormal login patterns.

The fourth phase encompassed performing simulated attack activity
designed to trigger detection rules and generate alerts.

The final phase entailed investigating the generated alerts and
evaluating Microsoft Sentinel\'s effectiveness.

## Project, Goals, and Objectives

One of the project\'s primary goals was to establish a centralized
monitoring solution within Ablique Game Studios to enable in-depth
visibility across the environment. The goal was accomplished by
configuring Microsoft Sentinel to collect authentication and system
activity logs from endpoints within the environment.

Supporting objectives included creating detection rules and validating
alert generation through simulated unapproved activity. These objectives
were successfully achieved, as the configured detection rules generated
alerts when abnormal login activity occurred.

## Project Timeline

  -----------------------------------------------------------------------
  **Milestone**     **Planned Dates** **Actual          **Notes**
                                      Completion**      
  ----------------- ----------------- ----------------- -----------------
  Configure         March 1-2, 2026   March 2, 2026     Completed on
  Sentinel                                              schedule
  workspace                                             

  Configure log     March 3-4, 2026   March 4, 2026     Data connectors
  ingestion                                             verified

  Create detection  March 5-6, 2026   March 6, 2026     Rules configured
  rules                                                 successfully

  Simulate          March 7-8, 2026   March 8, 2026     Alerts triggered
  suspicious                                            correctly
  activity                                              

  Investigate       March 9, 2026     March 9, 2026     Incident review
  alerts                                                completed

  Final evaluation  March 10, 2026    March 10, 2026    Finalize report
  and documentation                                     
  -----------------------------------------------------------------------

The project schedule established in the Proposal was largely followed
during implementation. Environment preparation and log ingestion were
completed within the planned timeframe. Detection rule configuration and
simulated attack testing were completed successfully with minimal
delays. Overall, the project benchmarks were achieved within the
anticipated timeline.

## Unanticipated Scope Creep

One obstacle encountered during this project involved configuring log
ingestion correctly within Microsoft Sentinel. Initial attempts to
collect authentication events did not yield the expected telemetry,
prompting further troubleshooting of the data connector configuration.
The issue was resolved by adjusting the data connector settings and
verifying that security event logs were successfully being forwarded to
the monitoring workspace. Once corrected, Sentinel began receiving the
required event data.

## Conclusion

The objective of this project was to design and implement a centralized
security monitoring solution capable of detecting suspicious
authentication and system activity within a simulated small game
development office environment. Prior to implementing this solution, the
organization lacked centralized monitoring capabilities, limiting
visibility pertaining to potential unauthorized login attempts and
abnormal user behavior.

To address this issue, a cloud-based monitoring platform was deployed
using Microsoft Sentinel. Log ingestion was configured to collect
authentication and system activity data from the simulated environment,
enabling centralized visibility into security events. Detection rules
were then configured to identify abnormal activity patterns, including
repeated failed login attempts and unusual sign-in behavior that may
show potential brute-force attacks or illicit access attempts.

Simulated suspicious activity was introduced into the environment to
validate the monitoring solution. The configured analytics rules
successfully generated alerts and security incidents in Microsoft
Sentinel, demonstrating that the monitoring system could identify
abnormal authentication activity and notify administrators of possible
threats.

The results of the implementation confirm that centralized monitoring
significantly improves an organization's ability to detect suspicious
activity and investigate potential security incidents. By aggregating
security telemetry and applying automated recognition logic, the
monitoring platform provides administrators with the visibility required
to respond to prospective threats in a timely manner.

Based on the evaluation criteria defined in Task 2, the project was
considered successful following the fine-tuned implementation of
Microsoft Sentinel within Ablique Game Studio's environment. The
monitoring system consistently generated alerts for simulated malicious
activity, while normal user behavior did not produce excessive false
positives. These results show that the implemented monitoring solution
met the defined evaluation framework by detecting suspicious activity
while upholding accurate alerting behavior. Consequently, the solution
substantially increases security visibility and supports the
identification and investigation of potential security incidents within
the environment.

## References

Microsoft. (2024). Microsoft Sentinel documentation. Microsoft Learn.

https://learn.microsoft.com/en-us/azure/sentinel/

SANS Institute. (2023). Security information and event management (SIEM)
implementation best practices.

https://www.sans.org/white-papers/

Microsoft. (2024). Security operations and incident response
documentation. Microsoft Learn.

https://learn.microsoft.com/en-us/security/operations/

**Appendix A**

**Artifact A**

*Microsoft Sentinel Dashboard*![](media/image3.png){width="6.5in"
height="2.852777777777778in"}

Artifact A displays the Microsoft Sentinel monitoring workspace
configured during the Ablique Game Studio's implementation phase. The
dashboard shows security event logs being ingested from the simulated
environment, including authentication and system activity generated by
user workstations. Consequently, this demonstrates that Microsoft
Sentinel was successfully implemented and that the monitoring platform
is collecting telemetry from the environment. This function allows
administrators to observe system activity and identify abnormal events
that may indicate suspicious behavior.

**Appendix B**

**Artifact B**

*Brute Force Sign-in Attempt*![](media/image1.png){width="6.5in"
height="3.2694444444444444in"}![](media/image4.png){width="6.5in"
height="3.2694444444444444in"}

Artifact B displays the analytics rule configured within Microsoft
Sentinel to detect suspicious authentication activity. The rule, labeled
"(Ems) Brute Force Sign-in Attempt," analyzes sign-in log data to
identify multiple failed login attempts that may indicate a brute-force
attack against user accounts. The rule uses query logic to monitor
authentication events and generates alerts when the number of failed
login attempts exceeds a predefined threshold within a specified time
period. This artifact demonstrates how the monitoring platform was
configured to automatically detect abnormal login behavior and support
the identification of potential unauthorized access attempts within the
environment.

**Appendix C**

**Artifact C**

*Incidents View*![](media/image5.png){width="6.5in"
height="3.2694444444444444in"}

Artifact C displays the incidents view within Microsoft Sentinel after
detection rules were executed in the monitored environment. The
screenshot shows multiple security incidents generated by the monitoring
platform, including alerts triggered by configured analytics rules that
analyze authentication and system activity logs. Each incident contains
details such as severity level, time of detection, associated alerts,
and the analytics rule that generated the alert. This artifact
demonstrates that the monitoring system successfully detected suspicious
or abnormal activity and generated alerts for investigation,
substantiating the effectiveness of the implemented monitoring solution.
