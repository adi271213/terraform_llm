# Terraform LLM Auditor Benchmark

This repository contains a research benchmark for evaluating whether Large Language Models can safely audit Terraform infrastructure-as-code against AWS security controls.

The project focuses on a security-critical failure mode called **Unsafe Compliance**, where an LLM incorrectly classifies a genuinely misconfigured Terraform snippet as compliant.

## Motivation

LLMs are increasingly used as security assistants, code reviewers, and compliance copilots. However, in cloud security and infrastructure-as-code workflows, a wrong approval can create false assurance.

This benchmark evaluates whether LLMs can act as reliable compliance auditors for Terraform IaC, using AWS CIS-style controls and Checkov as a static-analysis baseline.

## Current scope

- AWS IAM controls
- AWS S3 controls
- AWS CloudTrail and logging controls
- Terraform secure, misconfigured, and borderline snippets
- Comparison between LLM outputs and Checkov findings

## Key metric

### Unsafe Compliance Rate

Unsafe Compliance Rate measures how often a model labels a genuinely misconfigured Terraform snippet as secure or compliant.

This is important because false approval is more dangerous than simple uncertainty in security review workflows.

## Repository status

This project is under active development as part of my MSc Cyber Security Engineering research at the University of Warwick.
