## How does the Team contact me and sends me their code base for security review?

1. They actually verify their code on etherscan and sends us the link for security review:

CodeV1: 💻 Security Review - https://sepolia.etherscan.io/address/0x2ecf6ad327776bf966893c96efb24c9747f6694b

**1->** This is unacceptable to make a security review of a code base that is exclusively on etherscan and it should be made clear.

**2->** Its clear we are looking for as much bugs as possible, but we are looking also to code maturity; if there is no test suite, no deployment suite or others, how much sure is the code base?

**3->** My job as a security reviewer is to make sure the team/ protocol lives more educated on how to make their codebase more secure; I have to make sure that they are armed with knowledge to be as save as possible

**4->** Remember security is a culture not a one time thing; do your best to make them better and even if it is for writing better test.

## Before starting an Audit we should check the Audit readiness of the protocol/Team

Do they have:

### Simple security checklist:

1.  Tests suite with code coverage?
2.  Fuzzing, static analysis
3.  NatSpec especially for external/public function

### The rekt test: [>-Link-<](https://blog.trailofbits.com/2023/08/14/can-you-pass-the-rekt-test/)

1.  Do you have all actors, roles, and privileges documented?
2.  Do you keep documentation of all the external services, contracts, and oracles you rely on?
3.  Do you have a written and tested incident response plan?
4.  Do you document the best ways to attack your system?
5.  Do you perform identity verification and background checks on all employees?
6.  Do you have a team member with security defined in their role?
7.  Do you require hardware security keys for production systems?
8.  Does your key management system require multiple humans and physical steps?
9.  Do you define key invariants for your system and test them on every commit?
10. Do you use the best automated tools to discover security issues in your code?
11. Do you undergo external audits and maintain a vulnerability disclosure or bug bounty program?
12. Have you considered and mitigated avenues for abusing users of your system?

Code maturity is important

### This code base(etherscan does not pass the rekt test) so we do not go for any security review with the protocol/Team

2. Since they don't pass the rekt test and we denied to review the code, they send us a second version of the code:

CodeV2: 💻 Security Review - https://github.com/Cyfrin/3-passwordstore-audit

We now have a much better version here, structure project with the actual codebase, we've got a script for how they actually deploy everything, with a readme though it looks like a basic foundry project(Not quietly what we want here), we can seems to find any test folder, not only tests not present we are not event sure of what we want to audit, did they change the thinks in lib folder? ..
so before beginning anything we should make sure we "scoped" it, ask question on what exactly should be audited, you can reffered to:
[>-minimal-onboarding-questions.md-<](minimal-onboarding-questions.md)
We are going to send them this minimal onboarding questions and wait for the response, we need the documentaion and more context.

1. They contact us back with a new codebase:
   CodeV3: 💻 Security Review - https://github.com/Cyfrin/3-passwordstore-audit/tree/onboarded

They have filled and send us back the minimal-onboarding-questions form:
[>-minimal-onboarding-filled.md-<](minimal-onboarding-filled.md)
