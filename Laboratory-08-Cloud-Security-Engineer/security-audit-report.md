# Security Audit Report

## Principle of Least Privilege (PoLP)

The Principle of Least Privilege means giving users and applications only the permissions they need to perform their tasks. This is important in cloud computing because limiting access reduces the damage that can occur when an account is compromised.

## Attack Surface

An attack surface refers to all possible entry points that an attacker could use to access a virtual machine. These may include open network ports, running services, user accounts, and software vulnerabilities.

## Default Deny Policy

A Default Deny Policy blocks incoming network connections unless they are specifically allowed by firewall rules. This is safer than trying to block individual attackers because unauthorized traffic is rejected automatically, including traffic from unknown threats.

## Initial Security Audit

The initial audit will identify listening TCP and UDP ports using the `ss` command. Services that do not need to be publicly accessible should remain protected by firewall rules.
