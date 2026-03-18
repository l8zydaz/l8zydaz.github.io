# Design and Implementation of a Security Monitoring Program for a Small Game Development Studio

# Kiarah T. Pettaway

# Western Governors University

## Table of Contents

> [Problem Summary 3](#problem-summary)
>
> [IT Solution 3](#it-solution)
>
> [Implementation Plan 4](#implementation-plan)
>
> [Phase 1 --- Environment Preparation
> 4](#phase-1-environment-preparation)
>
> [Phase 2 --- Monitoring Deployment 5](#phase-2-monitoring-deployment)
>
> [Phase 3 --- Detection Configuration
> 5](#phase-3-detection-configuration)
>
> [Phase 4 --- Activity Simulation and Evaluation
> 5](#phase-4-activity-simulation-and-evaluation)
>
> [Phase 5 --- Tuning and Documentation
> 5](#phase-5-tuning-and-documentation)
>
> [Justification of Plan 6](#justification-of-plan)

[Review of Other Work 6](#review-of-other-work)

> [Summary of Four Works 6](#summary-of-four-works)
>
> [Relation of Works to Proposal Design
> 7](#relation-of-works-to-proposal-design)
>
> [Project Rationale 8](#project-rationale)
>
> [Current Project Environment 9](#current-project-environment)
>
> [Methodology 12](#methodology)
>
> [Project Goals, Objectives, and Deliverables
> 13](#project-goals-objectives-and-deliverables)
>
> [Project Goals 13](#headingh.xymtx16jl6x7)
>
> [Project Objectives 13](#headingh.xymtx16jl6x7)
>
> [Project Deliverables 14](#headingh.xymtx16jl6x7)
>
> [Goals, Objectives, and Deliverables Descriptions
> 14](#goals-objectives-and-deliverables-descriptions)
>
> [Goals, Objectives, and Deliverables Table
> 15](#goals-objectives-and-deliverables-table)
>
> [Project Timeline with Milestones
> 16](#project-timeline-with-milestones)
>
> [Outcome 17](#outcome)
>
> [References 19](#references)

**Proposal Overview**

## Problem Summary

Small game studios often lack centralized monitoring due to limited
security resources and online collaboration. This deficiency elevates
the risk of undetected unauthorized access, credential misuse, and
improper access to unreleased assets.

Ablique Game Studios is a small studio comprising approximately 18
employees, including developers, artists, and remote contractors,
supported by 10 managed workstations and 2 internal servers. The lack of
centralized visibility into authentication and system activity hinders
reliable detection and investigation of suspicious behavior, thereby
increasing the threat of data exposure and project disruption.

## IT Solution

The proposed solution entails implementing a centralized security
monitoring platform using Microsoft Sentinel, integrated with Windows
security event telemetry. This platform will collect and analyze
authentication, system, and account activity across the simulated studio
environment to expand visibility concerning user behavior and system
access. Microsoft Sentinel will serve as the central security
information and event management (SIEM) system, aggregating logs from
managed workstations and servers. The solution will enable alerting and
investigation of suspicious behaviors, including repeated authentication
failures, unauthorized privilege changes, remote logins such as
impossible travel, and persistence mechanisms.

Detection rules will be configured to identify abnormal activity
patterns and generate alerts to support the investigation of potential
security incidents. This procedure enables monitoring of access to
development resources and facilitates response to unauthorized
activities that would otherwise remain undetected in a decentralized
environment.

Implementing centralized monitoring augments security visibility,
accelerates incident identification, and enables evaluation of the
security posture within resource-limited environments.

## Implementation Plan 

The project will be implemented in phases to simulate the rollout of a
monitoring platform at Ablique Game Studios.

### Phase 1 --- Environment Preparation

A simulated studio network representing Ablique Game Studios will be
created, consisting of workstations and servers that represent user
systems and shared development resources. Baseline system activity will
be observed to establish normal operational patterns prior to monitoring
implementation.

### Phase 2 --- Monitoring Deployment

Microsoft Sentinel will be configured and connected to system telemetry
sources. Security event data from managed systems will be ingested into
the monitoring platform to establish centralized visibility.

### Phase 3 --- Detection Configuration

Detection rules will be developed to discover suspicious authentication
attempts, privilege changes, remote access activity, and
persistence-related behaviors. Alert generation will be validated to
ensure that events are captured by the monitoring system.

### Phase 4 --- Activity Simulation and Evaluation

Controlled security events representing unauthorized behavior will be
generated within the environment. The monitoring platform's ability to
detect and alert on these activities will be measured and documented.

### Phase 5 --- Tuning and Documentation

Detection rules will be refined to reduce false positives and improve
reliability. Final system behavior and monitoring effectiveness will be
documented for evaluation.

## Justification of Plan

The implementation plan is appropriate for this project because it
enables the introduction of monitoring capabilities in a controlled,
measurable manner. Beginning with environment preparation and baseline
activity assures that normal system operation is understood before
detection rules are introduced. Deploying the monitoring platform and
ingesting logs before configuring alerts guarantees sufficient telemetry
for accurate analysis. Simulated attack activity is introduced only
after detection rules are validated, allowing the system to be tested
under regulated conditions. This well-structured sequence reduces
configuration errors and ensures that each stage of the monitoring
solution operates properly before moving to the next phase.

# Review of Other Work

## Summary of Four Works 

Microsoft security monitoring guidance explains that centralized log
collection and alert correlation considerably improve an organization's
ability to detect unauthorized entry and suspicious behavior. The
documentation emphasizes monitoring authentication activity and account
usage trends to identify abnormal behavior and support incident
investigation processes (Microsoft, 2024).

MITRE ATT&CK framework delivers a structured catalog of real-world
adversary behaviors and techniques observed during security incidents.
The framework identifies attack methods such as credential misuse,
persistence, and lateral movement that can be detected through
monitoring systems and authentication events (MITRE, 2024).

NIST security logging and monitoring recommendations describe
centralized auditing as a core security control. The guidance notes that
organizations lacking monitoring capabilities often fail to detect
compromises until after operational or data damage has occurred,
strengthening the significance of ongoing visibility into system
activity (NIST, 2011).

Security monitoring implementation guidance recommends a phased
deployment consisting of baseline log collection, alert creation, and
assessment through simulated attack activity to ensure detection
effectiveness (Microsoft 2024).

## Relation of Works to Proposal Design

The proposed monitoring platform is directly informed by the practices
and frameworks described in the reviewed literature.

Microsoft security monitoring guidance emphasizes centralized log
collection and analysis to identify abnormal account behavior. The
project implements this concept by aggregating authentication and system
activity from endpoints and servers into a single monitoring platform,
enabling visibility into user activity across Ablique Game Studios.

The MITRE ATT&CK framework identifies adversary techniques such as
credential misuse, persistence, and lateral movement. Detection rules
within the monitoring platform are designed to detect these behaviors
through analyzing authentication failures, abnormal login patterns, and
privilege escalation events generated during simulated attack activity.

NIST continuous monitoring guidance recommends maintaining ongoing
awareness of system activity using centralized auditing. The project
applies this recommendation by continuously collecting system and
security logs and establishing a behavioral baseline to differentiate
normal activity from suspicious events.

Security monitoring implementation guidance describes a phased
deployment consisting of log creation, alert creation, and validation of
monitoring effectiveness by controlled attack simulations and incident
analysis.

## Project Rationale

Small organizations commonly lack dedicated security personnel and
centralized monitoring capabilities, impeding timely detection of
unauthorized access and account misuse. Because development environments
handle source code and intellectual property, delayed detection of
suspicious activity can result in business interruptions or data
exposure. Failure to detect unauthorized access may delay development
timelines and expose unreleased intellectual property, thereby adversely
affecting business operations and client or partner trust.

This project demonstrates the implementation of a realistic monitoring
architecture using accessible cloud-based security tools instead of
enterprise-only infrastructure. By simulating a small game development
office environment, designated as Ablique Game Studios, the solution
reflects conditions commonly found in small businesses that must balance
security requirements with limited resources.

Additionally, this project provides a practical demonstration of
security operations concepts, including log aggregation, behavioral
detection, and incident investigation. Rather than describing monitoring
theory, the implementation illustrates how detection rules pinpoint
suspicious behavior and how alerts can be analyzed within an
investigation workflow.

The system serves as a proof-of-concept (PoC) for small organizations
such as Ablique Game Studios, providing practical monitoring strategies
and a professional demonstration of applied security operations skills
that meet industry standards.

## Current Project Environment

Small organizations commonly lack dedicated security personnel and
centralized monitoring capabilities, impeding timely detection of
unauthorized access and account misuse. Because development environments
handle source code and intellectual property, delayed detection of
suspicious activity can result in business interruptions or data
exposure. Failure to detect unauthorized access may delay development
timelines and expose unreleased intellectual property, thereby adversely
affecting business operations and client or partner trust.

This project demonstrates the implementation of a realistic monitoring
architecture using accessible cloud-based security tools instead of
enterprise-only infrastructure. By simulating a small game development
office environment, designated as Ablique Game Studios, the solution
reflects conditions commonly found in small businesses that must balance
security requirements with limited resources.

Additionally, this project provides a practical demonstration of
security operations concepts, including log aggregation, behavioral
detection, and incident investigation. Rather than describing monitoring
theory, the implementation illustrates how detection rules pinpoint
suspicious behavior and how alerts can be analyzed within an
investigation workflow.

The system serves as a proof-of-concept (PoC) for small organizations
such as Ablique Game Studios, providing practical monitoring strategies
and a professional demonstration of applied security operations skills
that meet industry standards.

## Methodology

This project follows a staged implementation methodology aligned with a
simplified waterfall model in a simulated small-business environment.
The waterfall approach is appropriate because each stage of the
monitoring system depends on the successful completion of the previous
stage. Environment preparation and log ingestion must occur before
detection rules can be created, and detection rules must be configured
before simulated attack activity can be tested. This logical methodology
assures that monitoring capabilities are implemented and validated in a
logical sequence, reducing configuration errors and improving the
reliability of detection results.

Initially, the monitoring platform will be set up by creating a
cloud-hosted security workspace and enabling log ingestion. Data
connectors will be configured to collect authentication and system
activity from endpoints and servers within the simulated environment.

Subsequently, baseline activity will be generated through normal user
behavior, including logins, file access, and account usage. This
activity will establish expected behavioral patterns for comparison
against abnormal events.

Detection rules will be created to discover suspicious activity. These
rules will monitor repeated authentication failures, abnormal login
patterns, and privilege escalation attempts. Each rule will generate
alerts when configured thresholds are exceeded. After rule creation,
simulated attack activity will be run in the environment. Test scenarios
will include password-guessing attempts, unauthorized access, and
abnormal account usage, designed to trigger the detection rules.

Generated alerts will be investigated within the monitoring platform.
Incident details, including timestamps, affected accounts, and
triggering events, will be documented to evaluate detection validity.
Finally, monitoring effectiveness will be evaluated by confirming that
alerts are generated for malicious behavior while normal activity does
not produce excessive false positives.

The monitoring workflow will demonstrate how a system administrator
reviews and interprets alerts during routine operations.

## Project Goals, Objectives, and Deliverables

### Project Goals

This project aims to design and demonstrate a practical security
monitoring platform capable of detecting suspicious activity in a
simulated small-business environment. It demonstrates how centralized
monitoring improves visibility into system activity and supports
incident investigation using accessible cloud-based security tools.

### Project Objectives

1.  Configure a centralized monitoring platform to collect
    > authentication and system activity logs from endpoints and
    > servers.

2.  []{#headingh.xymtx16jl6x7 .anchor}Establish a baseline of normal
    > user activity within the environment.

3.  Create detection rules to identify abnormal behavior, including
    > repeated authentication failures, anomalous login activity, and
    > attempts to escalate privileges.

4.  []{#headingh.xymtx16jl6x7 .anchor}Simulate unauthorized behavior
    > designed to trigger detection rules.

5.  Investigate generated alerts and document incident details.

6.  []{#headingh.xymtx16jl6x7 .anchor}Evaluate monitoring effectiveness
    > by confirming that malicious behavior triggers alerts while normal
    > activity does not generate excessive false positives.

### Project Deliverables

-   Configured monitoring workspace with active ingestion

-   []{#headingh.xymtx16jl6x7 .anchor}Documented detection rules and
    > alert logic

-   Screenshots of generated alerts and incidents

-   []{#headingh.xymtx16jl6x7 .anchor}Investigation documentation
    > describing detected activity

-   Evaluation summary of monitoring effectiveness

-   []{#headingh.xymtx16jl6x7 .anchor}Final implementation report
    > describing system design and results

## Goals, Objectives, and Deliverables Descriptions

The primary focus of the project is to demonstrate how centralized
monitoring improves security visibility within the small organizational
environment of Ablique Game Studios. The monitoring platform provides
insight into authentication and system activity that would otherwise
remain isolated on individual machines, enabling identification and
investigation of suspicious behavior.

To achieve this goal, the project establishes normal operating
conditions by generating typical user activity, such as logins and file
access. This baseline enables differentiation of abnormal behavior from
expected behavior. Detection rules are configured to identify events
that may indicate unauthorized conduct, including repeated
authentication failures and privilege changes. Simulated attack activity
is introduced to evaluate whether the monitoring platform produces
alerts accurately. Each alert is reviewed to determine the triggering
behavior and confirm that the detection logic functions as intended. The
investigation process demonstrates how monitoring data supports incident
analysis rather than merely generating notifications.

The project deliverables provide evidence of implementation and
effectiveness. Configuration documentation shows how monitoring was
established, alert screenshots confirm detection occurred, and the
evaluation summary explains how the system performed. Together, these
deliverables demonstrate both the technical implementation and the
practical value of centralized monitoring.

## Goals, Objectives, and Deliverables Table

  -----------------------------------------------------------------------------
      **Goal**        **Supporting Objectives** **Deliverables Enabling the
                                                Project Objectives**
  --- --------------- ------------------------- -------------------------------
  1   Establish       Configure the monitoring  Screenshot setup of monitoring
      centralized     platform                  platform
      monitoring                                
      visibility                                

                                                

                                                

                      Ingest authentication and Screenshot showing active log
                      system logs               ingestion and connected data
                                                sources

                                                

                                                

                                                

                                                

                                                

  2   Detect          Create detection rules    Screenshot showing active
      suspicious      and trigger alerts        alerts using simulated
      activity                                  unauthorized behavior

                                                

                                                

                                                

                                                

                                                

                                                

                                                

                                                

  3   Validate        Investigate alerts and    Investigation documentation and
      monitoring      evaluate detection        final evaluation summary
      effectiveness   validity                  

                                                

                                                

                                                

                                                

                                                

                                                

                                                

                                                
  -----------------------------------------------------------------------------

## Project Timeline with Milestones

+----------------+----------------+-----------------+-----------------+
| **Milestone**  | **Duration**   | **Projected     | **Anticipated   |
|                |                | Start Date**    | End Date**      |
|                | **(hours or    |                 |                 |
|                | days)**        |                 |                 |
+================+================+=================+=================+
| Environment    | 2 days         | March 10, 2026  | March 11, 2026  |
| Preparation    |                |                 |                 |
+----------------+----------------+-----------------+-----------------+
| Log            | 3 days         | March 12, 2026  | March 14, 2026  |
| Integration    |                |                 |                 |
+----------------+----------------+-----------------+-----------------+
| Baseline       | 2 days         | March 15, 2026  | March 16, 2026  |
| Activity       |                |                 |                 |
| Generation     |                |                 |                 |
+----------------+----------------+-----------------+-----------------+
| Detection Rule | 3 days         | March 17, 2026  | March 19, 2026  |
| Configuration  |                |                 |                 |
+----------------+----------------+-----------------+-----------------+
| Attack         | 2 days         | March 20, 2026  | March 21, 2026  |
| Simulation     |                |                 |                 |
| Testing        |                |                 |                 |
+----------------+----------------+-----------------+-----------------+
| Alert          | 3 days         | March 22, 2026  | March 24, 2026  |
| Investigation  |                |                 |                 |
| & Validation   |                |                 |                 |
+----------------+----------------+-----------------+-----------------+
| Evaluation &   | 4 days         | March 25, 2026  | March 28, 2026  |
| Final          |                |                 |                 |
| Documentation  |                |                 |                 |
+----------------+----------------+-----------------+-----------------+

## Outcome

The completed project demonstrates a functional centralized monitoring
platform capable of detecting suspicious activity in a simulated
small-business environment named Ablique Game Studios. Authentication
events and system activity are collected and analyzed to trigger alerts
when abnormal behavior is detected.

Simulated unauthorized acts trigger detection rules, generating
incidents that can be investigated through the monitoring platform. The
investigation process demonstrates how collected log data provides
visibility into account activity, event timelines, and triggering
behaviors. The project confirms that centralized monitoring improves the
ability to identify and analyze potential security events compared to an
environment without aggregated visibility. The final implementation
provides documented evidence of detection, investigation, and evaluation
results. Effectiveness is evaluated based on whether simulated malicious
actions steadily generate alerts while normal activity does not produce
excessive false positives.

## References

"Microsoft Sentinel Documentation." Microsoft Learn,
learn.microsoft.com/en-us/azure/sentinel/. Accessed 1 Mar. 2026.

"Mitre ATT&CK®." MITRE ATT&CK®, attack.mitre.org/. Accessed 1 Mar. 2026.

NIST SP 800-137, Information Security Continuous Monitoring \...,
nvlpubs.nist.gov/nistpubs/legacy/sp/nistspecialpublication800-137.pdf.
Accessed 1 Mar. 2026.
