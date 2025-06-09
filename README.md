> [!IMPORTANT] 
> We are archiving this repository, as the Mainframe SIG's work is contributed to the specification, semantic conventions, Collector, and instrumentation repositories, and there's no need for a standalone repository for this SIG. The SIG is still very active! Please join us in our [weekly meetings](https://github.com/open-telemetry/community?tab=readme-ov-file#specification-sigs) or on [Slack](https://cloud-native.slack.com/archives/C05PXDFTCPJ) if you are interested in using or contributing to OpenTelemetry's mainframe efforts.

# Mainframe Special Interest Group
This is the home of the Specifial Interest Group (SIG) "OpenTelemetry on Mainframe". 
Our aim is to enable OpenTelemetry for the Mainframe and to contribute to the integration of the Mainframe into the OpenTelemetry ecosystem.

## Objectives
The Mainframe SIG will contribute to the OpenTelemetry in the following areas:
1. **Semantic Conventions:** Unify the mainframe resource naming using the [OpenTelemetry Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/) and map basic mainframe concepts to the conventions. 
2. **Code Instrumentation:** Create SDKs for mainframe-specific languages, e.g., COBOL and PL/1 and port of relevant [existing language SDKs](https://opentelemetry.io/docs/languages/) (go, python etc.) to z/OS and Linux on IBM Z.
3. **Collector Enhancements:** Port and maintain the collector to zos/s390x and linux/s390x, enhance the collector to gather platform-specific telemetry.

## Purpose of this repository

We will use this repository to manage the activities and backlog of SIG. If you have a request for a mainframe-specific OpenTelemetry functionality, please open an issue [here](https://github.com/open-telemetry/sig-mainframe/issues).

The SIG will use this repository to store pre-release content (draft documents and code) before actually opening issues and PRs for contributing it to the respective OpenTelemetry project repositories. 

## Meetings

Regular SIG Meeting: Tuesdays at 10 a.m. PDT
- [Zoom Meeting](https://zoom.us/j/96213920701?pwd=NnRFemhtWUJFeEhvRU5Wbk5TKzY5QT09)
- [Meeting notes and agenda](https://docs.google.com/document/d/14p-bpofozTL4n3jy6HZH_TKjoOXvog18G1HBRqq6liE/edit#heading=h.pss2tdsd549w)

## Project Leadership
- [Ruediger Schulze](https://github.com/rrschulze), IBM 
- [Aaron Young](https://github.com/youngaaronm), Broadcom Inc.

## Contact
[#otel-mainframes](https://cloud-native.slack.com/archives/C05PXDFTCPJ)
