# Cloud Intelligence Dashboards (CUDOS Framework)

## News Corp Customisation

### Changes

- add optimization data collector files for customisation and uploaded to ap-southeast-2 region
- rename tao dashboard in cfn

### Legacy changes

- rename dashboard
- deploy multi-payers TAO dashboard in a QuickSight
- bugfix: refresh-data not a valid identifier

### Documentation

- [Cost Intelligence and Trusted Advisor Org Dashboard](https://newscorp.atlassian.net/l/c/e5A92FrC)


---

[![PyPI version](https://badge.fury.io/py/cid-cmd.svg)](https://badge.fury.io/py/cid-cmd)

## Welcome to Cloud Intelligence Dashboards (CUDOS Framework) automation repository

### The scripts in this repo have been succesfully tested in [AWS CloudShell](https://console.aws.amazon.com/cloudshell/home) (`recommended`)

## Supported dashboards
- [CUDOS Dashboard](https://d1s0yx3p3y3rah.cloudfront.net/anonymous-embed?dashboard=cudos)
- [Cost Intelligence Dashboard](https://d1s0yx3p3y3rah.cloudfront.net/anonymous-embed?dashboard=cost_intelligence_dashboard)
- [Trusted Advisor Organisation (TAO) Dashboard](https://d1s0yx3p3y3rah.cloudfront.net/anonymous-embed?dashboard=e1799d0d-166c-4e61-8fa6-5c927f70c799)
- [Trends Dashboard](https://d1s0yx3p3y3rah.cloudfront.net/anonymous-embed?dashboard=tao-dashboard?dashboard=trends-dashboard)

:white_check_mark: means that the step you are reading below *Is* compatible with a deployment of the dashboards that used the [Cloudformation deployment method](https://wellarchitectedlabs.com/cost/200_labs/200_cloud_intelligence/cost-usage-report-dashboards/dashboards/2b_cudos_dashboard/#option-3-cloudformation-deployment)

:heavy_exclamation_mark: means that the step you are reading *Is not* compatible with a deployment of the dashboards that used the [legacy automation](./legacy)

## Before you start
1. :heavy_exclamation_mark: Complete the prerequisites for respective dashboard
    - [CUDOS Dashboard](https://wellarchitectedlabs.com/cost/200_labs/200_cloud_intelligence/cost-usage-report-dashboards/dashboards/1_prerequistes/)
    - [Cost Intelligence Dashboard](https://wellarchitectedlabs.com/cost/200_labs/200_cloud_intelligence/cost-usage-report-dashboards/dashboards/1_prerequistes/)
    - [Trusted Advisor (TAO) Dashboard](https://wellarchitectedlabs.com/cost/200_labs/200_cloud_intelligence/trusted-advisor-dashboards/dashboards/1_prerequistes/)
    - [Trends Dashboard](https://wellarchitectedlabs.com/cost/200_labs/200_cloud_intelligence/trusted-advisor-dashboards/dashboards/1_prerequistes/)

2. :heavy_exclamation_mark: [Specifying a Query Result Location Using a Workgroup](https://docs.aws.amazon.com/athena/latest/ug/querying.html#query-results-specify-location-workgroup)

## How to use

1. Launch [AWS CloudShell](https://console.aws.amazon.com/cloudshell/home) or your local shell

    Automation requires Python 3

2. Make sure you have latest pip package installed
    ```bash
    python3 -m ensurepip --upgrade
    ```

4. Install CID Python automation PyPI package
    ```bash
    pip3 install --upgrade cid-cmd
    ```

### Usage Demo

   [![asciicast](https://asciinema.org/a/467770.svg)](https://asciinema.org/a/467770)

## Troubleshooting 

If you experience unexpected behaviour of the cid-cmd script please run cid-cmd in debug mode 

```bash
cid-cmd -vv [command]
```
    
This will produce a log file in the same directory that were at the tile of launch of cid-cmd. 

:heavy_exclamation_mark:Inspect the produced debug log for any sensitive information and anonimise it.

We encourage you to open [new issue](https://github.com/aws-samples/aws-cudos-framework-deployment/issues/new) with description of the problem and attached debug log file.

## Legacy (bash) automation has been moved under [**legacy**](./legacy/) directory
