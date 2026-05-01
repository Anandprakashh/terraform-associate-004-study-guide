What is Infrastructure as Code (IaC)?

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure using machine‑readable configuration files instead of manual processes or point‑and‑click tools.

IaC treats infrastructure the same way software treats code — versioned, repeatable, testable, and automated.
⭐ Why IaC Exists

Before IaC, infrastructure was created manually:

    Clicking through cloud consoles

    Running ad‑hoc scripts

    Configuring servers by hand

    No consistent documentation

    Hard to reproduce environments

This led to:

    Drift

    Human error

    Slow deployments

    Inconsistent environments

IaC solves these problems by making infrastructure predictable, consistent, and automated.
⭐ Benefits of IaC (Exam‑Critical)

These benefits appear in exam questions frequently:
1. Consistency & Repeatability

Same configuration = same infrastructure every time.
2. Version Control

IaC files can be stored in Git, enabling:

    history

    rollbacks

    collaboration

    code reviews

3. Automation

IaC integrates with CI/CD pipelines for:

    automated provisioning

    automated testing

    automated deployments

4. Reduced Human Error

No manual clicking → fewer mistakes.
5. Faster Provisioning

Infrastructure can be created in minutes, not hours.
6. Documentation

The code is the documentation.
⭐ Declarative vs Imperative IaC (Exam‑Critical)
Declarative (WHAT you want)

You define the desired end state.

Terraform is declarative.

Example:
hcl

resource "aws_s3_bucket" "example" {
  bucket = "my-bucket"
}

You don’t tell Terraform how to create it — only what you want.
Imperative (HOW to do it)

You specify step‑by‑step instructions.

Example:
code
aws s3 mb s3://my-bucket
aws s3api put-bucket-versioning ...

The exam will ask you to identify which approach Terraform uses → Declarative.
⭐ How Terraform Implements IaC

Terraform uses:

    Configuration files (.tf)

    A declarative language (HCL)

    A state file to track real infrastructure

    A plan/apply workflow

    Providers to interact with cloud APIs

Terraform ensures the real infrastructure matches the desired configuration.
⭐ IaC Exam Traps (Important)

These appear often:
❗ IaC is NOT:

    A scripting language

    A replacement for cloud provider APIs

    A configuration management tool (like Ansible)

❗ Terraform is NOT:

    Imperative

    A tool that executes commands step‑by‑step

    A tool that automatically fixes drift without apply

❗ IaC does NOT:

    Guarantee security by itself

    Replace DevOps practices

    Remove the need for cloud knowledge

⭐ Summary (For Quick Revision)

    IaC = managing infrastructure using code

    Terraform uses declarative IaC

    IaC brings consistency, automation, versioning, and speed

    Terraform ensures desired state matches real state

    IaC reduces human error and drift