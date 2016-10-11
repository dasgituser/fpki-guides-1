---
layout: default
title: Federal PKI Overview
permalink: /overview/
---

## Overview

The Federal Public Key Infrastructure encompasses the Certificate Authorities which issue:

1. PIV credentials and person identity certificates 
2. PIV-Interoperable credentials and person identity certificates
3. Other person identity certificates
4. Device identity certificates

The participating Certificate Authorities **and** the Policies, Processes, and Auditing of all the participants is referred to as the **Federal Public Key Infrastructure (FPKI)**

## Example
To give a simple example, we'll explain the PIV certificates.  Although we have many other types of identity certificates, it's easiest to explain with **PIV** since you might have one: 

* Identity certificates are issued and digitally signed by a _Certificate Authority_.  
* The _Certificate Authority_ that issued and digitally signed your PIV certificates is called an _Intermediate Certificate Authority_ because it was issued a certificate by another _Certificate Authority_.  
* This process of issuing and signing continues until there is one  _Certificate Authority_ that is called the _Root Certificate Authority_.

The full process of proving identity when issuing the certificates, auditing the certificate authorities, and the cryptographic protections of the digital signatures establish the basis of Trust. 

![Example of an identity certificate with intermediate and root](../img/certificatechain_small.png){:style="float:center"}

The US Federal Government has also established Trust with other Certificate Authorities which serve business communities, State and Local government communities, and international government communities.

For the US Federal Government Executive branch agencies, there is one Root Certificate Authority named _Federal Common Policy Certificate Authority (COMMON)_, and dozens of Intermediate Certificate Authorities, and Bridged Certificate Authorities.  

*  [A graph of the federal public key infrastructure, including the business communities](https://fpki-graph.fpki-lab.gov/)

<div style="float:right; padding:10px; margin-right:20px; border-radius:10px; width:180px; height:40px; box-shadow:3px 3px 5px 0px; text-align:center; background-color:#CCC; color:#666666">
<div style="color:#000000">
<em>Introduction</em>
</div>
</div>

This section will help you quickly understand the basics of Federal PKI certificates, certificate policy, and certificate revocation lists (CRLs). This section will also provide you with commonly requested Federal PKI links.

1. [What are Certificates?](#public-key-certificates) 
2. [What is a Certificate Policy?](#certificate-policy)
3. [What are Certificate Revocation Lists (CRLs)?](#certificate-revocation-lists)
4. [Links to Commonly Requested Federal PKI CRLs and Certificates?](#federal-pki-crls-and-certificates)
5. [Where can I find the Federal Certificate Policies?](#federal-pki-certificate-polices-and-profiles)

### What are Certificates ###

![Example of certificate fields](https://raw.githubusercontent.com/djpackham/fpki-guides/gh-pages/img/certFieldsEx.png){:style="float:right"}

Certificates are files that can be used for gaining access to networks, applications, digitally signing, encrypting, or creating trusted connections. You can review [Details of a PIV Credential](https://gsa.github.io/piv-guides/details/) to learn more about viewing, exporting and understanding PIV certificates. You can also review the [HTTPS-Only Standard](https://https.cio.gov/certificates/) to learn more about certificates use in HTTPS connections.

A certificate can be issued to a person or a device. A certificate includes information about the person/device, the issuer of the certificate, the purpose(s) of the certificate, and other information to verify if the certificate is valid. An example of the common fields/values you'd find in a certificate can be seen to the right.

Similar to a paper certificate, certificates are made valid when they are signed by a recognized and trustworthy authority, known as a Certificate Authority (CA). Learn more about Certificate Authorities by reviewing the [Certificate Authorities page](/ca/). Also, learn more about the different types of certificates by reviewing the [What are the Different Types of Certificates and their Purpose page](/pki/).

### What is a Certificate Policy ###

All certificates are not used for the same reason or issued by the same Certificate Authority. Some certificates may be used for digitally signing a document, another certificate may be used for logging into a website. In simple terms, we can say that a certificate policy is a set of rules used to define the use of a certificate.

Similar to other PKIs, the Federal PKI has defined their own set of rules, or certificate policies, for Federal certificates. In-depth details on the certificate profiles are contained in the current and historical Federal Public Key Infrastructure (FPKI) Policy documents. This table contains links to the most recent documents:

| Certificates    | Policy Update Date  | Link to Profile Information|
| -------------            |:----:               |:----:|
| PIV Certificates           | May 5, 2015             | [Worksheets 5, 6, 8 and 9 in this document](https://www.idmanagement.gov/IDM/servlet/fileField?entityId=ka0t0000000TNP2AAO&field=File__Body__s)|
| PIV _Interoperable_ Certificates           | May 5, 2015             | [Worksheets 4, 5, 6, and 7 in this document](https://www.idmanagement.gov/IDM/servlet/fileField?entityId=ka0t0000000TN9YAAW&field=File__Body__s)|

![Example of certificate fields](https://raw.githubusercontent.com/djpackham/fpki-guides/gh-pages/img/certPolicy.PNG){:style="float:right"}

An example of a certificate policy is demonstrated to the right. If you lookup this policy in the Federal PKI Certificate Policy doc, you'll see that the policy identifier is mapped to the policy called *id-fpki-common-policy*. **NOTE: (Add brief description of what id-fpki-common-policy means).**

Following this example, an application can establish trust by only accepting certificates that include the *id-fpki-common-policy* policy in their certificate.   

### What are Certificate Revocation Lists ###
Various events can occur that require a certificate (or a set of certificates) to no longer be trusted.  When those events occur, the certificate needs to be revoked and Relying Parties notified,  Examples of such events include:

- Lost, stolen, damaged, or misused certificate.  
- Compliance issues with or a security breach of the Certification Authority that issued the certificate.  
- Termination of employment of certificate holder.
- Certificate holder switches to a different job role (e.g., switching from Role A to Role B, and the certificate is designated for use only by Role A), 
- Certification Authority that issued the certificate terminates its relationship with the Federal PKI.

> In technical terms, *a certificate should be revoked when the binding between the subject and the subject’s public key defined within a certificate is no longer considered valid*.

To notify Relying Parties of revoked certificates, CAs publish Certificate Revocation Lists (CRLs), which are simple lists of certificates that have been revoked and should no longer be relied upon.  

> Relying Parties Parties should obtain CRLs on an ongoing basis and process them accordingly. CAs publish CRLs on a regular schedule and on an emergency basis - as specified by applicable certificate policy.

> To help Relying Parties find CRLs, CAs make public both a description of how to obtain revocation information for the certificates they publish and an explanation of the consequences of using out of date revocation information.  

### Illustration of a Certificate and CRL ###

<img src="/img/crls_diagram1.jpg"/>


<!-- TODO: Reuse same information and visuals from here https://github.com/GSA/piv-guides/blob/staging/pages/certchains.md -->


