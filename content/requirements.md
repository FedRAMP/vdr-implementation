# Implementation Requirements

Cloud service providers are required to address all FedRAMP Practices in the Vulnerability Detection and Response and Vulnerability Evaluation and Reporting rulesets. To address a rule, you are expected to:

1. Understand the rule and consider its implications
2. Determine its appropriate application(s) in your particular environment, against your particular model
3. Implement the appropriate application(s)
4. Adopt ways to verify and validate the implementations on a persistent basis
5. Consider the risk to customer data based on the implementations and ways the customer may compensate
5. Document the implementations, verifications, validations, and risk

!!! tip "Review the Security Decision Record rules"

    For reference, providers should consult the Security Decision Record ruleset to understand what will be expected
    of them when they adopt that rule in particular, especially [SDR-CSO-FRR (FedRAMP Rules)](https://www.fedramp.gov/2026/reference/security-decision-record/#fedramp-rules).

## Fully vs Partially Addressed

To consider the ruleset **Fully Addressed**:

1. All MUST or MUST NOT rules are considered fully implemented such that all requirements and expectations of the rule are met and the security outcomes of the implementation are known.

2. All SHOULD or SHOULD NOT rules have been either been fully implemented such that all requirements and expectations of the rule are met and the security outcomes of the implementation are known; OR partially/not implemented with corresponding documentation explaining the valid reasons for not implementing the full requirements and expectations of the rule, with the risk of the implementation for both the service and customers documented.

3. All MAY rules have been considered and implemented or not, with the result documented.

Anything less, even a single MUST rule that is not fully implemented, means that ruleset is **Partially Addressed** - unless the ruleset has been ignored entirely, then it is simply **Not Addressed** (and that's very bad).

## Depth and Complexity of Implementation

FedRAMP recommends review the [It's Not a Trap!](https://www.fedramp.gov/2026/rules/#its-not-a-trap) section of [Using the Consolidated Rules for 2026](https://www.fedramp.gov/2026/rules/) while implementing the VDR/VER, especially for cloud service providers that are focusing specifically on those two rulesets first.

In short, FedRAMP acknowledges that there are many different implementations for effective vulnerability detection and response that work differently in many different environments. Cloud service providers should work with their security engineering team to take credit for the good security work being done across the organization instead of over-indexing on simply replacing the inefficient (and ineffective) historical vulnerability-scanning-only approach to vulnerability detection and response.

!!! tip "Do good security!"

    The VDR/VER rules are designed to reward good security practices such that most companies following modern
    vulnerability detection and response best practices should not need to redesign their security processes around
    FedRAMP requirements. Secure cloud services are already doing most of these practices, such as evaluating the
    exploitability and potential impact of vulnerabilities before prioritizing them based on risk.

    The compliance overhead should hit primarily in the reporting requirements.

