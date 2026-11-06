# Mini-SDR Schemas and CSV Templates

FedRAMP is requesting that all cloud service providers include a VDR/VER implementation-specific Mini Security Decision Record (Mini-SDR or MSDR) that follows a specific structured data format to optimize machine-readability. A human-readable version of the Mini-SDR is not required, but providers are
encouraged to considering making such available directly to agency customers in a way that provides an optimal customer experience.

The Mini-SDR may be provided in CSV or JSON. Each option has pros and cons depending on the tools and capabilities of the cloud service provider. FedRAMP has no preference and will accept either.

## Required Fields

- CSV repeats the metadata in every row, followed by `ruleId` and the response fields below. Keep the template’s column names and order.
- JSON uses a `metadata` object and a `responses` object keyed by rule ID.


| Field | What to enter |
| --- | --- |
| `schemaVersion` | `0.1.0` |
| `rulesVersion` | `2026.10.13.01` or the specific version of CR26 that you used. This is just informational. |
| `providerName` | Name of the cloud service provider - please match the information you supply for the Marketplace. |
| `offeringName` | Name of the cloud service offering - please match the information you supply for the Marketplace. |
| `framework` | `Rev5` or `20x`. This just helps automate processing without having to look things up.|
| `class` | `B`, `C`, or `D` for Rev5; `B` or `C` for 20x. This just helps automate processing without having to look things up. |
| `asOfDate` | Date the answers describe, as `YYYY-MM-DD`. It's probably the date that you're writing the Mini-SDR, but it could be the date everything was implemented if you'd like. |
| `fedrampId` | The FedRAMP ID for the cloud service offering, which you should know because it's your unique identifier. |
| `ruleId` | The trigram rule name. All rules are included in the CSV and JSON. |
| `status` | Choose one of: `Fully Implemented`, `Partially Implemented`, `Not Implemented`, `Not Applicable`.|
| `explanation` | A brief, high-level explanation of how the rule is followed, or the reason and risk for not following it. A single overview paragraph is fine. |
| `completionTarget` | Required if the status is `Partially Implemented` or `Not Implemented`: `YYYY-MM-DD`, `Unknown`, or `Not Planned`. |
| `completionTargetExplanation` | Required for `Unknown` or `Not Planned`; explain the uncertainty or decision. |
| `customerRisk` | Required if the status is `Partially Implemented` or `Not Implemented`: A short explanation of the risk to federal customer data of partially or not implementing this rule. |
| `providerCompensation` | Required if the status is `Partially Implemented` or `Not Implemented`: A short explanation of what you've done to reduce the risk of partially or not implementing this rule. |
| `agencyCompensation` | Required if the status is `Partially Implemented` or `Not Implemented`: A short explanation of actions agency customers might take to the reduce the risk of your partially or not implementing this rule. |
| `additionalAssurance` | Optional additional information that you would like to provide to assure agency customers that you are keeping their data safe. |
| `feedback` | Optional feedback about the rule itself for FedRAMP or agencies. |

## CSV Template & Schema

CSV allows individuals to use familiar spreadsheet editing software to manually draft responses, and is most appropriate for cloud service providers that do not use automated tooling to maintain security information. CSV is not an acceptable format for a full Security Decision Record, but the Mini-SDR for VDR/VER implementation is a simple enough data structure that using CSV is awkward but manageable. One downside to the CSV approach is that there will be duplicative information (such as the FedRAMP ID) in every row.

Cloud service providers are still strongly encouraged to ensure their CSV file is valid against the [CSV schema](https://digital-preservation.github.io/csv-schema/), using the provided tools.

- [Download the CSV template](/assets/implementation-status.csv)
- [Download the CSV schema](/assets/implementation-status.schema.csvs)

## JSON Schema

JSON is optimized for automated output from tools that generate the Mini-SDR on the fly using data stored in other systems. It generally should not be edited by humans directly. The JSON schema for the Mini-SDR is a simplified introduction to FedRAMP schemas.

Unlike typical FedRAMP schemas, the Mini-SDR schema is exhaustive and can be used to generate a template. Please only provide a JSON file that exactly matches the JSON schema, without adding or removing any fields.

- [Download the JSON schema](/assets/implementation-status.schema.json)


